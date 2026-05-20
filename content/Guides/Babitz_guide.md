---
title: Babitz guide
namespace: ''
original_url: https://warforkwiki.com/index.php?title=Babitz_guide
aliases:
- Babitz_guide
---

**If you don't want to bother with any of this, but want basically the same effect, follow [this](https://github.com/babitz0r/warfork_ansible) ansible guide, it will do everything that's in this tutorial plus a little extra.**

Original guide from [here](https://babitz.cf/warfork/multiple_server_guide.html).

First off, if you have any problems understanding this, or if you need me for whatever reason, you can always catch me on discord. I'm Babitz#4571
I'm also in the game's official discord server so you can catch me there as well.

This guide is based on this one to a relatively decent extent: [steam thread](https://steamcommunity.com/app/671610/discussions/0/1642045637381200640/)

I just did some minor changes and I'm going to show you how to set up multiple servers / instances of Warfork on the same Linux based server.

If anyone wants to turn this into a steam guide or put a copy or a modified version anywhere else, or if you want to base your guide on this, you don't have to ask for my permission. I'd like to know if you do so I can check it out, though. So hit me up with your link.

Requirements:

\- a Linux based server

\- basic familiarity with the command line

Ok, with that out of the way, let's move on.

## The Basics

You're going to need to install steamcmd for this so in case you want to use steamcmd for other purposes, you just might want to name the user steam like I did.

Install the dependencies first:

Ubuntu / Debian 64 bit

apt install lib32gcc1

RedHat/CentOS

yum install glibc libstdc++

RedHat/CentOS 64-Bit

yum install glibc.i686 libstdc++.i686

Ok. Moving on. We need our user.

useradd -m steam -s /bin/bash

su steam

cd

You should be in your steam home folder now

Grab steamcmd and extract it:

curl -sqL "<https://steamcdn-a.akamaihd.net/client/installer/steamcmd_linux.tar.gz>" \| tar zxvf -

Now we're ready to install the game

cd steamcmd
./steamcmd.sh

Now wait for some update checks, etc. and you should find yourself in the interface. Should show something like this now:

Steam\>

So let's login. You can login with your regular steam credentials that you use normally.

Steam\>login yourusername

It will prompt you for your password so once you're done with that I would recommend you force it to install to a specific directory within this user, unless you prefer hunting it down wherever it might end up on the server. I prefer to have it nice and close by.

I did it like this:

Steam\>force_install_dir ./warfork/

Just dot might have sufficed as I just made an extra directory this way, but oh well.

Now to install run

Steam\>app_update 671610 validate +quit

This will install the game and exit steamcmd. We're now done with this, at least until there's an update. When an update rolls out you will have to repeat this whole step all the way from the login, and yes, this includes the force_install_dir bit.

Now we're ready to run the server.
If you did everything like I did your path to where you should now go should now look like

cd ~/steamcmd/warfork/Warfork.app/Contents/Resources

Before you run it I would recommend installing "screen" if you don't have it on the server already:

apt install screen

or

yum install screen

You know the drill.
Screen will allow us to do something like having tabs and to exit the server without closing our warfork server. If you want to know more use:

man screen

or

screen --help

For more details about it, but we'll just need a handful of commands with it.

Let's create a screen in which we will run our server.

screen -S warfork

From here just run

./wf_server.x86_64

Now the server should boot up and if it ends up with something like this you did it right:

Gametype 'Clan Arena' initialized

  
AI Navigation Initialized.

------------------------------------------------------------------------

You're now in the server's very own console. You can type stuff and even say things to people on the server. To get the server in the ingame browser you'll want to type "heartbeat" in and you should get an output like this:

heartbeat

Sending heartbeat to 67.205.150.215:27950

Sending heartbeat to 107.161.23.68:279501

Type something like "say hello" or "kick babitz". You can monitor what's going on from here and this gets logged as well.

To leave from this screen into your main shell, hold ctrl and press A and then D.
You can view your current screens with

screen -ls

And if you did everything like in this guide, return to the screen with

screen -r warfork

Now we're back at our warfork server.
Ok, now ctrl + C out of this for now.
And let's also press ctrl + D to terminate this screen.

Let's configure your default config. It's relatively self explanatory and it has helpful comments in case you're unsure. I'm going with vim, but you should use whatever you prefer. You can use notepad out of FTP if you like.

vim ~/steamcmd/warfork/Warfork.app/Contents/Resources/basewf/dedicated_autoexec.cfg

Change this line into whatever you want your server to be named:

set sv_hostname "your server name"

You can also add colors to it same with your nickname, but that's a bit out of the scope of this .txt. Again, this .cfg is very self explanatory and sort of beyond the scope of what I am aiming for with this. So if you want to make a certain map rotation, force only one or only specific gamemodes, you're on your own. But again, it's very straightforward and self explanatory so just go through the .cfg and I'm sure you'll figure it out. That's all beyond the scope of this guide. What we're interested in is setting up multiple servers, so let's do just that.

There's two ways we can go about this. One way is to add parameters when we launch the server, which is good when you only want some small changes. The other is to create another configuration file and launch with that.

## Adding parameters to the server launcher

After you've configured your dedicated_autoexec.cfg, whatever changes you want to make to it you can use "+parameter" from the cfg that you wish to change. You will also need to set every server to a different port. So let's say you're running a default server with all gamemodes and all maps, which is what I'm doing. Let's say you want a different name for it and just make it a different name with instagib.

You would run

./wf_server.x86_64 +sv_hostname "your other server name" +sv_port "44401" +g_instagib "1"

This way you can change everything from your default setting, you can cram all of those parameters from the dedicated_autoexec.cfg and make something like a duel only server or a private ictf only server, etc. Just check that config and again, this should all be straightforward now.

But, this is a pain in the ass. It's a pain in the ass to have to directory hop all the way here. I mean it's like \*counts\* 7 whole directories before the server starting file AND on top of that you're supposed to run a stupidly long command. Thankfully, we're on linux, so we have ways to make life easier for ourselves. You may see where I'm going with this already.

First, let's stay in our current directory. Here's what I did.

We're still in ~/steamcmd/warfork/Warfork.app/Contents/Resources/

Create a file you're going to execute. Use whatever you like and name the file whatever you like, I'm going with vim. This is where you will create your custom, other servers.

vim wfsig

And then in here I added this:

cd ~/steamcmd/warfork/Warfork.app/Contents/Resources/
~/steamcmd/warfork/Warfork.app/Contents/Resources/wf_server.x86_64 +sv_port "44401" +g_instagib "1" +sv_hostname "^4babi^0t^4z's ^3instagib playground ^7- ^1ALL ^5gamemodes"

Obviously, name the file whatever you want, it doesn't have to be wfsig. It's how I named this to know it's a warfork server running with instagib.
Using the cd command might seem redundant here, but we're playing the long game here.

Now let's make it executable.

chmod +x wfsig

Now I can just run

./wfsig

And I can run it without writing all those parameters or copypasting them from somewhere every time. But let's go a bit further. Let's make it so we can run it with one command as soon as we log in as the steam user.

Go here. Edit what you want with etc. vim is for winners.

vim ~/.bashrc

We're adding this:

alias wfsnw="cd ~/steamcmd/warfork/Warfork.app/Contents/Resources/; ./wf_server.x86_64"
alias wfsig="~/steamcmd/warfork/Warfork.app/Contents/Resources/wfsig"

Don't forget to do this to apply the changes

source ~/.bashrc

You should understand what this does. You have to be in that directory to execute the file right, so we're cd-ing there for that reason. And yes I know I could have added the cd command for my custom server config here instead of in the wfsig file.

So now I can run this from wherever I am as long as I'm the steam user. Typing

wfsnw
or
wfsig

will bring me into the directory with those executables and run the server with my default or altered config rulesets.

So let's say I'm logged in as steam and want to run both servers. I would do something like this (you can name the screen whatever you like):

screen -S wf1
wfsnw

Don't forget to use the heartbeat command once the server starts running.
Then leave the screen by holding down ctrl and pressing A then D.

screen -S wf2
wfsig

Same process. Wait for the server to initialize and type "heartbeat" and go back with ctrl + A, D.

Then if you want to monitor or stop the first server for whatever reason, just type

screen -r wf1

To view all your screens, run

screen -ls

Now if you want to do some more changes to the server parameters and you want to have a few servers with drastically different settings, adding all those parameters in the launch command is a bit of a pain in the ass, even if you save them in a custom config command. Overall a much cleaner approach would be to go with method 2.
Without futher ado:

## Launching with another configuration file.

Go to your basewf directory. If you did everything like I did it's:

cd ~/steamcmd/warfork/Warfork.app/Contents/Resources/basewf/

Copy the existing default config and name it something else:

cp -p dedicated_autoexec.cfg test.cfg

Then edit it. Again, edit what you like in, I'm going with vim. Make sure you change the port. Just going +1 for every server is fine.

vim test.cfg

Now let's back up a bit and launch it.

cd ..
./wf_server.x86_64 +exec test.cfg

Ok let's type heartbeat and view it in the ingame browser to confirm it's working. It should. Ok, let's ctrl + C out of this.

We're smart so we're not going to launch this way, we like making our life easier, so we'll set up an alias. Time to visit .bashrc again.

vim ~/.bashrc

Add the following:
alias wftest="cd ~/steamcmd/warfork/Warfork.app/Contents/Resources/;./wf_server.x86_64 +exec test.cfg"

Don't forget to apply the changes.

source ~/.bashrc

Now wherever we are as the steam user we can freely start the server. Let's go into a screen:

screen -S anything
wftest

Type heartbeat and check if the game is in the ingame browser.
Now we're done and we can leave the screen with ctrl + A, D.

And now you can make as many configs and aliases and launch them in as many screens as you like, same like in method 1. Just don't forget to use different ports for the servers.
One major protip would be to never modify the default_autoexec.cfg because it WILL get reset at an update, so best if you have a separate .cfg for every custom .cfg you plan on using.

## BONUS: Let's automate E V E R Y T H I N G

Every proper server admin is lazy and is looking to relegate as much work to the computer as possible, so why would we be different.

Let's go back to our beloved .bashrc

vim ~/.bashrc

First off, I hate changing directories to ~/steamcmd/warfork/Warfork.app/Contents/Resources/ every now and then. So I'll just make an alias:

alias cdwfs="cd ~/steamcmd/warfork/Warfork.app/Contents/Resources/"

Now we can make some other aliases a little cleaner and nicer to look at. And have less for us to write later. For example the alias from earlier:

alias wftest="cd ~/steamcmd/warfork/Warfork.app/Contents/Resources/;./wf_server.x86_64 +exec test.cfg"

Now becomes:

alias wftest="cdwfs;./wf_server.x86_64 +exec test.cfg"

Now let's create a screen with a server running without entering the screen ourselves. Also let's enter "heartbeat" at the same time.

alias screentest="screen -d -m -S testscreen; screen -S testscreen -X stuff "wftest^M"; screen -S testscreen -X stuff "heartbeat^M"

Don't forget to

source ~/.bashrc

Let's break it down a bit if you're interested what this command does:

screen -d -m -S testscreen -\> creates a screen called "testscreen", but detached, so we don't automatically enter it once it's created

screen -S testscreen -X stuff "wftest^M" -\> this will send the text "wftest" to our "testscreen" named screen and hit enter. "^M" represents the enter key. This will run the server for us without us entering the screen

screen -S testscreen -X stuff "heartbeat^M" -\> same as above, except this time we're using the server command heartbeat so our server can be discovered in the ingame browser

So let's run

screentest

If we now go into it with

screen -r testscreen

We will see the server is running and heartbeat was sent. Check your ingame browser, the game should be there.

You can do this for multiple servers, of course, which is the idea.
And yes, at the bottom I did create an alias to run ALL of my servers with one command because I can and because I'm lazy. The sleep command makes it wait 1 second after every executed command, otherwise it doesn't quite work, at least not for me. Tested multiple times. Either way, here's a screenshot of my aliases:

[Click](https://babitz.cf/warfork/myaliases.png).

---
title: Streaming to Steam Store
namespace: ''
original_url: https://warforkwiki.com/index.php?title=Streaming_to_Steam_Store
aliases:
- Streaming_to_Steam_Store
---

Streaming Warfork's gameplay to Steam lets new players watch the live gameplay if they visit Warfork's store page. No software is mandatory for streaming to Store page, however it's possible to use [OBS Studio (obsproject.com)](https://obsproject.com/) if you want to stream in higher quality. This guide will cover both methods.

## Streaming directly from Steam client

Streaming to the Store page using the built-in broadcasting function in Steam client is the easiest and fastest option, however the streams have limited bitrate and framerate.

### Setting things up

1.  Open the Steam client.
2.  Click on Steam in the top left corner and choose Settings.
3.  Choose the Broadcasting tab.
4.  Change the privacy setting to *Anyone can watch my games*.
5.  Choose the quality options depending on your hardware.
6.  Click OK. The gameplay will be automatically streamed every time you're in-game. Steam will only stream the gameplay from Warfork, other games won't be streamed.

## Streaming using 3rd party software

Streaming using 3rd party software takes a bit longer to set up, however the quality can be precisely adjusted and it allows for streaming in high framerates (up to 60 fps).

### Requirements

You need to have a 3rd party streaming software and your Steam account needs to be a member of the [Store Broadcast Beta](https://steamcommunity.com/groups/storebroadcastbeta) Steam group.

### Configuration

1.  Open the [Steam broadcasting](https://steamcommunity.com/broadcast/upload/) page.
2.  Generate the RTMP token.
3.  **To make the stream visible on the Store page, add additional information:**
    1.  Broadcast App ID: 671610
    2.  Viewer Permission: Public
    3.  Create Chat Message Permission: Public
4.  Paste the upload server and RTMP token into the 3rd party streaming software.
5.  Configure the encoder settings according to this [site](https://partner.steamgames.com/doc/store/broadcast/setting_up).
6.  Start your stream.

## Notes

- **Only accounts permitted by [[User:Caine|Caine]] will have their streams visible on the Steam's Store page. You can ask for permission on the [Discord](https://discord.gg/VY95TKZ) server.**
- Your Steam account cannot be Steam Community banned and your Steam profile needs to be public.
- Steam doesn't save the broadcasts. If you want to save the broadcast, you need to record it using the [[Streaming to Steam Store#Streaming using 3rd party software|3rd party software]] method.
- Do not stream anything other than Warfork onto the Steam page. Doing so will get your permission revoked.

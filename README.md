# VCPlayerBot

![GitHub Repo stars](https://img.shields.io/github/stars/subinps/VCPlayerBot?color=blue&style=flat)
![GitHub issues](https://img.shields.io/github/issues/subinps/VCPlayerBot)
![GitHub pull requests](https://img.shields.io/github/issues-pr/subinps/VCPlayerBot)
![GitHub contributors](https://img.shields.io/github/contributors/subinps/VCPlayerBot?style=flat)
![GitHub forks](https://img.shields.io/github/forks/subinps/VCPlayerBot?style=flat)

Telegram bot to stream videos in telegram voicechat for both groups and channels. Supports live streams, YouTube videos and telegram media. With record stream support, Schedule streams, and many more.

## Config Vars:
### Mandatory Vars
1. `API_ID` : Get From [my.telegram.org](https://my.telegram.org/)
2. `API_HASH` : Get from [my.telegram.org](https://my.telegram.org)
3. `BOT_TOKEN` : [@Botfather](https://telegram.dog/BotFather)
4. `SESSION_STRING` : Generate From here [![GenerateStringName](https://img.shields.io/badge/repl.it-generateStringName-yellowgreen)](https://repl.it/@subinps/getStringName)
5. `CHAT` : ID of Channel/Group where the bot plays Music.

## Recommended Optional Vars

1. `DATABASE_URI`: MongoDB database Url, get from [mongodb](https://cloud.mongodb.com). This is an optional var, but it is recomonded to use this to experiance the full features.
2. `HEROKU_API_KEY`: Your heroku api key. Get one from [here](https://dashboard.heroku.com/account/applications/authorizations/new)
3. `HEROKU_APP_NAME`: Your heroku apps name.

### Optional Vars
1. `LOG_GROUP` : Group to send Playlist, if CHAT is a Group()
2. `ADMINS` : ID of users who can use admin commands.
3. `STARTUP_STREAM` : This will be streamed on startups and restarts of bot. You can use either any STREAM_URL or a direct link of any video or a Youtube Live link. You can also use YouTube Playlist.Find a Telegram Link for your playlist from [PlayList Dumb](https://telegram.dog/DumpPlaylist) or get a PlayList from [PlayList Extract](https://telegram.dog/GetAPlaylistbot). The PlayList link should in form `https://t.me/DumpPlaylist/xxx`.
4. `REPLY_MESSAGE` : A reply to those who message the USER account in PM. Leave it blank if you do not need this feature. (Configurable through bot if mongodb added.)
5. `ADMIN_ONLY` : Pass `True` If you want to make /play command only for admins of `CHAT`. By default /play is available for all.(Configurable through bot if mongodb added.)
6. `DATABASE_NAME`: Database name for your mongodb database.
7. `SHUFFLE` : Make it `False` if you dont want to shuffle playlists. (Configurable through bot if mongodb added.)
8. `EDIT_TITLE` : Make it `False` if you do not want the bot to edit video chat title according to playing song. (Configurable through bot if mongodb added.)
9. `RECORDING_DUMP` : A Channel ID with the USER account as admin, to dump video chat recordings.
10. `RECORDING_TITLE`: A custom title for your videochat recordings.
11. `TIME_ZONE` : Time Zone of your country, by default IST
12. `IS_VIDEO_RECORD` : Make it `False` if you do not want to record video, and only audio will be recorded.(Configurable through bot if mongodb added.)
13. `IS_LOOP` ; Make it `False` if you do not want 24 / 7 Video Chat. (Configurable through bot if mongodb added.)
14. `IS_VIDEO` : Make it `False` if you want to use the player as a musicplayer without video. (Configurable through bot if mongodb added.)
15. `PORTRAIT`: Make it `True` if you want the video recording in portrait mode. (Configurable through bot if mongodb added.)
16. `DELAY` : Choose the time limit for commands deletion. 10 sec by default.
18. `QUALITY` : Customize the quality of video chat, use one of `high`, `medium`, `low` . 
19. `BITRATE` : Bitrate of audio (Not recommended to change).
20. `FPS` : Fps of video to be played (Not recommended to change.)



## Requirements
- Python 3.8 or Higher.
- [FFMpeg](https://www.ffmpeg.org/).



## Deploy to Heroku

[![Deploy](https://www.herokucdn.com/deploy/button.svg)](https://heroku.com/deploy?template=https://github.com/amanrajput2001/VCPlayerBot)

## Deploy to Railway
[![Deploy on Railway](https://railway.app/button.svg)](https://railway.app/new/template?template=https%3A%2F%2Fgithub.com%2Famanrajput2001%2FVCPlayerBot&envs=ADMIN_ONLY%2CADMINS%2CAPI_HASH%2CAPI_ID%2CBOT_TOKEN%2CCHAT%2CDATABASE_URI%2CHEROKU_API_KEY%2CHEROKU_APP_NAME%2CLOG_GROUP%2CQUALITY%2CREPLY_MESSAGE%2CSESSION_STRING%2CSTARTUP_STREAM&optionalEnvs=ADMIN_ONLY%2CDATABASE_URI%2CHEROKU_API_KEY%2CHEROKU_APP_NAME%2CLOG_GROUP%2CQUALITY%2CREPLY_MESSAGE%2CSTARTUP_STREAM&ADMIN_ONLYDesc=Change+it+to+True+if+you+want+to+make+%2Fplay+command+available+for+everyone&ADMINSDesc=ID+OF+USERS+TO+ACCESS+THE+BOT&API_HASHDesc=api_hash+part+of+your+Telegram+API+Key+from+my.telegram.org%2Fapps&API_IDDesc=api_id+part+of+your+Telegram+API+Key+from+my.telegram.org%2Fapps&BOT_TOKENDesc=Bot+token+of+Bot%2C+get+from+%40Botfather&CHATDesc=ID+of+Channel+or+Group+where+the+Bot+plays+Music&DATABASE_URIDesc=Mongo+DB+database+URI+%2C+get+from+https%3A%2F%2Fcloud.mongodb.com%2C+even+if+this+is+optional%2C+many+of+functions+may+not+work+if+this+is+not+set.&HEROKU_API_KEYDesc=Your+heroku+api+key%2C+get+it+from+https%3A%2F%2Fdashboard.heroku.com%2Faccount%2Fapplications%2Fauthorizations%2Fnew&HEROKU_APP_NAMEDesc=Name+of+your+app&LOG_GROUPDesc=ID+of+the+group+to+send+playlist+If+CHAT+is+a+Group%2C+if+channel+then+leave+blank&QUALITYDesc=Quality+of+video&REPLY_MESSAGEDesc=A+reply+message+to+those+who+message+the+USER+account+in+PM.+Make+it+blank+if+you+do+not+need+this+feature&SESSION_STRINGDesc=Session+string%2C+read+the+README+to+learn+how+to+export+it+with+Pyrogram&STARTUP_STREAMDesc=YouTube+live+%2F+Direct+link+to+a+video+%2F+Telegram+link+to+a+YouTube+playlist.%28Read+the+README+for+more+info.%29&REPLY_MESSAGEDefault=Hey%2C+Iam+a+bot+to+play+music%2C+not+having+time+to+chat+with+you.&referralCode=Vr-DSL)

 
## Deploy to VPS

```sh
git clone https://github.com/subinps/VCPlayerBot
cd VCPlayerBot
pip3 install -r requirements.txt
# <Create Variables appropriately (.env [optional])>
python3 main.py
```

## Features

- Playlist, queue.
- Supports Video Recording.
- Supports Scheduling voicechats.
- Cool UI for controling the player.
- Customizabe to audio or video.
- Custom quality for video chats.
- Supports Play from Youtube Playlist.
- Change VoiceChat title to current playing song name.
- Supports Live streaming from youtube
- Play from telegram file supported.
- Starts Radio after if no songs in playlist.
- Automatic restart even if heroku restarts. (Configurable)
- Support exporting and importing playlist.

### Note

[Note To A So Called Dev](https://telegram.dog/subin_works/203): 

Kanging this codes and and editing a few lines and releasing a V.x  or an [alpha](https://telegram.dog/subin_works/204), beta , gama branches of your repo wont make you a Developer.
Fork the repo and edit as per your needs.

## LICENSE

- [GNU General Public License](./LICENSE)


## CREDITS

- [Laky-64](https://github.com/Laky-64) for [py-tgcalls](https://github.com/pytgcalls/pytgcalls)
- [Dan](https://github.com/delivrance) for [Pyrogram](https://github.com/pyrogram/pyrogram)



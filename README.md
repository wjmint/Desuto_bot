# Desuto_bot
changed the translation engine of twichTransFree

also, it is still beta version! you can only use English, Korean, Japanese now!
when I understand how to scrap, I will fix that problem!

# USAGE
1. rewrite `config.txt`
2. double-click `twitchTransFN.exe`

That's all!

# config.txt
```
######################################################
# PLEASE CHANGE FOLLOWING CONFIGS ####################
Twitch_Channel          = Twich_channel_here

Trans_Username         = Twitch_bot_name_here
Trans_OAUTH              = Oauth_here

#######################################################
# OPTIONAL CONFIGS ####################################
Trans_TextColor         = GoldenRod
# Blue, Coral, DodgerBlue, SpringGreen, YellowGreen, Green, OrangeRed, Red, GoldenRod, HotPink, CadetBlue, SeaGreen, Chocolate, BlueViolet, and Firebrick

lang_TransToHome        = ja
lang_HomeToOther        = en

Show_ByName             = True
Show_ByLang             = True

Ignore_Lang             = 
Ignore_Users            = Nightbot, BikuBikuTest
Ignore_Line             = http, BikuBikuTest
Delete_Words            = saatanNooBow, BikuBikuTest

# Any emvironment, set it to `True`, then text will be read by TTS voice!
gTTS                    = True


#######################################################
# For TLANSLATE ROOM CONFIGS ##########################
##### channelID <- owner_id, roomUUID <- _id ##########
# channelID               = wjmint
# roomUUID                = 00000000-0000-0000-0000-000000000000
```

| Option| Description |
| -- | -- |
| Twitch_Channel | The target chat room for translation. |
| Trans_Username | username for translation |
| Trans_OAUTH | Get key for Trans_Username at https://twitchapps.com/tmi/ |
| Trans_TextColor  | You can change text color of translator. |
| lang_TransToHome | If set it to [`ja`], all texts will be translated to the JAPANESE! |
| lang_HomeToOther | If set it to [`en`], the language in [`lang_TransToHome`] is trans to [`en`]. |
| Show_ByName | If it is set to `True`, user name is shown after translated text. |
| Show_ByLang | If it is set to `True`, the source language is shown after translated text. |
| Ignore_Lang | You can set some languages : [ja,en, ...] |
| Ignore_Users | You can set some users : [Nightbot, BikuBikuTest, someotheruser, ...] |
| Ignore_Line | If the words are in message, the message will be ignored.|
| Delete_Words | The words will be removed from message. |
| gTTS | Any emvironment, text will be read by TTS voice! |
| channelID | (with roomUUID) translated text is send to chat-room |
| roomUUID | (with channelID) translated text is send to chat-room |


# memo
## support language (pypapago)
    -English
    -Korean
    -Japanese

# secret functions
## choose trans destination language (for one text)
At the time of translation, you can select the target language like `en:` at the beginning of the sentence.  
Example) en: こんにちは -> hello

## translated text is send to chat-room
If you want to send the translated text to chat-room in your channel, please read this section.
You can get more information about [chat-room] following blogs.
https://blog.twitch.tv/bring-your-community-together-with-rooms-ad60cab1af0a

1. Make chat-room in your channel.
2. By using `roomUUID_checker.exe`, get `channelID(owner_id)` and `roomUUID(_id)`
3. Set it to config.txt

NOTE: When rewriting config.txt, please delete the `#` mark at the beginning of each setting value!


# Thanks
Thanks to Pioneers!
The developer of ...
- Google
- pypapago by Beomi
    - https://github.com/Beomi/pypapago
- gtts by pndurette
    - https://github.com/pndurette/gTTS
- playsound by TaylorSMarks
    - https://github.com/TaylorSMarks/playsound
- python_twitch_irc by jspaulsen
    - https://github.com/jspaulsen/python-twitch-irc
- twitchTransFreeNext by sayonari
    - https://github.com/sayonari/twitchTransFreeNext
    !!this is the original application!!


# Developer Info.

| Title | Death_troy_bot_powered_by_wjmint|
|--|--|
| Developer | wjmint (original : husband_sayonari_omega) |
| github | https://github.com/wjmint/Desuto_bot |
| original program github | https://github.com/sayonari/twitchTransFreeNext |
| mail | jamie060529@gmail.com |

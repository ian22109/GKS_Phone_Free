# GKS_Phone_Free
Hello there

Please do the following instructions properly for installation

create a [phone] folder in resource before starting the process
Extract the rar files into the file you created
and do the steps one by one in a way that suits you

1. Read the gks_gotur/esx_goturjob.sql file into your database
2. Read the esx_lapraces/lapraces.sql file into your database
3. Read the gksphone/gksphone.sql file into your database


4. don't change the licens key

5. ESX version and Config.lua settings

There is "Config.ESXVersion" in the gksphone/config.lua and gks_gotur/config.lua file, type whatever ESX version you are using (1.1 or 1.2)

6. To take a photo: Open gksphone/html/static/config/config.json Fill in the "PhotoWebHook" field on line 4

7. What you need to set in config.json

When you false ValePoup, you can only show vehicles

When you turn off Facetime, the icons for Facetime calls and the call will be turned off.

If you are not going to use voicemail 
Leave "RecordSite" blank
Make "MessageRecordMic" false


If you turn "BottomNotif" off, you will turn off the logos that appear at the bottom in the middle of the game.

"RealTime" real-time time zone works, if you turn it off, Fivem's own game clock will be active

Set "BlockNumber" to false if you don't want to use Phone number blocking function ( This will just make it send the notification accordingly. )

"BankTransferCom" Bank transfer fee is calculated as %

If the news application is to be used, use the profession code "NewsPerm" in this field.

You need to give permission to create the map in the race application, set the "Race Identifier" field in the config.json as in the example. (Only people you authorize can create a racecourse.)
example:
  "RaceIdentifier" : {
    "0": "char1:39bf1c13e9ce1d00453d549ceed37a08f54e0768",
    "1": "identifier"
  },

Job Notice application;
You can add profession like examples in "JobMessages" field 
(1st area code
The second field is the text written in the profession application.)
For the picture: it is enough to put the picture of the profession in the folder "gksphone\html\static\img\jobs". ( image name : jobcode.png - example : police.png)

example: 
  "JobMessages": {
    "police": "PD",
    "ambulance": "EMS",
    "mechanic": "GKS Mechanic"
  },

To close the applications you do not want, set the "MenuPage" close of the application you want to close from the applications section.

Close application by job: you should write the profession code in the "blockedjobs" section of the application you want in the apps section.
example:       
"blockedjobs": {
        "police": "police",
        "ambulance": "ambulance"
   }


If you want to translate language, just change the texts under "language" section in config.json


8. The important part you need to adjust in config.lua is which sound program you use, you need to true it.
Mumble, PMAvoice, Tokovoip, Saltychat are compatible, you need to make one of them true.

9. To set item images in Gotur;
You must add the images as "itemname.png" in the "gks_gotur/img/" folder

10. Finally, you must start the phone and add-ons in server.cfg.
You can start it at the bottom of server.cfg please note it should start after es_extended and required scripts

ensure gks_gotur
ensure esx_lapraces
ensure xsound
ensure gksphone






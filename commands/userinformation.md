# Trigger
Your preferance, I personally use **?userinfo**

# Code / BDSCRIPT2
```
$nomention

$author[$username[$mentioned[1;yes]]#$discriminator[$mentioned[1;yes]]]
$thumbnail[$userAvatar[$mentioned[1;yes]]]
$color[$getRoleColor[$highestRole[$mentioned[1;yes]]]]

$addField[Origin;<t:$calculate[($mentioned[1;yes] / 4194304 + 1420070400000) / 1000]:f> <t:$calculate[($mentioned[1;yes] / 4194304 + 1420070400000) / 1000]:R>;yes]
$httpPost[https://showcase.api.linx.twenty57.net/UnixTime/tounixtimestamp;{"Datetime": "$userJoined[$mentioned[1;yes];2006/01/02 15:04:05]"}]
$addField[Joined;<t:$httpResult[UnixTimeStamp]:f> <t:$httpResult[UnixTimeStamp]:R>]

$httpGet[https://cryptons.ga/utility/discorduser?id=$mentioned[1;yes]]
$if[$httpResult[bannerURL]==null]
$else
$image[$replaceText[$httpResult[bannerURL];.webp;.gif?size=4096]]
$endif
```

# Features
This has a feature that no other user information has with BDSCRIPT! It has userjoined date in Discord Timestamps.

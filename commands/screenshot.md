# Trigger
Your preferance, I personally use **?screenshot**

# Code / BDSCRIPT2
```
$nomention

$var[isUrl;$checkContains[$message;https://;http://] $checkContains[$message;.com;.org;.xyz;.io;.us;.lol;.gg;.net;.club;.wtf]]

$if[$checkCondition[$var[isUrl]==true true]==false]
$title[Error / Invaild Link]
$description[Your link is invaild, please make sure your link has http or https like `https://discord.com` and uses a supported TLD.

At the moment this commands only supports `.gg`, `.io`, `.us`, `.com`, `.lol`, `.net`, `.org`, `.wtf`, `.xyz`, `.club` TLDs]
$else
$title[Screenshot of $message]
$image[https://image.thum.io/get/width/1200/crop/675/png/$message]
$endif
```

# More TLDs
You make make the command support more TLDs by adding **;.(tld here)** in line 8 with the rest of the TLDs.

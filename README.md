# NightPI
Based on a Raspberry Pi 3B+ with Kali Linux installed, the "NightPi" is a briefcase that has been specially designed to learn and perform penetration testing, investigation (OSINT) and radio.
This repository contain all usefull explanation about how to make one, so don't hesitate to build for yourself this usefull tool and improve it :D
# Features
In order to be rapidly deployable, some features has been added :
- Offline database with documentation of many programs
- High security browser (protection against fingerprint + TOR proxy)
- Extra open-source tools installed (OSINT, SDR, etc)

## Offline database
<img src="https://github.com/Sekhan/NightPI/blob/master/HTTrack.jpg" alt="Offline Database" align="right" height="220px">

While Kali Linux come with a incredible amount of software, the issue is that if you want to learn how to use them, you'll need to rely on a internet connection and search for each documentation separately. **Centralizing all these usefull informations in one database by using a open source software like HTTrack is way more convenient :)**

Depending on each site, you may have to change some parameters. 
**Here is what I've modified in the option panel :**

- *Scan rules* (to prevent to download unwanted files) :
`+*.png +*.gif +*.jpg +*.jpeg
+*.css +*.js -ad.doubleclick.net/* -mime:application/foobar
-*.zip -*.tar -*.tgz -*.gz
-*.rar -*.z -*.exe -*.7z -*.pdf -*.xz -*.iso`

- *Build* : activate `No error page` and `No external page`
- *Link* : activate `Attempt to detect all links`, `Get non-html files related to a link`, `Test validity of all links`
and `Get HTML files first`
- *Log, index, cache* : activate `Force to store all files in cache`

To learn how to use it, I strongly recommand to have a look on the website : https://www.httrack.com/html/index.html

## Extra tools
Some interesting tools to perform OSINT and radio exploration has been added :
- <a href="https://github.com/TheYahya/sherlock">Sherlock </a> => A command-line tool that is used to scan many social network (like Facebook, Twitter, Tinder...) to find a user's account. All requests can be made over TOR.
- <a href="https://github.com/csete/gqrx">GQRX </a> => A software-defined radio that allow you to demodulate AM, FM and SSB and is compatible with many hardware (RTL-SDR, HackRF, BladeFR...).
- <a href="https://github.com/twintproject/twint">Twint </a> => This advanced Twitter OSINT tool allow you to scrap a user's Tweet, followers... without any API required.
- <a href="https://github.com/s0md3v/Photon">Photon </a> => A command-line tool that allow you to extract data of a website (subdomain, picture, email adress...).
- <a href="https://github.com/ggerganov/kbd-audio">Keytap </a> => Theses experimental tools can be used for analyzing mechanical keyboard input with microphone capture in order to predict the content of a written text.
- <a href="https://github.com/exiftool/exiftool">Exiftool </a> => A command-line tool that is used to analyze, modify and erase metadata in a wide variety of file (supported format include JPEG, PNG, DOC, MP4...).

## Enhanced security browser
Due to incompatibility of Tor Browser with Raspberry's architecture (ARM), a possible alternative has been to install Mozilla Firefox (ERS) and drastically renforced its security. The following open-source add-on has been added : <a href="https://addons.mozilla.org/fr/firefox/addon/ublock-origin/">uBlock Origin</a>, <a href="https://www.eff.org/privacybadger">Privacy Badger</a>, <a href="https://www.eff.org/https-everywhere">HTTPS Everywhere</a>, <a href="https://addons.mozilla.org/fr/firefox/addon/cookie-autodelete/">Cookie Autodelete</a>, <a href="https://decentraleyes.org/">Decentralised</a> and <a href="https://addons.mozilla.org/fr/firefox/addon/noscript/">Noscript</a>.

# Hardware
Here is a example of the hardware that I've used. Feel free to choose them according to your specific needs (dimension, more powerfull equipment...):

| **Raspberry Pi 3B+** | **64GB SD Card** | **Wired keyboard** |
| :---: | :---: | :---: |
| **External Hard Drive** | **Portable screen** | **RFID RC 522** |
| **RTL-SDR** | **USB/Jack cable** | **Wireless module** |
| **Powered USB hub** | **Fans** | **Battery** |

**Cost estimated :** around 500 $

But the most important piece is probably the briefcase itself :) Depending on the style/quality/size that you want, it will impact how you'll have to build it and the dimension of the components that you choose).

# Further improvements
- [ ] More powerfull computer (Raspberry Pi alternative ?)
- [ ] Better range for WIFI and radio
- [ ] Full-disk encryption

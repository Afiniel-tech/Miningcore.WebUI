## Miningcore WebUI

[Miningcore](https://github.com/oliverw/miningcore) is a high-performance Mining Pool Software for Linux and Windows
A public production pool requires a web-frontend for your users to check their hashrate, earnings etc. Miningcore does not include such frontend but there are several community projects that can be used as starting point like
Miningcore.WebUI. It's open source. so you can change it as you want. 

## How to install & Configure
First you clone the Miningcore WebUI to your webserver
```
git clone https://github.com/Afiniel-tech/Miningcore.WebUI.git
```
When you have clone the Miningcore WebUI to your webserver:
```
sudo nano Miningcore.WebUI/js/miningcore.js
``` 
Go to line: 

you should now see the site and live pool info.

  
## Website is visible, but no live data is shown.

Live info data is retrieved from the miningcore pool API.
The WebUI website default looks at the domain-name/api.
If this is not you api location, you need to edit the miningcore.js file.</br>

Chang API location</br>
- open the WebUI config file in you editor: js/miningcore.js
- change the following:

var WebURL         = window.location.protocol + "//" + window.location.hostname + "/";</br>
var API            = WebURL + "api/";</br>
var stratumAddress = "stratum+tcp://" + window.location.hostname + ":";</br>


it should be like this:</br>
(replace domain-name.com is you own domain name)</br>
var WebURL = "https://domain-name.com/";</br>
var API = "https://domain-name.com/api/";</br>
var stratumAddress = "stratum+tcp://domain-name.com:";</br>



<b>Live Miningcore.WebUI</b></br>
My pool website can be found at https://miningcore.eu


<b>Suggestion</b></br>
Do you have any idea what to add more to the website, or you found a bug
let me know and we will see what we can do.


<b>Roadmap:</b></br>
- add multiple single miningcore pool servers in one website
- add more color skins out off the box
- add last time block found (sec / min / hours)
- add blockchain height (number)
- add current round variance  (in %)
- add pool fee (in %)
- add block maturity (number blocks)
- add payment frequency  (hours)
- add payment threshold


## Changes:
version 1.1 (30 may 2022)
- Changes and clean up on miningcore.js
- Rewrite README.md
- Small changes to pool config page
- Change to index.html
#
Version 1.0  (1 jul 2019)
- simple and fast WebUI (html and javascript)
- one file website displays selected info block and hides the rest
- one modern colorfull look 



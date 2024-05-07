Miningcore.WebUI
Miningcore WebUI for the Coinfoundry Miningcore Pool
Miningcore is one of the best open source minning pools there are. To make this pool look good, you have to have a nice and fast user interface. Miningcore.WebUI does that for you and it open source. so you can change it as you want.

How to install & Configure This Miningcore WebUI need a working Miningcore Pool API

Download the Miningcore.WebUI files
Save them on your webserver and point your webserver config to the index.html
You should now see the site and live pool API info

Website is visible, but no live data is shown
Live info data is retrieved from the miningcore pool API.
The WebUI website default looks at the domain-name/api.
If this is not you api location, you need to edit the miningcore.js file.

Chang API location

open the WebUI config file in you editor: js/miningcore.js
change the following:
var WebURL = window.location.protocol + "//" + window.location.hostname + "/";
var API = WebURL + "api/";
var stratumAddress = "stratum+tcp://" + window.location.hostname + ":";

it should be like this:
(replace domain-name.com is you own domain name)
var WebURL = "https://domain-name.com/";
var API = "https://domain-name.com/api/";
var stratumAddress = "stratum+tcp://domain-name.com:";

Live Miningcore.WebUI
My pool website can be found at https://miningcore.eu

Suggestion
Do you have any idea what to add more to the website, or you found a bug let me know and we will see what we can do.

Roadmap:

add multiple single miningcore pool servers in one website
add more color skins out off the box
add last time block found (sec / min / hours)
add blockchain height (number)
add current round variance (in %)
add pool fee (in %)
add block maturity (number blocks)
add payment frequency (hours)
add payment threshold
Changes:
Version 1.0 (1 jul 2019)

simple and fast WebUI (html and javascript)
one file website displays selected info block and hides the rest
one modern colorfull look

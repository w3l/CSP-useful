# CSP, WTF?

Sometimes, CSP notifications are __really difficult to understand or very strange__. Here is a collection of some CSP WTF.
If you have an idea (even if the idea is WTF) for some of these, do not hesitate to participate :)

---------------------------------------
# function injectPageScriptAPI

```
{
    "csp-report": {
        "blocked-uri": "self",
        "document-uri": "[anonymised]",
        "line-number": 1,
        "original-policy": "default-src http://[anonymised]; script-src http://[anonymised] https://www.google-analytics.com http://www.google-analytics.com http://stats.g.doubleclick.net https://stats.g.doubleclick.net; style-src http://[anonymised] data:; img-src http://[anonymised] https://www.google-analytics.com http://www.google-analytics.com http://*.[anonymised] http://stats.g.doubleclick.net https://stats.g.doubleclick.net data:; child-src http://[anonymised]; report-uri http://[anonymised]/csp-parser.php",
        "referrer": "https://www.google.be/",
        "script-sample": "try {\r\n(function injectPageScriptAPI(scr...",
        "source-file": "[anonymised]",
        "violated-directive": "script-src http://[anonymised] https://www.google-analytics.com http://www.google-analytics.com http://stats.g.doubleclick.net https://stats.g.doubleclick.net"
    }
}
```
 ?
__WTF:__ nothing like this on the website.

__Answer:__ might be related to Adguard browser extension ? https://github.com/AdguardTeam/AdguardBrowserExtension/pull/694

---------------------------------------
# Skype web


```

{
    "csp-report": {
        "blocked-uri": "self",
        "document-uri": "https://www.estcequonmetenprodaujourdhui.info/",
        "line-number": 1,
        "original-policy": "default-src 'none'; script-src https://www.estcequonmetenprodaujourdhui.info; style-src https://www.estcequonmetenprodaujourdhui.info 'nonce-6e06851a1ca7ed29068ff9594b4b973f43b8841f724613df1c95136c3a59eeec71de4ceeac729c5280f688c6b808878c0c77c1dce5acc9b2ba927ca0fc4c2298'; img-src https://www.estcequonmetenprodaujourdhui.info data:; font-src https://www.estcequonmetenprodaujourdhui.info; child-src https://www.estcequonmetenprodaujourdhui.info; frame-ancestors 'none'; manifest-src https://www.estcequonmetenprodaujourdhui.info; report-uri https://www.estcequonmetenprodaujourdhui.info/csp-parser.php",
        "referrer": "https://web.skype.com/fr/",
        "script-sample": "[href^=\"https://plus.google.com/share?ur...",
        "source-file": "https://www.estcequonmetenprodaujourdhui.info/",
        "violated-directive": "style-src https://www.estcequonmetenprodaujourdhui.info 'nonce-6e06851a1ca7ed29068ff9594b4b973f43b8841f724613df1c95136c3a59eeec71de4ceeac729c5280f688c6b808878c0c77c1dce5acc9b2ba927ca0fc4c2298'"
    }
}
```
and 
```
{
    "csp-report": {
        "blocked-uri": "self",
        "document-uri": "https://www.estcequonmetenprodaujourdhui.info/",
        "line-number": 1,
        "original-policy": "default-src 'none'; script-src https://www.estcequonmetenprodaujourdhui.info; style-src https://www.estcequonmetenprodaujourdhui.info 'nonce-6e06851a1ca7ed29068ff9594b4b973f43b8841f724613df1c95136c3a59eeec71de4ceeac729c5280f688c6b808878c0c77c1dce5acc9b2ba927ca0fc4c2298'; img-src https://www.estcequonmetenprodaujourdhui.info data:; font-src https://www.estcequonmetenprodaujourdhui.info; child-src https://www.estcequonmetenprodaujourdhui.info; frame-ancestors 'none'; manifest-src https://www.estcequonmetenprodaujourdhui.info; report-uri https://www.estcequonmetenprodaujourdhui.info/csp-parser.php",
        "referrer": "https://web.skype.com/fr/",
        "script-sample": "ADS-RIGHT,\nAFS-AD,\n[ad-id^=\"googlead\"],\n...",

        "source-file": "https://www.estcequonmetenprodaujourdhui.info/",
        "violated-directive": "style-src https://www.estcequonmetenprodaujourdhui.info 'nonce-6e06851a1ca7ed29068ff9594b4b973f43b8841f724613df1c95136c3a59eeec71de4ceeac729c5280f688c6b808878c0c77c1dce5acc9b2ba927ca0fc4c2298'"
    }
}
```

__WTF:__ nothing like this on the website.

__Answer:__ related to Skype, didn't find how to reproduce.

---------------------------------------
# Google tag manager


```
{
    "csp-report": {
        "document-uri": "https://www.nicolas-hoffmann.net/source/cv-anciennes-experiences.php",
        "referrer": "https://www.google.fr/",
        "violated-directive": "script-src",
        "effective-directive": "script-src",
        "original-policy": "default-src 'none';  script-src 'self' google-analytics.com stats.g.doubleclick.net https://stats.g.doubleclick.net; style-src 'self' data:  ; img-src 'self' google-analytics.com stats.g.doubleclick.net https://stats.g.doubleclick.net ssl.google-analytics.com data: ;  connect-src 'self';  font-src 'self'; media-src 'self'; object-src 'self' www.youtube.com ;  child-src 'self' ;  frame-ancestors 'self' ; manifest-src 'self' ; form-action 'self' ; report-uri /csp-parser.php ;",
        "disposition": "enforce",
        "blocked-uri": "https://www.googletagmanager.com/gtm.js?id=GTM-TMLW42T",
        "line-number": 2,
        "column-number": 299,
        "status-code": 0,
        "script-sample": ""
    }
}
```

__WTF:__ nothing like this on the website.

__Answer:__ related to Google tag manager (extension, other ?)

---------------------------------------
# Google Search for Android


```
{
    "csp-report": {
        "document-uri": "[anonymised]",
        "referrer": "android-app://com.google.android.googlequicksearchbox",
        "violated-directive": "img-src",
        "effective-directive": "img-src",
        "original-policy": "default-src 'self';  script-src 'self' https://www.google-analytics.com http://www.google-analytics.com  stats.g.doubleclick.net https://stats.g.doubleclick.net ; style-src 'self' data: ; img-src 'self' https://www.google-analytics.com http://www.google-analytics.com *.[anonymised] stats.g.doubleclick.net https://stats.g.doubleclick.net data: ;  child-src 'self' ; report-uri /csp-parser.php ;",
        "disposition": "enforce",
        "blocked-uri": "http://1.1.1.1/bmi/[anonymised]/layout/images/swiss-label.png",
        "status-code": 200
    }
}
```

__WTF:__ nothing like this on the website.

__Answer:__ related to google search app on android.

---------------------------------------
# Adguard Ad Blocking Filters


```
{
    "csp-report": {
        "blocked-uri": "self",
        "document-uri": "https://www.nicolas-hoffmann.net/source/",
        "line-number": 1,
        "original-policy": "default-src 'none'; script-src https://www.nicolas-hoffmann.net https://google-analytics.com https://stats.g.doubleclick.net https://stats.g.doubleclick.net; style-src https://www.nicolas-hoffmann.net data:; img-src https://www.nicolas-hoffmann.net https://google-analytics.com https://stats.g.doubleclick.net https://stats.g.doubleclick.net https://ssl.google-analytics.com data:; connect-src https://www.nicolas-hoffmann.net; font-src https://www.nicolas-hoffmann.net; media-src https://www.nicolas-hoffmann.net; object-src https://www.nicolas-hoffmann.net https://www.youtube.com; child-src https://www.nicolas-hoffmann.net; frame-ancestors https://www.nicolas-hoffmann.net; manifest-src https://www.nicolas-hoffmann.net; form-action https://www.nicolas-hoffmann.net; report-uri https://www.nicolas-hoffmann.net/csp-parser.php",
        "referrer": "https://a11y.nicolas-hoffmann.net/",
        "script-sample": ".werbung, .text_werbung, .firstload, .We...",
        "source-file": "https://www.nicolas-hoffmann.net/source/",
        "violated-directive": "style-src https://www.nicolas-hoffmann.net data:"
    }
}
```

__WTF:__ nothing like this on the website.

__Answer:__ might be related to Adguard Ad Blocking Filters https://adguard.com/

---------------------------------------
# ng:cloak/ngInspect_clickedEl

```
{
    "csp-report": {
        "blocked-uri": "self",
        "document-uri": "https://www.estcequonmetenprodaujourdhui.info/",
        "line-number": 1,
        "original-policy": "default-src 'none'; script-src https://www.estcequonmetenprodaujourdhui.info; style-src https://www.estcequonmetenprodaujourdhui.info 'nonce-5a14701a62e1d1e782fea29568e4c1b34d9e13b579503eb9ab22849c754dc665eb10016ea1e7a767fd9463e0812f66c00f24b34c0878de0eef58f318b9b5a2df'; img-src https://www.estcequonmetenprodaujourdhui.info data:; font-src https://www.estcequonmetenprodaujourdhui.info; child-src https://www.estcequonmetenprodaujourdhui.info; frame-ancestors 'none'; manifest-src https://www.estcequonmetenprodaujourdhui.info; report-uri https://www.estcequonmetenprodaujourdhui.info/csp-parser.php",
        "referrer": "",
        "script-sample": "@charset \"UTF-8\";[ng\\:cloak],[ng-cloak],...",

        "source-file": "https://www.estcequonmetenprodaujourdhui.info/",
        "violated-directive": "style-src https://www.estcequonmetenprodaujourdhui.info 'nonce-5a14701a62e1d1e782fea29568e4c1b34d9e13b579503eb9ab22849c754dc665eb10016ea1e7a767fd9463e0812f66c00f24b34c0878de0eef58f318b9b5a2df'"
    }
}
```
or
```
{
    "csp-report": {
        "blocked-uri": "self",
        "document-uri": "https://www.estcequonmetenprodaujourdhui.info/",
        "line-number": 1,
        "original-policy": "default-src 'none'; script-src https://www.estcequonmetenprodaujourdhui.info; style-src https://www.estcequonmetenprodaujourdhui.info 'nonce-2905cfa57de27d0311c5a7926fff9ba90e2f29934fe3fe100691ae4688d46410819413d239d2338287978476be84634a7ade18863c03f8d64f20236c3dc07c5e'; img-src https://www.estcequonmetenprodaujourdhui.info data:; font-src https://www.estcequonmetenprodaujourdhui.info; child-src https://www.estcequonmetenprodaujourdhui.info; frame-ancestors 'none'; manifest-src https://www.estcequonmetenprodaujourdhui.info; report-uri https://www.estcequonmetenprodaujourdhui.info/csp-parser.php",
        "referrer": "",
        "script-sample": "window._ngInspect_clickedEl = null;docum...",
        "source-file": "https://www.estcequonmetenprodaujourdhui.info/",
        "violated-directive": "script-src https://www.estcequonmetenprodaujourdhui.info"
    }
}
```

__WTF:__ This is not on this website. :)

__Answer:__ related to angular directive https://docs.angularjs.org/api/ng/directive/ngCloak (however, don't know how it came to this website, maybe debug tool? Might be related to https://addons.mozilla.org/fr/firefox/addon/ng-inspect/)


---------------------------------------
# ahrefs.*


```
{
    "csp-report": {
        "blocked-uri": "self",
        "document-uri": "https://www.estcequonmetenprodaujourdhui.info/",
        "original-policy": "default-src https://ahrefs.com http://ahrefs.com https://*.ahrefs.me http://*.ahrefs.me https://ahrefs.com http://ahrefs.com https://*.ahrefs.me http://*.ahrefs.me; script-src https://ahrefs.com http://ahrefs.com https://*.ahrefs.me http://*.ahrefs.me https://ahrefs.com http://ahrefs.com https://*.ahrefs.me http://*.ahrefs.me https://www.estcequonmetenprodaujourdhui.info https://www.google-analytics.com https://stats.g.doubleclick.net https://stats.g.doubleclick.net; style-src https://www.estcequonmetenprodaujourdhui.info 'unsafe-inline'; img-src https://www.estcequonmetenprodaujourdhui.info https://www.google-analytics.com https://stats.g.doubleclick.net https://stats.g.doubleclick.net data:; font-src https://www.estcequonmetenprodaujourdhui.info; child-src https://www.estcequonmetenprodaujourdhui.info; frame-ancestors 'none'; manifest-src https://www.estcequonmetenprodaujourdhui.info; report-uri https://www.estcequonmetenprodaujourdhui.info/csp-!
 parser.php",
        "referrer": "",
        "script-sample": "onsubmit attribute on DIV element",

        "source-file": "https://www.estcequonmetenprodaujourdhui.info/",
        "violated-directive": "script-src https://ahrefs.com http://ahrefs.com https://*.ahrefs.me http://*.ahrefs.me https://ahrefs.com http://ahrefs.com https://*.ahrefs.me http://*.ahrefs.me https://www.estcequonmetenprodaujourdhui.info https://www.google-analytics.com https://stats.g.doubleclick.net https://stats.g.doubleclick.net"
    }
}
```

__WTF:__ ???

__Answer:__ related to https://ahrefs.com/ tool, however, I was not able to reproduce. 

---------------------------------------
# int.search.myway.com


```
{
    "csp-report": {
        "blocked-uri": "self",
        "document-uri": "https://www.nicolas-hoffmann.net/source/cascade_rouget.php",
        "line-number": 1,
        "original-policy": "default-src 'none'; script-src https://www.nicolas-hoffmann.net https://google-analytics.com https://stats.g.doubleclick.net https://stats.g.doubleclick.net; style-src https://www.nicolas-hoffmann.net data:; img-src https://www.nicolas-hoffmann.net https://google-analytics.com https://stats.g.doubleclick.net https://stats.g.doubleclick.net https://ssl.google-analytics.com data:; connect-src https://www.nicolas-hoffmann.net; font-src https://www.nicolas-hoffmann.net; media-src https://www.nicolas-hoffmann.net; object-src https://www.nicolas-hoffmann.net https://www.youtube.com; child-src https://www.nicolas-hoffmann.net; frame-ancestors https://www.nicolas-hoffmann.net; manifest-src https://www.nicolas-hoffmann.net; form-action https://www.nicolas-hoffmann.net; report-uri https://www.nicolas-hoffmann.net/csp-parser.php",
        "referrer": "http://int.search.myway.com/search/GGmain.jhtml?p2=%5EBYC%5Exdm024%5ELMFRFR%5Efr&ptb=97120439-8D7B-41CC-84DD-7E9B53B40901&n=78399c5d&ind=&cn=fr&ln=fr&si=&tpr=hpsb&trs=wtt&brwsid=1afe115d-7025-46e5-9a3d-42b6374704b5&searchfor=Photos%20de%20la%20cascade%20du%20rouget&st=tab",
        "script-sample": "//\r\n//alert('videodownload2 begin');\r\n;(...",
        "source-file": "https://www.nicolas-hoffmann.net/source/cascade_rouget.php",
        "violated-directive": "script-src https://www.nicolas-hoffmann.net https://google-analytics.com https://stats.g.doubleclick.net https://stats.g.doubleclick.net"
    }
}
```
or
```
{
    "csp-report": {
        "blocked-uri": "self",
        "document-uri": "https://www.nicolas-hoffmann.net/source/cascade_rouget.php",
        "line-number": 1,
        "original-policy": "default-src 'none'; script-src https://www.nicolas-hoffmann.net https://google-analytics.com https://stats.g.doubleclick.net https://stats.g.doubleclick.net; style-src https://www.nicolas-hoffmann.net data:; img-src https://www.nicolas-hoffmann.net https://google-analytics.com https://stats.g.doubleclick.net https://stats.g.doubleclick.net https://ssl.google-analytics.com data:; connect-src https://www.nicolas-hoffmann.net; font-src https://www.nicolas-hoffmann.net; media-src https://www.nicolas-hoffmann.net; object-src https://www.nicolas-hoffmann.net https://www.youtube.com; child-src https://www.nicolas-hoffmann.net; frame-ancestors https://www.nicolas-hoffmann.net; manifest-src https://www.nicolas-hoffmann.net; form-action https://www.nicolas-hoffmann.net; report-uri https://www.nicolas-hoffmann.net/csp-parser.php",
        "referrer": "http://int.search.myway.com/search/GGmain.jhtml?p2=%5EBYC%5Exdm024%5ELMFRFR%5Efr&ptb=97120439-8D7B-41CC-84DD-7E9B53B40901&n=78399c5d&ind=&cn=fr&ln=fr&si=&tpr=hpsb&trs=wtt&brwsid=1afe115d-7025-46e5-9a3d-42b6374704b5&searchfor=Photos%20de%20la%20cascade%20du%20rouget&st=tab",
        "script-sample": "/*!\r\n * jQuery JavaScript Library v1.4.2...",

        "source-file": "https://www.nicolas-hoffmann.net/source/cascade_rouget.php",
        "violated-directive": "script-src https://www.nicolas-hoffmann.net https://google-analytics.com https://stats.g.doubleclick.net https://stats.g.doubleclick.net"
    }
}
```
or
```
{
    "csp-report": {
        "blocked-uri": "self",
        "document-uri": "https://www.nicolas-hoffmann.net/source/cascade_rouget.php",
        "line-number": 1,
        "original-policy": "default-src 'none'; script-src https://www.nicolas-hoffmann.net https://google-analytics.com https://stats.g.doubleclick.net https://stats.g.doubleclick.net; style-src https://www.nicolas-hoffmann.net data:; img-src https://www.nicolas-hoffmann.net https://google-analytics.com https://stats.g.doubleclick.net https://stats.g.doubleclick.net https://ssl.google-analytics.com data:; connect-src https://www.nicolas-hoffmann.net; font-src https://www.nicolas-hoffmann.net; media-src https://www.nicolas-hoffmann.net; object-src https://www.nicolas-hoffmann.net https://www.youtube.com; child-src https://www.nicolas-hoffmann.net; frame-ancestors https://www.nicolas-hoffmann.net; manifest-src https://www.nicolas-hoffmann.net; form-action https://www.nicolas-hoffmann.net; report-uri https://www.nicolas-hoffmann.net/csp-parser.php",
        "referrer": "http://int.search.myway.com/search/GGmain.jhtml?p2=%5EBYC%5Exdm024%5ELMFRFR%5Efr&ptb=97120439-8D7B-41CC-84DD-7E9B53B40901&n=78399c5d&ind=&cn=fr&ln=fr&si=&tpr=hpsb&trs=wtt&brwsid=1afe115d-7025-46e5-9a3d-42b6374704b5&searchfor=Photos%20de%20la%20cascade%20du%20rouget&st=tab",
        "script-sample": ";(function($){\r\n\tvar Plugin = $.Wondersh...",

        "source-file": "https://www.nicolas-hoffmann.net/source/cascade_rouget.php",
        "violated-directive": "script-src https://www.nicolas-hoffmann.net https://google-analytics.com https://stats.g.doubleclick.net https://stats.g.doubleclick.net"
    }
}
```
or
```
{
    "csp-report": {
        "blocked-uri": "self",
        "document-uri": "https://www.nicolas-hoffmann.net/source/cascade_rouget.php",
        "line-number": 1,
        "original-policy": "default-src 'none'; script-src https://www.nicolas-hoffmann.net https://google-analytics.com https://stats.g.doubleclick.net https://stats.g.doubleclick.net; style-src https://www.nicolas-hoffmann.net data:; img-src https://www.nicolas-hoffmann.net https://google-analytics.com https://stats.g.doubleclick.net https://stats.g.doubleclick.net https://ssl.google-analytics.com data:; connect-src https://www.nicolas-hoffmann.net; font-src https://www.nicolas-hoffmann.net; media-src https://www.nicolas-hoffmann.net; object-src https://www.nicolas-hoffmann.net https://www.youtube.com; child-src https://www.nicolas-hoffmann.net; frame-ancestors https://www.nicolas-hoffmann.net; manifest-src https://www.nicolas-hoffmann.net; form-action https://www.nicolas-hoffmann.net; report-uri https://www.nicolas-hoffmann.net/csp-parser.php",
        "referrer": "http://int.search.myway.com/search/GGmain.jhtml?p2=%5EBYC%5Exdm024%5ELMFRFR%5Efr&ptb=97120439-8D7B-41CC-84DD-7E9B53B40901&n=78399c5d&ind=&cn=fr&ln=fr&si=&tpr=hpsb&trs=wtt&brwsid=1afe115d-7025-46e5-9a3d-42b6374704b5&searchfor=Photos%20de%20la%20cascade%20du%20rouget&st=tab",
        "script-sample": "//alert('jQuery.Wondershare_WSVCU_Plugin...",

        "source-file": "https://www.nicolas-hoffmann.net/source/cascade_rouget.php",
        "violated-directive": "script-src https://www.nicolas-hoffmann.net https://google-analytics.com https://stats.g.doubleclick.net https://stats.g.doubleclick.net"
    }
}
```
or
```
{
    "csp-report": {
        "blocked-uri": "self",
        "document-uri": "https://www.nicolas-hoffmann.net/source/cascade_rouget.php",
        "line-number": 1,
        "original-policy": "default-src 'none'; script-src https://www.nicolas-hoffmann.net https://google-analytics.com https://stats.g.doubleclick.net https://stats.g.doubleclick.net; style-src https://www.nicolas-hoffmann.net data:; img-src https://www.nicolas-hoffmann.net https://google-analytics.com https://stats.g.doubleclick.net https://stats.g.doubleclick.net https://ssl.google-analytics.com data:; connect-src https://www.nicolas-hoffmann.net; font-src https://www.nicolas-hoffmann.net; media-src https://www.nicolas-hoffmann.net; object-src https://www.nicolas-hoffmann.net https://www.youtube.com; child-src https://www.nicolas-hoffmann.net; frame-ancestors https://www.nicolas-hoffmann.net; manifest-src https://www.nicolas-hoffmann.net; form-action https://www.nicolas-hoffmann.net; report-uri https://www.nicolas-hoffmann.net/csp-parser.php",
        "referrer": "http://int.search.myway.com/search/GGmain.jhtml?p2=%5EBYC%5Exdm024%5ELMFRFR%5Efr&ptb=97120439-8D7B-41CC-84DD-7E9B53B40901&n=78399c5d&ind=&cn=fr&ln=fr&si=&tpr=hpsb&trs=wtt&brwsid=1afe115d-7025-46e5-9a3d-42b6374704b5&searchfor=Photos%20de%20la%20cascade%20du%20rouget&st=tab",
        "script-sample": "/*!\n * jquery.base64.js 0.1 - https://gi...",

        "source-file": "https://www.nicolas-hoffmann.net/source/cascade_rouget.php",
        "violated-directive": "script-src https://www.nicolas-hoffmann.net https://google-analytics.com https://stats.g.doubleclick.net https://stats.g.doubleclick.net"
    }
}
```
or
```
{
    "csp-report": {
        "blocked-uri": "self",
        "document-uri": "https://www.nicolas-hoffmann.net/source/cascade_rouget.php",
        "line-number": 1,
        "original-policy": "default-src 'none'; script-src https://www.nicolas-hoffmann.net https://google-analytics.com https://stats.g.doubleclick.net https://stats.g.doubleclick.net; style-src https://www.nicolas-hoffmann.net data:; img-src https://www.nicolas-hoffmann.net https://google-analytics.com https://stats.g.doubleclick.net https://stats.g.doubleclick.net https://ssl.google-analytics.com data:; connect-src https://www.nicolas-hoffmann.net; font-src https://www.nicolas-hoffmann.net; media-src https://www.nicolas-hoffmann.net; object-src https://www.nicolas-hoffmann.net https://www.youtube.com; child-src https://www.nicolas-hoffmann.net; frame-ancestors https://www.nicolas-hoffmann.net; manifest-src https://www.nicolas-hoffmann.net; form-action https://www.nicolas-hoffmann.net; report-uri https://www.nicolas-hoffmann.net/csp-parser.php",
        "referrer": "http://int.search.myway.com/search/GGmain.jhtml?p2=%5EBYC%5Exdm024%5ELMFRFR%5Efr&ptb=97120439-8D7B-41CC-84DD-7E9B53B40901&n=78399c5d&ind=&cn=fr&ln=fr&si=&tpr=hpsb&trs=wtt&brwsid=1afe115d-7025-46e5-9a3d-42b6374704b5&searchfor=Photos%20de%20la%20cascade%20du%20rouget&st=tab",
        "script-sample": "//WS\u00e8\u00a7\u0086\u00e9\u00a2\u0091\u00e4\u00b8\u008b\u00e8\u00bd\u00bd\u00e6\u008f\u0092\u00e4\u00bb\u00b6\u00e8\u00be\u0085\u00e5\u008a\u00a9\u00e5\u00ae\u009e\u00e7\u008e\u00b0\u00e5\u008d\u0095\u00e5\u0085\u0083...",
        "source-file": "https://www.nicolas-hoffmann.net/source/cascade_rouget.php",
        "violated-directive": "script-src https://www.nicolas-hoffmann.net https://google-analytics.com https://stats.g.doubleclick.net https://stats.g.doubleclick.net"
    }
}
```
or
```
{
    "csp-report": {
        "blocked-uri": "self",
        "document-uri": "https://www.nicolas-hoffmann.net/source/cascade_rouget.php",
        "line-number": 1,
        "original-policy": "default-src 'none'; script-src https://www.nicolas-hoffmann.net https://google-analytics.com https://stats.g.doubleclick.net https://stats.g.doubleclick.net; style-src https://www.nicolas-hoffmann.net data:; img-src https://www.nicolas-hoffmann.net https://google-analytics.com https://stats.g.doubleclick.net https://stats.g.doubleclick.net https://ssl.google-analytics.com data:; connect-src https://www.nicolas-hoffmann.net; font-src https://www.nicolas-hoffmann.net; media-src https://www.nicolas-hoffmann.net; object-src https://www.nicolas-hoffmann.net https://www.youtube.com; child-src https://www.nicolas-hoffmann.net; frame-ancestors https://www.nicolas-hoffmann.net; manifest-src https://www.nicolas-hoffmann.net; form-action https://www.nicolas-hoffmann.net; report-uri https://www.nicolas-hoffmann.net/csp-parser.php",
        "referrer": "http://int.search.myway.com/search/GGmain.jhtml?p2=%5EBYC%5Exdm024%5ELMFRFR%5Efr&ptb=97120439-8D7B-41CC-84DD-7E9B53B40901&n=78399c5d&ind=&cn=fr&ln=fr&si=&tpr=hpsb&trs=wtt&brwsid=1afe115d-7025-46e5-9a3d-42b6374704b5&searchfor=Photos%20de%20la%20cascade%20du%20rouget&st=tab",
        "script-sample": "\r\n;(function($){\r\n\tjq_relocation = $.rel...",

        "source-file": "https://www.nicolas-hoffmann.net/source/cascade_rouget.php",
        "violated-directive": "script-src https://www.nicolas-hoffmann.net https://google-analytics.com https://stats.g.doubleclick.net https://stats.g.doubleclick.net"
    }
}
```
Etc.



__WTF:__ ???

__Answer:__ all related to int.search.myway.com, however, I was not able to reproduce.

---------------------------------------
# connectionstrenth.com

```
{
    "csp-report": {
        "document-uri": "https://www.nicolas-hoffmann.net/source/cv-developpeur-web-integrateur-xhtml-css.php",
        "referrer": "https://www.google.com/",
        "violated-directive": "script-src",
        "effective-directive": "script-src",
        "original-policy": "default-src 'none';  script-src 'self' google-analytics.com stats.g.doubleclick.net https://stats.g.doubleclick.net; style-src 'self' data:  ; img-src 'self' google-analytics.com stats.g.doubleclick.net https://stats.g.doubleclick.net ssl.google-analytics.com data: ;  connect-src 'self';  font-src 'self'; media-src 'self'; object-src 'self' www.youtube.com ;  child-src 'self' ;  frame-ancestors 'self' ; manifest-src 'self' ; form-action 'self' ; report-uri /csp-parser.php ;",
        "disposition": "enforce",
        "blocked-uri": "https://connectionstrenth.com/optout/get?jsonp=__twb_cb_56941106&key=da2e092ff7bc4ea89e&t=1496394531140",
        "line-number": 1,
        "column-number": 5387,

        "source-file": "https://s3.amazonaws.com/cashe-js/da2e092ff7bc4ea89e.js",
        "status-code": 0
    }
}
```
or 
```
{
    "csp-report": {
        "document-uri": "https://www.nicolas-hoffmann.net/source/cv-developpeur-web-integrateur-xhtml-css.php",
        "referrer": "https://www.google.com/",
        "violated-directive": "img-src",
        "effective-directive": "img-src",
        "original-policy": "default-src 'none';  script-src 'self' google-analytics.com stats.g.doubleclick.net https://stats.g.doubleclick.net; style-src 'self' data:  ; img-src 'self' google-analytics.com stats.g.doubleclick.net https://stats.g.doubleclick.net ssl.google-analytics.com data: ;  connect-src 'self';  font-src 'self'; media-src 'self'; object-src 'self' www.youtube.com ;  child-src 'self' ;  frame-ancestors 'self' ; manifest-src 'self' ; form-action 'self' ; report-uri /csp-parser.php ;",
        "disposition": "enforce",
        "blocked-uri": "https://connectionstrenth.com/metric/?mid=&wid=51067&sid=&tid=3490&rid=LAUNCHED&t=1496394531110",
        "status-code": 0
    }
}
```

__WTF:__ nothing like this on the website.

__Answer:__ appears to be related to ad server used by some Chrome extensions: https://www.reddit.com/r/technology/comments/4lltgu/psa_imgur_uploader_is_injecting_ads_on_google_and/

---------------------------------------
# Google Analytics Opt-out Add-on

```
{
    "csp-report": {
        "blocked-uri": "self",
        "document-uri": "https://www.nicolas-hoffmann.net/source/",
        "line-number": 1,
        "original-policy": "default-src 'none'; script-src https://www.nicolas-hoffmann.net https://google-analytics.com https://stats.g.doubleclick.net https://stats.g.doubleclick.net; style-src https://www.nicolas-hoffmann.net data:; img-src https://www.nicolas-hoffmann.net https://google-analytics.com https://stats.g.doubleclick.net https://stats.g.doubleclick.net https://ssl.google-analytics.com data:; connect-src https://www.nicolas-hoffmann.net; font-src https://www.nicolas-hoffmann.net; media-src https://www.nicolas-hoffmann.net; object-src https://www.nicolas-hoffmann.net https://www.youtube.com; child-src https://www.nicolas-hoffmann.net; frame-ancestors https://www.nicolas-hoffmann.net; manifest-src https://www.nicolas-hoffmann.net; form-action https://www.nicolas-hoffmann.net; report-uri https://www.nicolas-hoffmann.net/csp-parser.php",
        "referrer": "https://www.youtube.com/",
        "script-sample": "window[\"_gaUserPrefs\"] = { ioo : functio...",
        "source-file": "https://www.nicolas-hoffmann.net/source/",
        "violated-directive": "script-src https://www.nicolas-hoffmann.net https://google-analytics.com https://stats.g.doubleclick.net https://stats.g.doubleclick.net"
    }
}
```

__WTF:__ nothing like this on the website.

__Answer:__ might be related to Google Analytics Opt-out Add-on: https://github.com/sj26/mailcatcher/issues/205

---------------------------------------
# feedly.com

```

{
    "csp-report": {
        "blocked-uri": "self",
        "document-uri": "https://www.nicolas-hoffmann.net/source/1704-Je-hacke-le-retour-d-experience-via-un-phrase-veloute-Sud-Web.html",
        "original-policy": "default-src 'none'; script-src https://www.nicolas-hoffmann.net https://google-analytics.com https://stats.g.doubleclick.net https://stats.g.doubleclick.net; style-src https://www.nicolas-hoffmann.net data:; img-src https://www.nicolas-hoffmann.net https://google-analytics.com https://stats.g.doubleclick.net https://stats.g.doubleclick.net https://ssl.google-analytics.com data:; connect-src https://www.nicolas-hoffmann.net; font-src https://www.nicolas-hoffmann.net; media-src https://www.nicolas-hoffmann.net; object-src https://www.nicolas-hoffmann.net https://www.youtube.com; child-src https://www.nicolas-hoffmann.net; frame-ancestors https://www.nicolas-hoffmann.net; manifest-src https://www.nicolas-hoffmann.net; form-action https://www.nicolas-hoffmann.net; report-uri https://www.nicolas-hoffmann.net/csp-parser.php",
        "referrer": "https://feedly.com/i/category/Webdesign",
        "script-sample": "call to eval() or related function blocked by CSP",
        "violated-directive": "script-src https://www.nicolas-hoffmann.net https://google-analytics.com https://stats.g.doubleclick.net https://stats.g.doubleclick.net"
    }
}
```

__WTF:__ nothing like this on the website.

__Answer:__ Probably caused by RSS-reader like feedly.

---------------------------------------
# audiocdn.lingualeo.com


```
{
    "csp-report": {
        "document-uri": "https://van11y.net/accessible-tab-panel/",
        "referrer": "https://habrahabr.ru/company/zfort/blog/328636/",
        "violated-directive": "media-src",
        "effective-directive": "media-src",
        "original-policy": "default-src 'none' ;  script-src 'self'; style-src 'self' ; img-src 'self'; font-src 'self';  connect-src 'self'; child-src 'self' ; frame-ancestors 'none' ; manifest-src 'self' ; report-uri /csp-parser.php ;",
        "disposition": "enforce",
        "blocked-uri": "https://audiocdn.lingualeo.com/v2/1/1771-631152008.mp3",
        "status-code": 0
    }
}
```

__WTF:__ nothing like this on the website (not in sources, neither in scripts). (a mp3 that says ARIA!)

__Answer:__ seems like http://lingualeo.com/ is a tool to learn languages.

---------------------------------------
# yellowads.men


```
{
    "csp-report": {
        "document-uri": "https://www.nicolas-hoffmann.net/source/cv-developpeur-web-integrateur-xhtml-css.php",
        "referrer": "https://www.google.com/",
        "violated-directive": "script-src",
        "effective-directive": "script-src",
        "original-policy": "default-src 'none';  script-src 'self' google-analytics.com stats.g.doubleclick.net https://stats.g.doubleclick.net; style-src 'self' data:  ; img-src 'self' google-analytics.com stats.g.doubleclick.net https://stats.g.doubleclick.net ssl.google-analytics.com data: ;  connect-src 'self';  font-src 'self'; media-src 'self'; object-src 'self' www.youtube.com ;  child-src 'self' ;  frame-ancestors 'self' ; manifest-src 'self' ; form-action 'self' ; report-uri /csp-parser.php ;",
        "disposition": "enforce",
        "blocked-uri": "https://yellowads.men/code/pid/812933_BNX.js?rev=479",
        "line-number": 1,
        "column-number": 894,
        "source-file": "https://yellowads.men/code/?pid=812933&r=8076680",
        "status-code": 0
    }
}
```

__WTF:__ nothing like this on the website.

__Answer:__ probably malware on client side (see https://www.supprimervirus.net/supprimer-b-yellowads-men/ in french)

---------------------------------------
# volcanicpixels.com


```
{
    "csp-report": {
        "document-uri": "https://www.estcequonmetenprodaujourdhui.info/",
        "referrer": "",
        "violated-directive": "font-src",
        "effective-directive": "font-src",
        "original-policy": "default-src 'none';  script-src 'self' ; style-src 'self' 'nonce-18be64c7f0c944fcb4616aaa4bedf3b3b68f137d288bdbe5431f83db2659ccc084dfb1772f70aeeb6990db7c731d7052ea3fa87ad1853cf47f6a92c96478266f' ; img-src 'self'  data: ;  font-src 'self'; child-src 'self' ;  frame-ancestors 'none' ; manifest-src 'self' ; report-uri /csp-parser.php ;",
        "disposition": "enforce",
        "blocked-uri": "https://commondatastorage.googleapis.com/assets.volcanicpixels.com/webfonts/blokk/BLOKKRegular.woff",
        "status-code": 0
    }
}
```

__WTF:__ nothing like this on the website.

__Answer:__ probably related to https://www.volcanicpixels.com/

---------------------------------------
# jsl.infostatsvc.com


```
{
    "csp-report": {
        "document-uri": "https://www.nicolas-hoffmann.net/source/1302-Balise-video-de-HTML5-comment-l-inserer.html",
        "referrer": "https://www.google.tn/",
        "violated-directive": "img-src",
        "effective-directive": "img-src",
        "original-policy": "default-src 'none';  script-src 'self' google-analytics.com stats.g.doubleclick.net https://stats.g.doubleclick.net; style-src 'self' data:  ; img-src 'self' google-analytics.com stats.g.doubleclick.net https://stats.g.doubleclick.net ssl.google-analytics.com data: ;  connect-src 'self';  font-src 'self'; media-src 'self'; object-src 'self' www.youtube.com ;  child-src 'self' ;  frame-ancestors 'self' ; manifest-src 'self' ; form-action 'self' ; report-uri /csp-parser.php ;",
        "disposition": "enforce",
        "blocked-uri": "https://jsl.infostatsvc.com/?InitException_3=1163|,|EvalError%3A%20Refused%20to%20evaluate%20a%20string%20as%20JavaScript%20because%20%27unsafe-eval%27%20is%20not%20an%20allowed%20source%20of%20script%20in%20the%20following%20Content%20Security%20Policy%20directive%3A%20%22script-src%20%27self%27%20google-analytics.com%20stats.g.doubleclick.net%20https%3A%2F%2Fstats.g.doubleclick.net%22.%0A|,|7b4157d9-ecfb-4481-8e94-9f8f55a3e7f3|,|0|,|1000R|,|Chrome|,|Browser",
        "status-code": 0
    }
}

```

__WTF:__ nothing like this on the website.

__Answer:__ it seems to be an adware on client side: https://malwaretips.com/blogs/remove-jsl-infostatsvc-com-virus/

---------------------------------------
# GeckoScriptBridge.js

```
{
    "csp-report": {
        "blocked-uri": "self",
        "document-uri": "https://www.estcequonmetenprodaujourdhui.info/",
        "line-number": 48,
        "original-policy": "default-src 'none'; script-src https://www.estcequonmetenprodaujourdhui.info; style-src https://www.estcequonmetenprodaujourdhui.info 'nonce-dd3204dc997ae03878f3be16ed08edd4b56f28feb5f91d78c828174b83475f5d0c89f80e537f9e71dc805a5cecbfe9c54189040bc027e10120fa81630fbb2094'; img-src https://www.estcequonmetenprodaujourdhui.info data:; font-src https://www.estcequonmetenprodaujourdhui.info; child-src https://www.estcequonmetenprodaujourdhui.info; frame-ancestors 'none'; manifest-src https://www.estcequonmetenprodaujourdhui.info; report-uri https://www.estcequonmetenprodaujourdhui.info/csp-parser.php",
        "referrer": "",
        "script-sample": "call to eval() or related function blocked by CSP",
        "source-file": "jar:file:///C:/Program%20Files%20(x86)/ZennoLab/RU/ZennoPoster%20Pro/5.10.7.0/Progs/XulFx.xpi!/components/GeckoScriptBridge.js",
        "violated-directive": "script-src https://www.estcequonmetenprodaujourdhui.info"
    }
}
```

__WTF:__ nothing like this on the website.

__Answer:__ probably an extension on Firefox (related to http://zennolab.com/en/products/zennoposter/ ?).


---------------------------------------
# password toggler

```
{
    "csp-report": {
        "blocked-uri": "self",
        "document-uri": "https://rocssti.net/en/builder-css",
        "line-number": 1,
        "original-policy": "default-src 'none'; script-src https://rocssti.net https://www.google-analytics.com https://stats.g.doubleclick.net https://stats.g.doubleclick.net; style-src https://rocssti.net; img-src https://rocssti.net https://www.google-analytics.com https://stats.g.doubleclick.net https://stats.g.doubleclick.net data:; font-src https://rocssti.net; connect-src https://rocssti.net; child-src https://rocssti.net; frame-ancestors 'none'; manifest-src https://rocssti.net; form-action https://rocssti.net; report-uri https://rocssti.net/csp-parser.php",
        "referrer": "https://github.com/nico3333fr/ROCSSTI",
        "script-sample": ".password-toggler-button-parent {positio...",
        "source-file": "https://rocssti.net/en/builder-css",
        "violated-directive": "style-src https://rocssti.net"
    }
}
```

__WTF:__ nothing like this on the website.

__Answer:__ might be related to this extension: https://github.com/pckltr/password-toggler 

---------------------------------------
# zscaler.net

```
{
    "csp-report": {
        "blocked-uri": "self",
        "document-uri": "https://www.estcequonmetenprodaujourdhui.info/",
        "line-number": 33,
        "original-policy": "default-src 'none'; script-src https://*.zscaler.net https://www.estcequonmetenprodaujourdhui.info; style-src https://*.zscaler.net https://www.estcequonmetenprodaujourdhui.info 'nonce-4515373d1f1bbf1fb067e0413eb950978109202566edfe05826f0654dfb581b133a5b9e824faad5d2a46ffe5c3068cdfe576568f48e3ae604a9c1ce597ccb59a'; img-src https://*.zscaler.net https://www.estcequonmetenprodaujourdhui.info data:; font-src https://*.zscaler.net https://www.estcequonmetenprodaujourdhui.info; frame-ancestors 'none'; report-uri https://www.estcequonmetenprodaujourdhui.info/csp-parser.php",
        "referrer": "https://www.google.fr/search?q=est-ce+qu%27on+met+en+prod+aujourd%27hui&ie=utf-8&oe=utf-8&safe=active&gws_rd=cr&ei=dpPwWKS5NoObU-yrvrAJ",
        "script-sample": "\n\nbody {\n  background: #fff;\n  color: #0...",
        "source-file": "https://www.estcequonmetenprodaujourdhui.info/",
        "violated-directive": "style-src https://*.zscaler.net https://www.estcequonmetenprodaujourdhui.info 'nonce-4515373d1f1bbf1fb067e0413eb950978109202566edfe05826f0654dfb581b133a5b9e824faad5d2a46ffe5c3068cdfe576568f48e3ae604a9c1ce597ccb59a'"
    }
}
```
or 
```
{
    "csp-report": {
        "blocked-uri": "self",
        "document-uri": "https://www.estcequonmetenprodaujourdhui.info/",
        "line-number": 33,
        "original-policy": "default-src 'none'; script-src https://www.estcequonmetenprodaujourdhui.info; style-src https://www.estcequonmetenprodaujourdhui.info 'nonce-34341fafadab0a7272c62cddbde2fc8eaca52160cdf3977ae2775ec4e460d5416d5e1104371cb1f5633c7e2615bd8d778949e6cc704751f3e88241d243a4c9e8'; img-src https://www.estcequonmetenprodaujourdhui.info data:; font-src https://www.estcequonmetenprodaujourdhui.info; frame-ancestors 'none'; report-uri https://www.estcequonmetenprodaujourdhui.info/csp-parser.php",
        "referrer": "https://login.zscalertwo.net/sfc_upq?origurl=https%3A%2F%2Fwww%2eestcequonmetenprodaujourdhui%2einfo%2f&_ordtok=RN43WVqnbHJrHTVMqVqkWnSDpR&smup_ca=ifVFH1s2wK3jKL7Q&smup_ci=4b2WWVhRN3F2s&smupcat=akpEMmY3bjU1RkZnTg",
        "script-sample": "\n\nbody {\n  background: #fff;\n  color: #0...",
        "source-file": "https://www.estcequonmetenprodaujourdhui.info/",
        "violated-directive": "style-src https://www.estcequonmetenprodaujourdhui.info 'nonce-34341fafadab0a7272c62cddbde2fc8eaca52160cdf3977ae2775ec4e460d5416d5e1104371cb1f5633c7e2615bd8d778949e6cc704751f3e88241d243a4c9e8'"
    }
}
```

__WTF:__ nothing like this on the website (no zscaler.net in this website CSP policy).

__Answer:__ zscaler is a cloud web security solution, any idea how it changes CSP settings for a website?

---------------------------------------
# comic-sans-replacer

```
{
    "csp-report": {
        "document-uri": "https://www.estcequonmetenprodaujourdhui.info/",
        "referrer": "",
        "violated-directive": "font-src",
        "effective-directive": "font-src",
        "original-policy": "default-src 'none';  script-src 'self' ; style-src 'self' 'nonce-76972fbfb86f1f6b41a0174d3c05b814d0d47e4aaa20d33b1da9e93d66bb8183fd39cc383d7d6bfc382dc3d08cd42eb78337aaec644abd4892e7cd1afa73830d' ; img-src 'self'  data: ;  font-src 'self'; child-src 'self' ;  frame-ancestors 'none' ; manifest-src 'self' ; report-uri /csp-parser.php ;",
        "disposition": "enforce",
        "blocked-uri": "https://cdn.jsdelivr.net/comic-sans-replacer/1.1/fonts/ComicNeue-Regular.ttf",
        "status-code": 0
    }
}
```

__WTF:__ nothing like this on the website.

__Answer:__ might be related to this extension: https://github.com/niutech/comic-sans-replacer (see http://comicneue.com/)

---------------------------------------
# rdc.apicit.net/tags.clickintext.net

```
{
    "csp-report": {
        "document-uri": "https://www.estcequonmetenprodaujourdhui.info/",
        "referrer": "",
        "violated-directive": "script-src",
        "effective-directive": "script-src",
        "original-policy": "default-src 'none';  script-src 'self' ; style-src 'self' 'nonce-a1c74e229ddba899e0755f048c03cbef27f7b82c91246ed161cb7eb96e92f2de170082a9a64d133e3aec9e5a339a0627ee6d860a016ad7397c40ca0dc9781131' ; img-src 'self'  data: ;  font-src 'self'; child-src 'self' ;  frame-ancestors 'none' ; manifest-src 'self' ; report-uri /csp-parser.php ;",
        "disposition": "enforce",
        "blocked-uri": "https://rdc.apicit.net/addtrack/index.fr.r1s147942.jquery.js?_=1491288121",
        "line-number": 12,
        "column-number": 31,
        "source-file": "https://tags.clickintext.net/fNTzhFiADKTTZ",
        "status-code": 0
    }
}
```

__WTF:__ nothing like this on the website.

__Answer:__ probable malware/ads on client. (to confirm)


---------------------------------------
# Anti adblock killer

```
{
    "csp-report": {
        "document-uri": "https://www.estcequonmetenprodaujourdhui.info/",
        "referrer": "",
        "violated-directive": "script-src 'unsafe-eval' 'self' www.3-analytics.com stats.g.doubleclick.net https://stats.g.doubleclick.net",
        "effective-directive": "script-src",
        "original-policy": "default-src 'none';script-src 'unsafe-eval' 'self' www.google-analytics.com stats.g.doubleclick.net https://stats.g.doubleclick.net;style-src 'self' 'unsafe-inline';img-src 'self' www.google-analytics.com stats.g.doubleclick.net https://stats.g.doubleclick.net data:;font-src 'self';child-src 'self';frame-ancestors 'none';manifest-src 'self';report-uri /csp-parser.php;",
        "blocked-uri": "https://reek.github.io/anti-adblock-killer/k2Uw7isHrMm5JXP1Vwdxc567ZKc1aZ4I.js",
        "line-number": 787,
        "column-number": 18,
        "status-code": 0
    }
}
```

__WTF:__ no script like this on the website ```anti-adblock-killer```.

__Answer:__ related to https://github.com/reek/anti-adblock-killer use.


---------------------------------------
# getpingu

```
{
    "csp-report": {
        "document-uri": "https://www.estcequonmetenprodaujourdhui.info/",
        "referrer": "",
        "violated-directive": "font-src",
        "effective-directive": "font-src",
        "original-policy": "default-src 'none';  script-src 'self' ; style-src 'self' 'nonce-5a294a67d2b3dbad928c8c7f3c9a9e8863c64676f6f5a3cd3297f933bc668f4fb18a672b7a0bbba10556c08664c8828a1cca6b652430dc7061919d4e95082192' ; img-src 'self'  data: ;  font-src 'self'; child-src 'self' ;  frame-ancestors 'none' ; manifest-src 'self' ; report-uri /csp-parser.php ;",
        "disposition": "enforce",
        "blocked-uri": "https://getpingu.com/assets/fonts/icomoon/icomoon.ttf",
        "status-code": 0
    }
}
```

__WTF:__ no asset like this on the website ```https://getpingu.com/assets/fonts/icomoon/icomoon.ttf```.

__Answer:__ probably related to a Chrome extension of https://getpingu.com/.


---------------------------------------
# BitDefender js injection?

```
{
    "csp-report": {
        "document-uri": "https://www.nicolas-hoffmann.net/source/",
        "referrer": "",
        "violated-directive": "style-src 'self' data:  ",
        "effective-directive": "style-src",
        "original-policy": "default-src 'none';  script-src 'self' google-analytics.com stats.g.doubleclick.net https://stats.g.doubleclick.net; style-src 'self' data:  ; img-src 'self' google-analytics.com stats.g.doubleclick.net https://stats.g.doubleclick.net ssl.google-analytics.com data: ;  connect-src 'self';  font-src 'self'; media-src 'self'; object-src 'self' www.youtube.com ;  child-src 'self' ;  frame-ancestors 'none' ; manifest-src 'self' ; form-action 'self' ; report-uri /csp-parser.php ;",
        "blocked-uri": "inline",
        "source-file": "https://www.nicolas-hoffmann.net/B1D671CF-E532-4481-99AA-19F420D90332/netdefender/hui/ndhui.js?0=0&0=0&0=0",
        "line-number": 195,
        "column-number": 10,
        "status-code": 0
    }
}
```

__WTF:__ no file like https://www.nicolas-hoffmann.net/B1D671CF-E532-4481-99AA-19F420D90332/netdefender/hui/ndhui.js?0=0&0=0&0=0" on this website

__Answer:__ a bug from BitDefender https://forum.bitdefender.com/index.php?/topic/36108-netdefenderhuindhuijs/ && https://www.mediawiki.org/wiki/Topic:Sfreu9aqsah82mdz


---------------------------------------
# var Cacaoweb

```
{
    "csp-report": {
        "blocked-uri": "self",
        "document-uri": "[anonymised]",
        "line-number": 1,
        "original-policy": "default-src [anonymised]; script-src [anonymised] http://www.google-analytics.com https://www.google-analytics.com http://stats.g.doubleclick.net https://stats.g.doubleclick.net 'unsafe-eval'; style-src [anonymised] data: 'unsafe-inline'; img-src [anonymised] http://www.google-analytics.com https://www.google-analytics.com http://stats.g.doubleclick.net https://stats.g.doubleclick.net data:; child-src [anonymised]; report-uri [anonymised]/csp-parser.php",
        "referrer": "https://www.google.fr/",
        "script-sample": "var Cacaoweb = { callbackIsRunning: func...",
        "source-file": "[anonymised]/fr/",
        "violated-directive": "script-src [anonymised] http://www.google-analytics.com https://www.google-analytics.com http://stats.g.doubleclick.net https://stats.g.doubleclick.net 'unsafe-eval'"
    }
}
```

__WTF:__ var Cacaoweb = { callbackIsRunning… (nothing like this on this website)

__Answer:__ Might be related to an extension named Cacaoweb https://github.com/PinoDeiPalazzi/cacaowebinterface/blob/master/chrome%20addon/cacaoweb.js


---------------------------------------
# uBlock and Faceporn (yes!)

```
{
    "csp-report": {
        "blocked-uri": "self",
        "document-uri": "https://www.estcequonmetenprodaujourdhui.info/",
        "line-number": 1,
        "original-policy": "default-src 'none'; script-src https://www.estcequonmetenprodaujourdhui.info; style-src https://www.estcequonmetenprodaujourdhui.info 'nonce-IfAzvGfLDZPy2xJ5ew818hNfNFX8X8IDJleC1bw0+4laSFwurX1LT76CTFga'; img-src https://www.estcequonmetenprodaujourdhui.info data:; font-src https://www.estcequonmetenprodaujourdhui.info; child-src https://www.estcequonmetenprodaujourdhui.info; frame-ancestors 'none'; manifest-src https://www.estcequonmetenprodaujourdhui.info; report-uri https://www.estcequonmetenprodaujourdhui.info/csp-parser.php",
        "referrer": "",
        "script-sample": "[href^=\"http://www.faceporn.net/free?\"]\n...",
        "source-file": "https://www.estcequonmetenprodaujourdhui.info/",
        "violated-directive": "style-src https://www.estcequonmetenprodaujourdhui.info 'nonce-IfAzvGfLDZPy2xJ5ew818hNfNFX8X8IDJleC1bw0+4laSFwurX1LT76CTFga'"
    }
}
```

__WTF:__ faceporn.net ?????????????????????????????????????????????????????????? (nothing like this on this website)

__Answer:__ Might be related to an issue in extensions like uBlock https://github.com/chrisaljoudi/uBlock/issues/161 that are inserting inline-styles to hide links pointing out to this.

---------------------------------------
# Android webview

```
{
    "csp-report": {
        "document-uri": "https://www.nicolas-hoffmann.net/source/1301-Balise-video-Ogg-Theora-Mp4-et-HTML5.html",
        "referrer": "https://www.google.com/search?q=mp4&hl=fr&source=android-browser-type&prmd=svin&source=lnms&tbm=vid&sa=X&ved=0ahUKEwiikYPD_ZXSAhWjHsAKHQoNAgkQ_AUICCgB",
        "violated-directive": "img-src 'self' google-analytics.com stats.g.doubleclick.net https://stats.g.doubleclick.net ssl.google-analytics.com data: ",
        "original-policy": "default-src 'none';  script-src 'self' google-analytics.com stats.g.doubleclick.net https://stats.g.doubleclick.net; style-src 'self' data:  ; img-src 'self' google-analytics.com stats.g.doubleclick.net https://stats.g.doubleclick.net ssl.google-analytics.com data: ;  connect-src 'self';  font-src 'self'; media-src 'self'; object-src 'self' www.youtube.com ;  child-src 'self' ;  frame-ancestors 'self' ; manifest-src 'self' ; form-action 'self' ; report-uri /csp-parser.php ;",
        "blocked-uri": "android-webview",
        "status-code": 0

    }
}
```

__WTF:__ android-webview

__Answer:__ web view in android app.


---------------------------------------
# Devtools ?

```
{
    "csp-report": {
        "blocked-uri": "self",
        "document-uri": "https://www.estcequonmetenprodaujourdhui.info/",
        "line-number": 1,
        "original-policy": "default-src 'none'; script-src https://www.estcequonmetenprodaujourdhui.info; style-src https://www.estcequonmetenprodaujourdhui.info 'unsafe-inline'; img-src https://www.estcequonmetenprodaujourdhui.info data:; font-src https://www.estcequonmetenprodaujourdhui.info; child-src https://www.estcequonmetenprodaujourdhui.info; frame-ancestors 'none'; manifest-src https://www.estcequonmetenprodaujourdhui.info; report-uri https://www.estcequonmetenprodaujourdhui.info/csp-parser.php",
        "referrer": "",
        "script-sample": "window.devToolsOptions = Object.assign(w...",

        "source-file": "https://www.estcequonmetenprodaujourdhui.info/",
        "violated-directive": "script-src https://www.estcequonmetenprodaujourdhui.info"
    }
}
```

__WTF:__ window.devToolsOptions

__Answer:__ might be related to [Redux DevTools extension](http://extension.remotedev.io/) (to confirm).  


---------------------------------------
# Digg

```
{
    "csp-report": {
        "blocked-uri": "self",
        "document-uri": "https://rocssti.net/realisations-css-rocssti",
        "line-number": 1,
        "original-policy": "default-src 'none'; script-src https://rocssti.net https://www.google-analytics.com https://stats.g.doubleclick.net https://stats.g.doubleclick.net; style-src https://rocssti.net; img-src https://rocssti.net https://www.google-analytics.com https://stats.g.doubleclick.net https://stats.g.doubleclick.net data:; font-src https://rocssti.net; connect-src https://rocssti.net; child-src https://rocssti.net; frame-ancestors 'none'; manifest-src https://rocssti.net; form-action https://rocssti.net; report-uri https://rocssti.net/csp-parser.php",
        "referrer": "https://t.co/JFev84Iili",
        "script-sample": "dummyRuleForDigg{}",

        "source-file": "https://rocssti.net/realisations-css-rocssti",
        "violated-directive": "style-src https://rocssti.net"
    }
}
```

__WTF:__ dummyRuleForDigg{} ?

__Answer:__ caused by Digg, but don't have any details on how it happens (extension, other ?).

---------------------------------------
# Evernote

```
{
    "csp-report": {
        "blocked-uri": "self",
        "document-uri": "https://www.nicolas-hoffmann.net/source/1573-Guides-de-styles-CSS-pour-integrateur.html",
        "line-number": 1,
        "original-policy": "default-src 'none'; script-src https://www.nicolas-hoffmann.net https://google-analytics.com https://stats.g.doubleclick.net https://stats.g.doubleclick.net; style-src https://www.nicolas-hoffmann.net data:; img-src https://www.nicolas-hoffmann.net https://google-analytics.com https://stats.g.doubleclick.net https://stats.g.doubleclick.net https://ssl.google-analytics.com data:; connect-src https://www.nicolas-hoffmann.net; font-src https://www.nicolas-hoffmann.net; media-src https://www.nicolas-hoffmann.net; object-src https://www.nicolas-hoffmann.net https://www.youtube.com; child-src https://www.nicolas-hoffmann.net; frame-ancestors 'none'; manifest-src https://www.nicolas-hoffmann.net; form-action https://www.nicolas-hoffmann.net; report-uri https://www.nicolas-hoffmann.net/csp-parser.php",
        "referrer": "http://openweb.eu.org/articles/taking-css-conventions-and-document-them",
        "script-sample": "/* Copyright 2014 Evernote Corporation. ...",

        "source-file": "https://www.nicolas-hoffmann.net/source/1573-Guides-de-styles-CSS-pour-integrateur.html",
        "violated-directive": "style-src https://www.nicolas-hoffmann.net data:"
    }
}
```

__WTF:__ Copyright 2014 Evernote

__Answer:__ caused by Evernote Web Clipper, https://discussion.evernote.com/topic/85811-evernote-adding-styling-to-my-html-in-phpstorm/


---------------------------------------
# CSP What The Font number two

```
{
    "csp-report": {
        "document-uri": "https://van11y.net/fr/infobulles-tooltips-accessibles/",
        "referrer": "https://t.co/TgcBdtHiqn",
        "violated-directive": "font-src",
        "effective-directive": "font-src",
        "original-policy": "default-src 'none' ;  script-src 'self'; style-src 'self' ; img-src 'self'; font-src 'self';  connect-src 'self'; child-src 'self' ; frame-ancestors 'none' ; manifest-src 'self' ; report-uri /csp-parser.php ;",
        "disposition": "enforce",
        "blocked-uri": "http://themes.googleusercontent.com/static/fonts/inconsolata/v5/BjAYBlHtW3CJxDcjzrnZCIbN6UDyHWBl620a-IRfuBk.woff",
        "status-code": 0
    }
}
```
and
```
{
    "csp-report": {
        "document-uri": "https://rocssti.net/realisations-css-rocssti",
        "referrer": "https://t.co/JFev84Iili",
        "violated-directive": "font-src",
        "effective-directive": "font-src",
        "original-policy": "default-src 'none';  script-src 'self' www.google-analytics.com stats.g.doubleclick.net https://stats.g.doubleclick.net; style-src 'self' ; img-src 'self' www.google-analytics.com stats.g.doubleclick.net https://stats.g.doubleclick.net data: ;  font-src 'self'; connect-src 'self'; child-src 'self' ;  frame-ancestors 'none' ; manifest-src 'self' ; form-action 'self' ; report-uri /csp-parser.php ;",
        "disposition": "enforce",
        "blocked-uri": "http://themes.googleusercontent.com/static/fonts/rosarivo/v1/OGdIq-p0tOtBN2VMVvO9W_esZW2xOQ-xsNqO47m55DA.woff",
        "status-code": 0

    }
}
```

__WTF:__ Inconsolata et Rosarivo are not used on these sites, neither any reference to CSS from google font. (?)

__Answer:__ Related to extension that allow to personnalize fonts, like https://chrome.google.com/webstore/detail/font-changer-with-google/jgjhhoglgjdklldfgoffdiaceffijeke/related

---------------------------------------
# CSP What The Font number one

```
{
    "csp-report": {
        "document-uri": "about:blank",
        "referrer": "",
        "violated-directive": "font-src 'self'",
        "effective-directive": "font-src",
        "original-policy": "default-src 'none';  script-src 'self' google-analytics.com stats.g.doubleclick.net https://stats.g.doubleclick.net; style-src 'self' data:  ; img-src 'self' google-analytics.com stats.g.doubleclick.net https://stats.g.doubleclick.net ssl.google-analytics.com data: ;  connect-src 'self';  font-src 'self'; media-src 'self'; object-src 'self' www.youtube.com ;  child-src 'self' ;  frame-ancestors 'none' ; manifest-src 'self' ; form-action 'self' ; report-uri /csp-parser.php ;",
        "blocked-uri": "https://github.com/google/fonts/blob/master/apache/opensans/OpenSans-Light.ttf?raw=true",
        "status-code": 0
    }
}
```
and
```
{
    "csp-report": {
        "document-uri": "about:blank",
        "referrer": "",
        "violated-directive": "font-src 'self'",
        "effective-directive": "font-src",
        "original-policy": "default-src 'none';  script-src 'self' google-analytics.com stats.g.doubleclick.net https://stats.g.doubleclick.net; style-src 'self' data:  ; img-src 'self' google-analytics.com stats.g.doubleclick.net https://stats.g.doubleclick.net ssl.google-analytics.com data: ;  connect-src 'self';  font-src 'self'; media-src 'self'; object-src 'self' www.youtube.com ;  child-src 'self' ;  frame-ancestors 'none' ; manifest-src 'self' ; form-action 'self' ; report-uri /csp-parser.php ;",
        "blocked-uri": "https://fonts.gstatic.com/s/opensans/v13/PRmiXeptR36kaC0GEAetxko2lTMeWA_kmIyWrkNCwPc.woff2",
        "status-code": 0

    }
}
```

__WTF:__ Open Sans is suggested on the website https://www.estcequonmetenprodaujourdhui.info/ but not from Github or Google, and not even loaded from a webfont.

__Answer:__ Might be related to extension that allow to personnalize fonts, like https://chrome.google.com/webstore/detail/font-changer-with-google/jgjhhoglgjdklldfgoffdiaceffijeke/related

---------------------------------------
# Opera mini double WTF

```
{
    "csp-report": {
        "document-uri": "[Anonymised]",
        "referrer": "https://www.google.ch/",
        "violated-directive": "style-src 'self' data: ",
        "effective-directive": "style-src",
        "original-policy": "default-src 'self';  script-src 'self' https://www.google-analytics.com http://www.google-analytics.com  stats.g.doubleclick.net https://stats.g.doubleclick.net ; style-src 'self' data: ; img-src 'self' https://www.google-analytics.com http://www.google-analytics.com *.[anonymised] stats.g.doubleclick.net https://stats.g.doubleclick.net data: ;  child-src 'self' ; report-uri /csp-parser.php ;",
        "blocked-uri": "http://adblockers.opera-mini.net",
        "status-code": 200

    }
}
```
or
```
{
    "csp-report": {
        "document-uri": "https://www.estcequonmetenprodaujourdhui.info/",
        "referrer": "",
        "violated-directive": "style-src",
        "effective-directive": "style-src",
        "original-policy": "default-src 'none';  script-src 'self' ; style-src 'self' 'nonce-1e06551000a8d8186c9e4fa4b3a3d42536156246d4f94be747dea5b2b3513850dbfd186ffd8bf437b33ead6c16f9bdb4b349156b75e91a1f8df880471cf69bb3' ; img-src 'self'  data: ;  font-src 'self'; child-src 'self' ;  frame-ancestors 'none' ; manifest-src 'self' ; report-uri /csp-parser.php ;",
        "disposition": "enforce",
        "blocked-uri": "https://adblockers.opera-mini.net/css_block/page_0_24e0kl4y70wbt1yl6ubo6mmu4iikj9axe517otg3vbutjnpeiy.css",
        "line-number": 143,
        "source-file": "https://www.estcequonmetenprodaujourdhui.info/",

        "status-code": 0
    }
}
```
and
```
{
    "csp-report": {
        "document-uri": "[Anonymised]",
        "referrer": "https://www.google.ch/",
        "violated-directive": "script-src 'self' https://www.google-analytics.com http://www.google-analytics.com  stats.g.doubleclick.net https://stats.g.doubleclick.net ",
        "effective-directive": "script-src",
        "original-policy": "default-src 'self';  script-src 'self' https://www.google-analytics.com http://www.google-analytics.com  stats.g.doubleclick.net https://stats.g.doubleclick.net ; style-src 'self' data: ; img-src 'self' https://www.google-analytics.com http://www.google-analytics.com *.[anonymised] stats.g.doubleclick.net https://stats.g.doubleclick.net data: ;  child-src 'self' ; report-uri /csp-parser.php ;",
        "blocked-uri": "opera://js-inject",

        "status-code": 200
    }
}
```

__WTF:__ adblockers.opera-mini.net and opera://js-inject ???

__Answer:__ related to Opera Mini (these 2 notification came at the same time on the same page). If you have more details on how Opera mini works (I’m not expert in Opera mini), do not hesitate to complete.


---------------------------------------
# ms-browser-extension

```
{
    "csp-report": {
        "document-uri": "http://www.visionclinique.ch/fr/la-clinique",
        "referrer": "http://www.visionclinique.ch/fr/",
        "violated-directive": "img-src 'self' http://www.google-analytics.com https://www.google-analytics.com stats.g.doubleclick.net https://stats.g.doubleclick.net data: ",
        "effective-directive": "img-src",
        "original-policy": "default-src 'self';  script-src 'self' http://www.google-analytics.com https://www.google-analytics.com stats.g.doubleclick.net https://stats.g.doubleclick.net 'unsafe-eval' ; style-src 'self'  data: 'unsafe-inline' ; img-src 'self' http://www.google-analytics.com https://www.google-analytics.com stats.g.doubleclick.net https://stats.g.doubleclick.net data: ;  child-src 'self' ; report-uri /csp-parser.php ;",
        "blocked-uri": "ms-browser-extension",
        "status-code": 200

    }
}
```

__WTF:__ ms-browser-extension ? 

__Answer:__ browser extension on Edge/IE ? (to confirm, I don't know how to reproduce)



---------------------------------------
# ISP updates/adds files on mobiles

```
{
    "csp-report": {
        "document-uri": "[anonymised]",
        "referrer": "http://www.google.fr/",
        "violated-directive": "img-src 'self' *.google-analytics.com stats.g.doubleclick.net data: ",
        "effective-directive": "img-src",
        "original-policy": "default-src 'self';  script-src 'self' *.google-analytics.com stats.g.doubleclick.net ; style-src 'self' data: ; img-src 'self' *.google-analytics.com stats.g.doubleclick.net data: ;  child-src 'self' ; report-uri /csp-parser.php ;",
        "blocked-uri": "http://91.68.209.8/bmi/[anonymised]/layout/images/…",
        "status-code": 200
    }
}
```

__WTF:__ no code like this 91.68.209.8/bmi/ on the website.

__Answer:__ might be related to some ISPs that are inserting scripts on your website, probably with proxies (see http://security.stackexchange.com/questions/9368/mobile-carrier-javascript-injection or https://reflets.info/sfr-modifie-le-source-html-des-pages-que-vous-visitez-en-3g/ in french).


---------------------------------------
# Google translate

```
{
    "csp-report": {
        "document-uri": "[anonymised]",
        "referrer": "[anonymised]",
        "violated-directive": "img-src 'self' *.google-analytics.com stats.g.doubleclick.net data: ",
        "effective-directive": "img-src",
        "original-policy": "default-src 'self';  script-src 'self' *.google-analytics.com stats.g.doubleclick.net ; style-src 'self' data: ; img-src 'self' *.google-analytics.com stats.g.doubleclick.net data: ;  child-src 'self' ; report-uri /csp-parser.php ;",
        "blocked-uri": "https://www.gstatic.com/images/branding/product/2x/translate_24dp.png",
        "status-code": 200
    }
}
```

__WTF:__ no code like this on this website.

__Answer:__ related to Google Translate <del>however, to confirm in which exact case it happens</del>, Pavel B. confirmed: happens when a user translates the page using Google Translate inside Google Chrome (at least on Android, did not happen in Chrome for desktop).


---------------------------------------
# onsubmit/onchange/onfocusin/etc. attribute on DIV element

```
{
    "csp-report": {
        "blocked-uri": "self",
        "document-uri": "https://van11y.net/accessible-accordion/",
        "original-policy": "default-src 'none'; script-src https://van11y.net; style-src https://van11y.net; img-src https://van11y.net; font-src https://van11y.net; connect-src https://van11y.net; child-src https://van11y.net; frame-ancestors 'none'; manifest-src https://van11y.net; report-uri https://van11y.net/csp-parser.php",
        "referrer": "https://www.google.com.au/",
        "script-sample": "onsubmit attribute on DIV element",
        OR
        "script-sample": "onchange attribute on DIV element",
        OR 
        "script-sample": "onfocusin attribute on DIV element",
        OR
        "script-sample": "onselectstart attribute on DIV element", 

        "source-file": "https://van11y.net/accessible-accordion/",
        "violated-directive": "script-src https://van11y.net"
    }
}
```

__WTF:__ WTF is this? (no event like this on this website)

__Answer:__ This seems to be related to a check in Jquery 1.x. See https://bugzilla.mozilla.org/show_bug.cgi?id=1336076 for details


---------------------------------------
# pstatic.davebestdeals.com

```
{
    "csp-report": {
        "document-uri": "[anonymised]",
        "referrer": "https://www.google.pl/",
        "violated-directive": "script-src 'self' *.google-analytics.com stats.g.doubleclick.net ",
        "effective-directive": "script-src",
        "original-policy": "default-src 'self';  script-src 'self' *.google-analytics.com stats.g.doubleclick.net ; style-src 'self' data: ; img-src 'self' *.google-analytics.com stats.g.doubleclick.net data: ;  child-src 'self' ; report-uri /csp-parser.php ;",
        "blocked-uri": "http://pstatic.davebestdeals.com/nwp/v0_0_1143/release/Shared/App/SharedApp.js?t=3",

        "line-number": 2,
        "column-number": 1381,
        "source-file": "http://istatic.davebestdeals.com/fo/ec/ade.js?subid=test5",
        "status-code": 200
    }
}
```

__WTF:__ WTF is this? (no source like this in the website)

__Answer:__ Might be a malware on client machine: http://urlquery.net/report.php?id=1482137618866 (to confirm)


---------------------------------------

# function installGlobalHook(window)?
```
{
    "csp-report": {
        "blocked-uri": "self",
        "document-uri": "https://www.estcequonmetenprodaujourdhui.info/",
        "line-number": 1,
        "original-policy": "default-src 'none'; script-src https://www.estcequonmetenprodaujourdhui.info https://www.google-analytics.com https://stats.g.doubleclick.net https://stats.g.doubleclick.net; style-src https://www.estcequonmetenprodaujourdhui.info 'unsafe-inline'; img-src https://www.estcequonmetenprodaujourdhui.info https://www.google-analytics.com https://stats.g.doubleclick.net https://stats.g.doubleclick.net data:; font-src https://www.estcequonmetenprodaujourdhui.info; frame-ancestors 'none'; manifest-src https://www.estcequonmetenprodaujourdhui.info; report-uri https://www.estcequonmetenprodaujourdhui.info/csp-parser.php",
        "referrer": "",
        "script-sample": ";(function installGlobalHook(window) {\n\"...",

        "source-file": "https://www.estcequonmetenprodaujourdhui.info/",
        "violated-directive": "script-src https://www.estcequonmetenprodaujourdhui.info https://www.google-analytics.com https://stats.g.doubleclick.net https://stats.g.doubleclick.net"
    }
}
```

__WTF:__ WTF is this?

__Answer:__ related to React Devtools Chrome extension https://github.com/facebook/react-devtools/blob/master/backend/installGlobalHook.js (thanks @julienbrument)


---------------------------------------

# Facebook

```
{
    "csp-report": {
        "document-uri": "https://van11y.net/fr/news",
        "referrer": "http://l.facebook.com/lsr.php?u=https%3A%2F%2Fvan11y.net%2Ffr%2Fnews&ext=1484049768&hash=Acnqg-XK_DjHw5pz1PFrhONBex15J-PaH_UELLYmOrB5qA",
        "violated-directive": "script-src 'self'",
        "effective-directive": "script-src",
        "original-policy": "default-src 'none' ;  script-src 'self'; style-src 'self' ; img-src 'self'; font-src 'self';  connect-src 'self'; child-src 'self' ; frame-ancestors 'none' ; manifest-src 'self' ; report-uri /csp-parser.php ;",
        "blocked-uri": "eval",
        "line-number": 1,
        "column-number": 33772,
        "status-code": 0
    }
}
```

__WTF:__ WTF is this? (no Facebook on website)

__Answer:__ This notification happens when you share a page on Facebook.


---------------------------------------

## "Reader" in MacOS Safari?
```
{
    "csp-report": {
        "document-uri": "Anonymized",
        "referrer": "Anonymized",
        "violated-directive": "default-src 'self'",
        "original-policy": "default-src 'self';  script-src 'self' https://www.google-analytics.com http://www.google-analytics.com  stats.g.doubleclick.net https://stats.g.doubleclick.net ; style-src 'self' data: ; img-src 'self' https://www.google-analytics.com http://www.google-analytics.com Anonymized stats.g.doubleclick.net https://stats.g.doubleclick.net data: ;  child-src 'self' ; report-uri /csp-parser.php ;",
        "blocked-uri": "mx://res/reader-mode/reader.html"
    }
}
```

__WTF:___ ```mx://res/reader-mode/reader.html```

__Answer:__ Might be related to "Reader" in MacOS Safari. (to confirm)

---------------------------------------

## Kaspersky

```
{
    "csp-report": {
        "document-uri": "Anonymized",
        "referrer": "https://www.google.ch/",
        "violated-directive": "script-src 'self' https://www.google-analytics.com http://www.google-analytics.com stats.g.doubleclick.net https://stats.g.doubleclick.net http://gc.kis.scr.kaspersky-labs.com",
        "effective-directive": "script-src",
        "original-policy": "default-src 'self'; connect-src 'self' http://gc.kis.scr.kaspersky-labs.com; script-src 'self' https://www.google-analytics.com http://www.google-analytics.com stats.g.doubleclick.net https://stats.g.doubleclick.net http://gc.kis.scr.kaspersky-labs.com; img-src 'self' https://www.google-analytics.com http://www.google-analytics.com Anonymized stats.g.doubleclick.net https://stats.g.doubleclick.net data: http://gc.kis.scr.kaspersky-labs.com; style-src 'self' data: 'nonce-1B74BD89-2A22-4B93-B451-1C9E1052A0EC'; child-src 'self' ; report-uri /csp-parser.php",
        "blocked-uri": "http://www.tabcontent.net",
        "source-file": "http://apps-analytics.net",
        "line-number": 1,
        "column-number": 299,
        "status-code": 200
    }
}
```
__WTF:___ ```http://gc.kis.scr.kaspersky-labs.com```, ```http://gc.kis.scr.kaspersky-labs.com```, ```nonce-1B74BD89-2A22-4B93-B451-1C9E1052A0EC``` are not in the CSP policy header sent (????), how these can be reported?

__Answer:__ Explanation kindly provided by [@tigertoes](https://github.com/tigertoes):

> Browser extensions can, and do have the ability to modify CSP policy directives BEFORE the user agent applies them. https://matthewspencer.github.io/browser-extensions-and-csp-headers/
this useful blog post expands more on how to practically apply it. I too have seen lots of reports (it appears in 5% of all my reports on a large trafficked website). Kaspersky offers browser extensions that some users to actually install, I'm convinced it's these that are the cause.

> Bloxx, Zscaler, Blackspider, and many more products are also doing this. What's really hard is that some of these products also offer MITM products, so it's hard to know if they are rewriting the response headers at the networking layer, or it's "MITB" (man in the browser, aka these extensions). One can corellate from HPKP reporting, however if the user's machine has the MITM'd CA in their trust chain, it's all moot.

---------------------------------------

## Kaspersky crap

```
{
    "csp-report": {
        "blocked-uri": "self",
        "document-uri": "https://www.nicolas-hoffmann.net/source/1447-Background-image-couleurs-CSS-accessibilite.html",
        "original-policy": "default-src 'none'; connect-src https://www.nicolas-hoffmann.net https://ff.kis.v2.scr.kaspersky-labs.com wss://ff.kis.v2.scr.kaspersky-labs.com; script-src https://www.nicolas-hoffmann.net https://google-analytics.com https://stats.g.doubleclick.net https://stats.g.doubleclick.net https://ff.kis.v2.scr.kaspersky-labs.com wss://ff.kis.v2.scr.kaspersky-labs.com; img-src https://www.nicolas-hoffmann.net https://google-analytics.com https://stats.g.doubleclick.net https://stats.g.doubleclick.net https://ssl.google-analytics.com data: https://ff.kis.v2.scr.kaspersky-labs.com wss://ff.kis.v2.scr.kaspersky-labs.com; style-src https://www.nicolas-hoffmann.net data: 'nonce-CE685168D546AE408DFC9824262D6189' https://ff.kis.v2.scr.kaspersky-labs.com wss://ff.kis.v2.scr.kaspersky-labs.com; font-src https://www.nicolas-hoffmann.net; media-src https://www.nicolas-hoffmann.net; object-src https://www.nicolas-hoffmann.net https://www.youtube.com; child-src https:!
 //www.nicolas-hoffmann.net; frame-ancestors https://www.nicolas-hoffmann.net; manifest-src https://www.nicolas-hoffmann.net; form-action https://www.nicolas-hoffmann.net; report-uri https://www.nicolas-hoffmann.net/csp-parser.php",
        "referrer": "https://www.google.fr/",
        "script-sample": "transform:translate(NaNpx, NaNpx);",

        "source-file": "https://www.nicolas-hoffmann.net/source/1447-Background-image-couleurs-CSS-accessibilite.html",
        "violated-directive": "style-src https://www.nicolas-hoffmann.net data: 'nonce-CE685168D546AE408DFC9824262D6189' https://ff.kis.v2.scr.kaspersky-labs.com wss://ff.kis.v2.scr.kaspersky-labs.com"
    }
}
```

__WTF:___ ```"script-sample": "transform:translate(NaNpx, NaNpx);",``` seriously.

__Answer:__ still Kaspersky doign some crap.


---------------------------------------

## GSA

```
{
    "csp-report": {
        "document-uri": "Anonymized",
        "referrer": "https://www.google.ch/",
        "violated-directive": "default-src 'self'",
        "original-policy": "default-src 'self';  script-src 'self' http://www.google-analytics.com https://www.google-analytics.com stats.g.doubleclick.net https://stats.g.doubleclick.net 'unsafe-eval' ; style-src 'self'  data: 'unsafe-inline' ; img-src 'self' http://www.google-analytics.com https://www.google-analytics.com stats.g.doubleclick.net https://stats.g.doubleclick.net data: ;  child-src 'self' ; report-uri /csp-parser.php ;",
        "blocked-uri": "gsa://onpageload"
    }
}
```
__WTF:___ ```gsa://onpageload```

__Answer:__ Appears to be related to Google Search App on iOS.

---------------------------------------

## Ghostery
```
{
    "csp-report": {
        "blocked-uri": "self",
        "document-uri": "https://rocssti.net/",
        "line-number": 1,
        "original-policy": "default-src https://rocssti.net https://rocssti.net; script-src https://rocssti.net https://rocssti.net https://www.google-analytics.com https://stats.g.doubleclick.net https://stats.g.doubleclick.net; style-src https://rocssti.net https://rocssti.net data:; img-src https://rocssti.net https://rocssti.net https://www.google-analytics.com https://stats.g.doubleclick.net https://stats.g.doubleclick.net data:; child-src https://rocssti.net; report-uri https://rocssti.net/csp-parser.php",
        "referrer": "https://rocssti.net/realisations-css-rocssti",
        "script-sample": "@media print {#UNIQUE_ID-ghostery {displ...",

        "source-file": "https://rocssti.net/",
        "violated-directive": "style-src https://rocssti.net https://rocssti.net data:"
    }
}
```
or
```
        "script-sample": "@media print {#ghostery-purple-box {disp...",
```
or
```
        "script-sample": "#ghostery-button{z-index: 2147483646 !im...",
```

__WTF:__ Ghostery???

__Answer:__ Might be generated by inline-styles (if not allowed) by Ghostery extension on Firefox (to confirm). It is related to this bug of bookmarklets/extensions https://bugzilla.mozilla.org/show_bug.cgi?id=866522, and reported https://bugzilla.mozilla.org/show_bug.cgi?id=866522#c73

---------------------------------------

## Trusteer Rapport

```
{
    "csp-report": {
        "violated-directive": "connect-src 'self' checkout.stripe.com",
        "column-number": 9,
        "line-number": 49,
        "effective-directive": "connect-src",
        "document-uri": null,
        "status-code": 0
        "blocked-uri": "https://nikkomsgchannel/e?001e005100[...]",
        "original-policy": "script-src 'self' checkout.stripe.com; default-src 'self'; img-src 'self' q.stripe.com encryptr.org; media-src 'self'; style-src 'self' 'unsafe-inline'; frame-src 'self' checkout.stripe.com player.vimeo.com; connect-src 'self' checkout.stripe.com; font-src 'self'; report-uri /csp_report/",
    }
}
```

__WTF:__ Trusteer Rapport

__Answer:__ From an email conversation with IBM Security Trusteer Technical Support:

> "[...] please be advise [sic] that when a Chrome user clicks on areas in the page, it triggers https nikko requests (https://nikkomsgchannel/e?xxxx) in order to communicate with Rapport and to protect the user. The Nikko messages are expected as they indicate back and forth https requests between Rapport and the Chrome browser.

> In addition, kindly note that Rapport injects itself into the Chrome browser in order to track user action and to protect it from malicious activities. To do that, Rapport sends and uses back & forth requests with Chrome. The main implication is that when opening the Console (F12) these requests seem like failed requests.
The reason for this is that the console issues the https request externally / outside of the network. As a result, it returns with errors because there is no such external address, as the communication is internal between Rapport and Chrome.

> Lastly, please be advised that we can suggest steps on how to avoid these messages, but since these messages appear in an internal report, we suggest simply label it as a legit source."

Confirmed CSP reports received contain the user agent:  
`Mozilla/5.0 (Windows NT 10.0; Win64; x64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/53.0.2785.116 Safari/537.36`

Does not seem to affect Safari, Firefox or Micorsoft browsers.

---------------------------------------

# Browser Malware

```
{
"csp-report": {
            "document-uri": anonymised,
            "referrer": "https://www.google.fr/",
            "violated-directive": "script-src 'self' ssl.google-analytics.com www.google-analytics.com",
            "effective-directive": "script-src",
            "original-policy": "default-src 'self'; style-src 'self'; connect-src www.google-analytics.com; font-src 'none'; object-src 'none'; frame-src https://www.youtube-nocookie.com; child-src https://www.youtube-nocookie.com; script-src 'self' ssl.google-analytics.com www.google-analytics.com; img-src 'self' ssl.google-analytics.com www.google-analytics.com; report-uri /csp-report.php",
            "blocked-uri": "https://m12.dnsqa.me/QualityCheck/ga.js",
            "line-number": 45,
            "column-number": 285,
            "source-file": "https://www.google-analytics.com/analytics.js",
            "status-code" => 0
        }
}
```

__WTF:__ ```https://m12.dnsqa.me/QualityCheck/ga.js``` originating from ```https://www.google-analytics.com/analytics.js```

__Answer:__ A reply from security@google.com, relating to this and similar reports:

> I talked this report over with some of my colleagues on the security team, and at first I had thought that you might have had a user with a compromised corporate MITM proxy somewhere.  However, I think that the most likely situation is that these log entries are coming from a client who has been compromised and is running in-browser malware.  This in-browser malware is modifying the Analytics script to redirect users to the malicious domain, and I think this explains the discrepancy in line length between the analytics.js file you see and what shows up in the CSP violation report.

> I can mention that the Chrome team has a lot of people who are working on defending against in-browser malware, but I'm afraid that this isn't something that we can fix on the server side.


---------------------------------------

# Google Translate?

```
{
    "csp-report": {
        "document-uri": "Anonymized",
        "referrer": "Anonymized",
        "violated-directive": "img-src 'self' *.google-analytics.com stats.g.doubleclick.net data: ",
        "effective-directive": "img-src",
        "original-policy": "default-src 'self';  script-src 'self' *.google-analytics.com stats.g.doubleclick.net ; style-src 'self' data: ; img-src 'self' *.google-analytics.com stats.g.doubleclick.net data: ;  child-src 'self' ; report-uri /csp-parser.php ;",
        "blocked-uri": "https://www.gstatic.com/images/branding/product/2x/translate_24dp.png",
        "status-code": 200
    }
}
```

__WTF:__ The image is not on the website, at any place.

__Answer:__ Might be related to Google Translate. (to confirm how, and check how it can happen)


---------------------------------------
If you have some examples to share (even if you don't know what the fuck it is coming from), feel free to share them. Anonymize the URL/policy if needed.

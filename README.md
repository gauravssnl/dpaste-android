# dpaste-android
Android Application for sharing codes on [dpaste.com](http://dpaste.com) 


![ScreenShot]( https://github.com/gauravssnl/dpaste-android/blob/master/20180329_124139.gif )


Howto create a paste on dpaste.com?

We need to make a POST request to dpaste.com with thess paramaters:
content, syntax, title, poster, expiry_days

Sample code for making POST request to dpaste.com in JavaScript:
 ```javascript
url = "http://dpaste.com/api/v2/";
req = new XMLHttpRequest()
req.open("POST", url);
req.setRequestHeader("Content-Type", "application/x-www-form-urlencoded");
req.onload = function ()
{
	alert(req.response);
	app.SetClipboardText( req.response );
}
 params = "poster=gauravssnl&content=alert(ok)&syntax=js";
req.send(params);

```

You can set poster name and expiry days from Settings option from left drawer.

Author: gauravssnl

Dpaste Author: [Paul Bissex]( https://mobile.twitter.com/pbx/)

Thanks to Paul Bissex for creating dpaste.com

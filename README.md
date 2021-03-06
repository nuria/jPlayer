
http://www.jplayer.org/


Changes so jPlayer (audio) works with zepto. Added  1 skin.
------------------------------------------------------------

* Player requires zepto  with data and animation modules
  There is one method missing on zepto animation module to get player to work
  just stub it as follows

  ```javascript
      
	  $.fn.stop = function() {
			
			    }
  ```

* We have changed initialization, so the whole player is initialized in the
  Zepto callback.

* We have changed calls to data module, they are of the form $.data(this, <something>) on jquery
  and of the form $(this).data(<something>) on zepto.

* Note that the initialization for zepto and jquery is different 
  so player does not work under jquery now. It requires zepto-1.0 compiled with the
  optional data module.

* We have also added 1 skin called slim.


To use
------

There is plenty information on the jPlayer site on how to get it working, same applies here.
The only difference is that where it says to load jquery first you should load zepto first

```html
<script type="text/javascript" src="zepto.js"></script>
<script src="jquery.jplayer.js"></script>
```

Original readme of jPlayer follows
---------------------------------------------------
What is jPlayer?

jPlayer is a jQuery plugin that allows you to:

 * play and control media files in your webpage
 * create and style a media player using just HTML and CSS
 * add audio and video to your jQuery projects
 * support more devices using HTML5
 * support older browsers using a Flash Fallback
 * control media on your website using a JavaScript API

jPlayer supports:
 * HTML5: mp3, m4a (AAC), m4v (H.264), ogv*, oga*, wav*, webm*
 * Flash: mp3, m4a (AAC), m4v (H.264)
(*) Optional counterpart formats to increase HTML5 x-browser support.

Dual licensed under the MIT and GPL licenses.
 * http://www.opensource.org/licenses/mit-license.php
 * http://www.gnu.org/copyleft/gpl.html

Quick Start Guide:
http://www.jplayer.org/latest/quick-start-guide/

Developer Guide and API Reference:
http://www.jplayer.org/latest/developer-guide/

Author: Mark J Panaghiston

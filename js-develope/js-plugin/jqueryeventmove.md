#### *jquery.event.move*
---
> jquery 鼠标移动事件插件

* Version: 1.3.6
* Github: https://github.com/stephband/jquery.event.move
* Usage:
```
  $('.mydiv')
  .bind('movestart', function(e) {
      // move starts.

  })
  .bind('move', function(e) {
      // move .mydiv horizontally
      jQuery(this).css({ left: e.startX + e.deltaX });

  }).bind('moveend', function() {
      // move is complete!

  });
```
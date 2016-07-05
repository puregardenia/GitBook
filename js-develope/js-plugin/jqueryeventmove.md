## jquery.event.move

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

### API:

#### movestart

Fired following mousedown or touchstart, when the pointer crosses a threshold distance from the position of the mousedown or touchstart.

#### move

Fired on every animation frame where a mousemove or touchmove has changed the cursor position.

#### moveend

Fired following mouseup or touchend, after the last move event, and in the case of touch events when the finger that started the move has been lifted.

Move event objects are augmented with the properties:

  1. e.pageX  e.pageY
```
    Current page coordinates of pointer.
```
  1. e.startX e.startY
```
    Page coordinates the pointer had at movestart.
```
  1. e.deltaX e.deltaY
```
    Distance the pointer has moved since movestart.
```
  1. e.velocityX e.velocityY
```
    Velocity in pixels/ms, averaged over the last few events.
```
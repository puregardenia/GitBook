# jquery

> jquery 类库

* Version: 1.8.3
* CDN: http://apps.bdimg.com/libs/jquery/1.8.3/jquery.js
* Usage:
  *  示例一
  ```
  seajs.use('jquery',function($){
    $('.demo').hide();
  });
  ```
  *  示例二
  ```
  seajs.use(['jquery','animateColor']function($,animateColor){
    $('.demo').hide();
    $('.header a').animate({color: '#fff'},500);
  });
  ```

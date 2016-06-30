## JS插件说明
---
> 百度静态资源库公共库: http://cdn.code.baidu.com/

### COMMON
#### *tools*
---
* Version:
* Github:
* Website:

### LIB
#### *jquery*
---
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

#### *cookie*
---
> 操作cookie 插件

* Version: v2.1.2
* Github: https://github.com/js-cookie/js-cookie
* Usage

  Create a cookie, valid across the entire site:
  ```
  Cookies.set('name', 'value');
  ```

  Create a cookie that expires 7 days from now, valid across the entire site:
  ```
  Cookies.set('name', 'value', { expires: 7 });
  ```

  Create an expiring cookie, valid to the path of the current page:
  ```
  Cookies.set('name', 'value', { expires: 7, path: '' });
  ```

  Read cookie:
  ```
  Cookies.get('name'); // => 'value'
  Cookies.get('nothing'); // => undefined
  ```

  Read all visible cookies:
  ```
  Cookies.get(); // => { name: 'value' }
  ```

  Delete cookie:
  ```
  Cookies.remove('name');
  ```

  Delete a cookie valid to the path of the current page:
  ```
  Cookies.set('name', 'value', { path: '' });
  Cookies.remove('name'); // fail!
  Cookies.remove('name', { path: '' }); // removed!
  ```

#### *jquery.query*
---
> URL 查询插件

* Version: 2.2.3
* Github: https://github.com/alrusdi/jquery-plugin-query-object
* Usage:

  ```
  var url = location.search;
  > "?action=view&section=info&id=123&debug&testy[]=true&testy[]=false&testy[]"
  var section = $.query.get('section');
  > "info"
  var id = $.query.get('id');
  > 123
  var debug = $.query.get('debug');
  > true
  var arr = $.query.get('testy');
  > ["true", "false", true]
  var arrayElement = $.query.get('testy[1]');
  > "false"
  var newUrl = $.query.set("section", 5).set("action", "do").toString();
  > "?action=do&section=5&id=123"
  var newQuery = "" + $.query.set('type', 'string');
  > "?action=view&section=info&id=123&type=string"
  var oldQuery = $.query.toString();
  > "?action=view&section=info&id=123"
  var oldQuery2 = $.query;
  > ?action=view&section=info&id=123
  var newerQuery = $.query.SET('type', 'string');
  > ?action=view&section=info&id=123&type=string
  var notOldQuery = $.query.toString();
  > "?action=view&section=info&id=123&type=string"
  var oldQueryAgain = $.query.REMOVE("type");
  > ?action=view&section=info&id=123
  var removeElementByValue = $.query.REMOVE('section', 'info');
  > ?action=view&id=123
  var newerQuery2 = $.query.set('testy[]', 'true').set('testy[]', 'false').set('testy[]', 'true');
  > ?action=view&id=123&testy[0]=true&testy[1]=false&testy[2]=true
  var removeElementByValue1 = $.query.REMOVE('testy', 'false');
  > ?action=view&id=123&testy[0]=true&testy[1]=true
  var emptyQuery = $.query.empty();
  > ""
  var stillTheSame = $.query.copy();
  > ?action=view&section=info&id=123
  In case you dynamically change document.location via history API
  var parsedQuery = $.query.parseNew("?foo=bar", "bar=foo");
  > ?foo=bar&bar=foo
  In case you are using History.js
  var parsedQuery = $.query.parseNew(location.search, location.hash.split("?").length > 1 ? location.hash.split("?")[1] : "");
  ```

#### *placeholder*
---
* Version:
* Github:
* Website:

#### *animateColor*
---
> 颜色渐变插件

* Version: 1.6.0
* Github: https://github.com/edwinm/Color-animation-jQuery-plugin
* Website: http://www.bitstorm.org/jquery/color-animation/
* Usage:
  ```
  $('#demodiv').animate({color: '#E4D8B8'},500);
  $('#demodiv').animate({backgroundColor: '#400101'},1000);
  $('#demodiv').animate({borderBottomColor: '#00346B'});
  $('#demodiv').animate({borderColor: 'darkolivegreen'});
  $('#demodiv').animate({color: 'rgba(42, 47, 76, 0.1)'});
  ```

#### *animateNumber*
---
> 数字缓动插件

* Version: 0.0.13
* Github: https://github.com/aishek/jquery-animateNumber
* Website/Docs: http://aishek.github.io/jquery-animateNumber/
* CDN: ```<script src="//cdn.jsdelivr.net/jquery.color-animation/1/mainfile"></script>```


#### *Amcharts、serial*
---
> 报表

* Version:
* Website: https://www.amcharts.com/
* LiveEditor: https://live.amcharts.com/
* Docs: https://docs.amcharts.com/3/

#### *customSelect*
---
> 自定义下拉菜单

* Version: *
* Github: https://github.com/adamcoulombe/jquery.customSelect
* LiveEditor: http://jsfiddle.net/adamco/7ttWj/
* Usage:
  ```
  $('#fabric-type').customSelect({width:"120px",padding:"12px 5px"});
  ```

### *snipe*
---
> 放大镜插件

* Usage:

#### *spinner*
---
> 数字加减插件

* 参数：
  ```
  var defaults = {
      value: 1, //当前值
      min: 0, //最小值
      max: 999999, //最大值
      addEvent: function () { }, //加号事件
      cutEvent: function () { } //减号事件
  };
  ```
* Usage
  ```
  $('#abb-spinner').spinner({
    min:1,
    max:4,
    addEvent: function(){
      // 增加按钮事件
    },
    cutEvent: function(){
      // 减少按钮事件
    }
  }
  ```
#### *FancyRadioCheckBox*
---
> 美化单选复选框插件

* Version: *
* Github:
* Website:
* Require: ``.label_radio、.label_check``
  ```
  <label class="label_radio">
    <input name="radio1" type="radio" checked="checked"/>
    <span>单选按钮</span>
  </label>
  <label class="label_check">
    <input name="check1" type="checkbox" checked="checked" />
    <span>复选按钮</span>
  </label>
  ```
* Usage:
  ```
  FancyRadioCheckBox.init();
  ```

#### *tip*
---
> 提醒插件``poshytip``

* Version:
* Github:
* Website:

#### *layer*
---
> 弹窗插件

* Version: 1.8.5
* Github: https://github.com/sentsin/layer
* Website: http://layer.layui.com/1.8.5/

#### *laydate*
---
> 日历弹窗插件

* Version: 1.1
* Github: https://github.com/sentsin/laydate
* Website/Docs: http://laydate.layui.com/

#### *switchable*
---
> 标签切换、轮播图、幻灯片、手风琴 4合1

* Version: 2.0
* Github: https://github.com/jsw0528/jQuery.Switchable
* Website: http://switchable.mrzhang.me/

#### *fullPage*
---
> 全屏滚动插件

* Version: 2.5.4
* Github/Docs: https://github.com/alvarotrigo/fullPage.js

#### *jquery.event.move*
---
> jquery 鼠标移动事件插件

* Version: 1.3.6
* Github: https://github.com/stephband/jquery.event.move
* Usage
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
* API:
---
**movestart**

Fired following mousedown or touchstart, when the pointer crosses a threshold distance from the position of the mousedown or touchstart.

**move**

Fired on every animation frame where a mousemove or touchmove has changed the cursor position.

**moveend**

Fired following mouseup or touchend, after the last move event, and in the case of touch events when the finger that started the move has been lifted.
Move event objects are augmented with the properties:

**e.pageX** **e.pageY**

Current page coordinates of pointer.

**e.startX** **e.startY**

Page coordinates the pointer had at movestart.

**e.deltaX** **e.deltaY**

Distance the pointer has moved since movestart.

**e.velocityX** **e.velocityY**

Velocity in pixels/ms, averaged over the last few events.


#### *jquery.twentytwenty*
---
> 图片对比插件(有改动)

* Version: *
* Github: https://github.com/zurb/twentytwenty
* Website: http://zurb.com/playground/twentytwenty

# spinner
---
> 数字加减插件

* 参数

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
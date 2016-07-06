## tools

> 自定义常用工具

** 包含: **

  * `cookieHelp`:cookie 操作
  * `riqi`
  * `urlHelp`: url变量替换
  * `formate`: 数字小数位格式化
  * `addCss`: 向浏览器添加一个样式表
  * `validate`: 验证组件

### cookieHelp


*** Usage ***

```javascript
tool.cookieHelp.SetCookie('id',11);
tool.cookieHelp.GetCookie('id');
tool.cookieHelp.DeleteCookie('id');
tool.cookieHelp.getCookieVal(offset);
```

*** Demo ***

```javascript
seajs.use('tools',function(tool){
      tool.cookieHelp.SetCookie('a',13);
      console.log(tool.cookieHelp.GetCookie('a'));
}
```
### dateHelp

*** Usage ***


~~dateHelp.NewDate()~~


### urlHelp

*** Usage ***

```javascript
// url = http://localhost:8180/html/demo/test.html?a=20&b=1
console.log(tool.urlHelp.replaceParam('a',10));
// 输出 http://localhost:8180/html/demo/test.html?a=10&b=1
```

### formate

*** Usage ***

```javascript
///////////////////////格式化输入数字//////////////////////////////
tool.toDecimal2(x)        //强制保留2位小数，如：2，会在2后面补上00.即2.00

//如果小数位数大于2，保留2位小数，如：2.333，会即2.33 不四舍五入
//如果小数位数小于2，如为2.3结果仍为2.3 不强制补0 不四舍五入
tool.toKeepDecimal2(x)
```

### addCss

> 直接添加一个css文本

*** Usage ***

```JavaScript
tool.addCss(cssText)
```

### validate

*** Usage ***

```javascript
tool.validtaePhoneNum
tool.phoneRule
~~tool.countdown~~
tool.selectAllOrNone_ck(checkboxName,flag)    // 全选
tool.validate.PositiveNum(value)               // 验证正数 不包含0、负数
tool.validate.Num(value)                       // 验证数字包含负数 0
tool.validate.Num_plus(value)                  // 验证数字 不包含负数 包含0、整数、小数
tool.validate.NumPointNum(value,pointNum)           // 验证数字 可以是负数 小数 正数 ,自定义小数位数
tool.validate.NumPointNum_plus(value,pointNum)      //验证数字 可以 小数 正数 ,自定义小数位数
tool.validate.AllNum(value)                         // 验证数字 可以是负数 小数 正数
tool.validate.PositiveInt(value)                    // 大于0的整数

bankCoardCheck(bankno)                        //银行卡校验
```

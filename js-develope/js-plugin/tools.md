## tools

> 自定义常用工具，包含:
  * cookie 操作
  * 

### API

#### cookieHelp

```javascript
tool.cookieHelp.SetCookie('id',11);
tool.cookieHelp.GetCookie('id');
tool.cookieHelp.DeleteCookie('id');
tool.cookieHelp.getCookieVal(offset);
```

** Usage **

```javascript
seajs.use('tools',function(tool){
      tool.cookieHelp.SetCookie('a',13);
      console.log(tool.cookieHelp.GetCookie('a'));
}
```
## tools

> 自定义常用工具，包含:
  * cookie 操作
  * 

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
tool.urlHelp.replaceParam('a',10)
```
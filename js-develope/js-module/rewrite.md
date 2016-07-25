# 模块开发重写

```javascript
// 模块
define(function (require, exports, module) {
    // 提供重写接口
    exports.overwrite;
    
    if(exports.overwrite) exports.overwrite();
});

// 调用
 var match = require('js/front/easydata/common/match');
 match.overwrite = function () {
    
 }

seajs.use('match',function(match){
    match.overwrite = function(){
        
    }
});

```
```
define(function (require, exports, module) {
    var modExp = module.exports;
    
    var rules = modExp.rules;
    var submitHandler = modExp.submitHandler;
});
```
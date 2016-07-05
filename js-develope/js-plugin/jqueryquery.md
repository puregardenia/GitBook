# jquery.query

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
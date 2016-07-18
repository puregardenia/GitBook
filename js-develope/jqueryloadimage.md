## jquery.loadImage

> 图片加载等待功能

### Alias:

* jquery
* spin.js\(此插件已在jquery.loadImage.js引入\)

  > spin.js:[http://spin.js.org/](http://spin.js.org/)


### Usage:

```javascript
$("img").LoadImage({
 'imgSrc': 图片路径,
 'container': '显示等待图标的容器'
 'spin_size': '等待图标大小/normal/small'});
);

```

### Demo

```javascript
require(['jquery',' js/front/lib/jquery.loadImage '],function($,loadImage){
     var $li = $("<li clickLink='http://112.124.127.214:2323/images/production/easydesign/simulateFabric/02_simulateFabric.jpg'><img /></li>");
     $li.find('img').LoadImage({
        'imgSrc': 'http://112.124.127.214:2323/images/production/easydesign/simulateFabric/01_simulateFabric_vr.jpg',
        'container': '.simulationFabricImg',
        'spin_size': 'small'
    }); 
});
```

Url: `http://182.168.1.134:8180/html/easydesign/simulationFabric.html`


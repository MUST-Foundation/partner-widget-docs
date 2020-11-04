## Инструкция по установке виджета на сайт партнера

**Перед установкой виджета необходимо предоставить разработчикам api список всех доменов, на которые он будет установлен (в том числе и тестовые).**

Партнеру необходимо разместить у себя на странице контейнер виджета MUST Insurance
```
<div id="must-eosago-insurance-partner-widget"></div>
```

А ниже вставить скрипт
```
<script type="text/javascript">
  (function (document) {
    var tag = 'script';
    var el = document.createElement(tag)
    var bs = document.getElementsByTagName(tag)[0]
    el.src = 'https://osago-k8s.stage.mustins.ru/partner-loader.js?' + new Date().getTime()
    el.onload = function () {
      mustins({
        selector: '#must-eosago-insurance-partner-widget',
        ym: '52986040',
        source: '1111-1111-1111'
     })
    }
    bs.parentNode.insertBefore(el, bs);
  })(document);
</script>
```


Эту часть партнер может настроить самостоятельно
```
mustins({
  selector: '#must-eosago-insurance-partner-widget',
  ym: '52986040',
  source: '1111-1111-1111'
})

``` 
**selector** - это селектор для контейнера виджета  
**ym** - это номер счетчика яндекс метрики партнера  
**source** - id, который необходимо получить от разработчиков api, чтобы в битриксе правильно проставлялся источник сделки


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
        source: 'значение мы предоставим'
        theme: 'значение мы предоставим',
        mainPageUrl: 'адрес страницы где будет размещен виджет'
     })
    }
    bs.parentNode.insertBefore(el, bs);
  })(document);
</script>
```

**selector** - это селектор для контейнера виджета
**source** - id, который необходимо получить от разработчиков api, чтобы в битриксе правильно проставлялся источник сделки 
**theme** - название темы по которой дается общая стилистика виджета 


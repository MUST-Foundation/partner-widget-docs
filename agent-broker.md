
Для размещения на страницах

http://fura.agentbroker.ru

http://fura.agentbroker.ru/confirm-payment 

следует использовать следующий код

**Контейнер:**

```
<div id="must-eosago-insurance-partner-widget"></div>
```
**Скрипт виджета:**
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
        source: '6481d719-e635-480b-8f45-c5b1621bfcd2',
        theme: 'mustagentbroker',
        mainPageUrl: 'http://fura.agentbroker.ru'
      })
    }
    bs.parentNode.insertBefore(el, bs);
  })(document);
</script>
```

**Размещение виджета на странице http://fura.agentbroker.ru/confirm-payment  необходимо для работы виджета. На этой странице будет осуществляться загрузка документов подтверждающих оплату. Эти страницы должны быть доступны по прямой ссылке. На этих страницах форма ввода гос номера отображаться не будет, а будет сразу открываться попап для загрузки документов.**

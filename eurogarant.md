
Для размещения на страницах

http://www.eurogarant.ru

http://www.eurogarant.ru/confirm-payment 

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
        source: 'ce46d363-2166-4686-a223-46b85a1c523d',
        theme: 'musteurogarant',
        mainPageUrl: 'http://www.eurogarant.ru/'
      })
    }
    bs.parentNode.insertBefore(el, bs);
  })(document);
</script>
```

**Размещение виджета на странице http://www.eurogarant.ru/confirm-payment  необходимо для работы виджета. На этой странице будет осуществляться загрузка документов подтверждающих оплату. Эта страница должна быть доступна по прямой ссылке. На этой странице форма ввода гос номера отображаться не будет, а будет сразу открываться попап для загрузки документов.**

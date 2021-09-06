Для размещения на страницах

https://fleetly.kamaz.ru/osago

https://fleetly.kamaz.ru/confirm-payment

следует использовать следующий код

**Контейнер:**

```
<div id="kamaz-eosago-insurance-widget-prod"></div>
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
        selector: "#kamaz-eosago-insurance-widget-prod",
        source: "df290f83-d5d6-4260-a732-3ba4450b962b",
        theme: "kamaz",
        mainPageUrl: "https://fleetly.kamaz.ru/osago",
      })
    }
    bs.parentNode.insertBefore(el, bs);
  })(document);
</script>
```

**Размещение виджета на странице https://fleetly.kamaz.ru/confirm-payment необходимо для работы виджета. На этой странице будет осуществляться загрузка документов подтверждающих оплату. Эта страница должна быть доступна по прямой ссылке. На этой странице форма ввода гос номера отображаться не будет, а будет сразу открываться попап для загрузки документов.**

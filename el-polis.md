
Для размещения на страницах

https://el-polis.ru/agent#/osago/strahovanie_categoria_c

https://el-polis.ru/confirm-payment 

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
        source: '88cc9f26-d156-4835-940f-7304ade326a5',
        theme: 'mustelpolis',
        mainPageUrl: 'https://el-polis.ru/agent#/osago/strahovanie_categoria_c'
      })
    }
    bs.parentNode.insertBefore(el, bs);
  })(document);
</script>
```


Для размещения на

https://agentpolis.ru/agent#/osago/strahovanie_categoria_c

https://agentpolis.ru/confirm-payment

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
        source: '88cc9f26-d156-4835-940f-7304ade326a5',
        theme: 'mustelpolis',
        mainPageUrl: 'https://agentpolis.ru/agent#/osago/strahovanie_categoria_c\n'
      })
    }
    bs.parentNode.insertBefore(el, bs);
  })(document);
</script>

```
**Размещение виджета на страницах https://agentpolis.ru/confirm-payment и 
https://el-polis.ru/confirm-payment необходимо для работы виджета. На этих страницах будет осуществляться загрузка документов подтверждающих оплату. Эти страницы должны быть доступны по прямой ссылке. На этих страницах форма ввода гос номера отображаться не будет, а будет сразу открываться попап для загрузки документов.**

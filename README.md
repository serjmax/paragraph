# paragraph
Красивый текст в редимаг. 
Параграф:
1. Включает межсловесные переносы;
1. Добавляет свойство, в котором задаётся ширина пробелов;
1. Добавляет в проект стороннию библиотеку типограф.

## 1. Параграф
Добавляет межсловесные переносы. Управляет шириной межсловесных пробелов
В элемент `body` добавляем css свойства для межсловесных переносов и задания межсловесного расстояния.
```css
body{
  hyphens: auto;
  -moz-hyphens: auto;
  -webkit-hyphens: auto;
  -ms-hyphens: auto;

  word-spacing: normal;
}
```

Переносы работают только для основного языка. Поэтому чтобы переносы заработали в элемент `html` добавляем атрибут `lang="ru"` для русского языка как основного на сайте.
```javascript
<script>
  const htmlElement = document.documentElement;
  htmlElement.setAttribute("lang", "ru");
</script>
```

### Ссылки на сторонние библиотеки
+ https://mnater.github.io/Hyphenopoly/
+ http://mnater.github.io/Hyphenator/
+ https://github.com/bramstein/hypher/

## 2. Типограф
Помогает автоматически расставить неразрывные пробелы, исправить мелкие опечатки, привести кавычки к правильному виду, заменить дефисы на тире в нужных местах и многое другое.

Попробуйте [типограф в действии](https://typograf.github.io).
___
Подключаем типограф
```js
<script src="https://cdn.jsdelivr.net/gh/serjmax/paragraph@master/typograf.min.js"></script>
```

Добавляем код, который находит все элементы с тегом `p` и применяет к ним библиотеку типограф.
```js
<script>
  document.addEventListener('DOMContentLoaded', function() {
  	(function() {
      var tp = new Typograf({ locale: ["ru", "en-US"] });

      for (var i = 0; i < elements.length; i++) {
        elements[i].innerHTML = tp.execute(elements[i].innerHTML);
      };
    })();
  }, false);
</script>
```

## 3. Lottie-web
Библиотека lottie-web для JSON анимации

Подключаем библиотеку https://www.npmjs.com/package/lottie-web

```js
<script src="https://cdnjs.cloudflare.com/ajax/libs/bodymovin/5.5.2/lottie_svg.min.js"></script>
```

Вставляем анимацию из json файла

```js
<script>
  document.addEventListener('DOMContentLoaded', function() {
    // Получаем элемент в который будем вставлять анимацию
    const container = document.querySelector('[data-id="5cd88dc0f468402c4a53e9e0"]');

    // Вставляем анимацию
    const animation = bodymovin.loadAnimation({
      container: container,
      renderer: 'svg',
      loop: true,
      autoplay: true,
      path: 'https://raw.githubusercontent.com/serjmax/paragraph/master/data.json'
    });
    
  }, false);
</script>
```
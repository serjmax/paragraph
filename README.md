# paragraph
Красивый текст в редимаг. 
Параграф:
1. Включает межсловесные переносы;
1. Добавляет свойство, в котором задаётся ширина пробелов;
1. Добавляет в проект стороннию библиотеку типограф.

## 1. Межсловесные переносы и пробелы
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

## 3. JSON анимация

<!-- Вставляем новый объект в нутрь существующего -->
<script>
  document.addEventListener('DOMContentLoaded', function() {
  
    // Создаем новый элемент
    var div = document.createElement('div');
    div.className = "alert alert-success";
    div.innerHTML = "<strong>Ура!</strong> Вы прочитали это важное сообщение.";

    // Находим объект в который будем вставлять новый элемент
    var element = document.querySelector('[data-id="5cd6a16fe1fa4b788641b49a"]');

    // Вставляем элемент внутрь объекта
    element.appendChild(div);
    
  }, false);
</script>

<!-- Поиск и замена висящих предлогов через регулярные выражения -->
<script>
  document.addEventListener('DOMContentLoaded', function() {
  	
    // Выбираем весь DOM
  	const htmlElement = document.documentElement;
    
    
  }, false);
</script>
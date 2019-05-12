# paragraph
Красивый текст в редимаг. 
Параграф умеет делать:
1. Включать межсловесные переносы;
1. Помогает задать расстояние у пробелов;
1. (скоро) Автоматически расставлять неразрывные пробелы;
1. (скоро) Исправляет мелкие опечатки;
1. (скоро) Приводит кавычки к правильному виду;
1. (скоро) Заменяет дефисы на тире в нужных местах.

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


<script src="https://raw.githubusercontent.com/typograf/jquery-typograf/gh-pages/autotypograf.vanilla.js"></script>

<!-- Типограф -->
<script>
  document.addEventListener('DOMContentLoaded', function() {
  	
    // Выбираем весь DOM
  	const htmlElement = document.documentElement.typograf();
    
    
  }, false);
</script>






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
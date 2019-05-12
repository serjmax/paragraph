# paragraph
Красивый текст в редимаг. 
Параграф умеет делать:
1. Автоматически расставлять неразрывные пробелы;
2. Исправляет мелкие опечатки;
3. Приводит кавычки к правильному виду;
4. Заменяет дефисы на тире в нужных местах;
5. Включает межсловесные переносы;
6. Помогает задать расстояние межсловесным пробелам.

## 1. Межсловесные переносы и пробелы

Добавляем в эелемент html атрибут lang="ru":
```javascript
<script>
  const htmlElement = document.documentElement;
  htmlElement.setAttribute("lang", "ru");
  htmlElement.classList.add("hyphens");
</script>
```

Добавляем межсловесные переносы и задаем межсловесные расстояния через CSS свойства:
```css
html{
  hyphens: auto;
  -moz-hyphens: auto;
  -webkit-hyphens: auto;
  -ms-hyphens: auto;

  word-spacing: normal;
}
```
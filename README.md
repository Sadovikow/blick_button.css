# blick_button.css
Кнопка с эффектом блика

<b>1. Сама кнопка должна быть в теге button</b>
```html
<button type="submit" name="submit" class="s-button is-blicked" title="Отправить" value="Отправить">Отправить</button>
```

<b>2. Класс, который нужно добавить к кнопке</b>
```css
.is-blicked:after {
    content: "";
    position: absolute;
    top: 0;
    bottom: 0;
    height: 100%;
    background: linear-gradient(90deg,hsla(0,0%,100%,.1) 10%,hsla(0,0%,100%,.2) 20%,hsla(0,0%,100%,.6));
    width: 100px;
    -webkit-transform: skewX(-45deg);
    transform: skewX(-45deg);
    left: -20%;
    transition: all .6s ease;
    -webkit-animation-name: blick;
    animation-name: blick;
    -webkit-animation-duration: 6s;
    animation-duration: 6s;
    -webkit-animation-iteration-count: infinite;
    animation-iteration-count: infinite;
}
```

3. Фрейм анимации
```css
@-webkit-keyframes blick{
    15%, to {
        left:110%;
    }
}
@keyframes blick{
    15%, to {
        left:110%;
        }
}
```

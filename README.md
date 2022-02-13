# blick_button.css
Кнопка с эффектом блика


<b>1. Класс, который нужно добавить к кнопке</b>
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

2. Фрейм анимации
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

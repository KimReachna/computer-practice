---
## Front matter
title: "Отчёт по лабораторной работе №5"
subtitle: "Построение графиков"
author: "Ким Реачна"

## Generic otions
lang: ru-RU
toc-title: "Содержание"

## Bibliography
bibliography: bib/cite.bib
csl: pandoc/csl/gost-r-7-0-5-2008-numeric.csl

## Pdf output format
toc: true # Table of contents
toc-depth: 2
lof: true # List of figures
fontsize: 12pt
linestretch: 1.5
papersize: a4
documentclass: scrreprt
## I18n polyglossia
polyglossia-lang:
  name: russian
  options:
	- spelling=modern
	- babelshorthands=true
polyglossia-otherlangs:
  name: english
## I18n babel
babel-lang: russian
babel-otherlangs: english
## Fonts
mainfont: PT Serif
romanfont: PT Serif
sansfont: PT Sans
monofont: PT Mono
mainfontoptions: Ligatures=TeX
romanfontoptions: Ligatures=TeX
sansfontoptions: Ligatures=TeX,Scale=MatchLowercase
monofontoptions: Scale=MatchLowercase,Scale=0.9
## Biblatex
biblatex: true
biblio-style: "gost-numeric"
biblatexoptions:
  - parentracker=true
  - backend=biber
  - hyperref=auto
  - language=auto
  - autolang=other*
  - citestyle=gost-numeric
## Pandoc-crossref LaTeX customization
figureTitle: "Рис."
listingTitle: "Листинг"
lofTitle: "Список иллюстраций"
lolTitle: "Листинги"
## Misc options
indent: true
header-includes:
  - \usepackage{indentfirst}
  - \usepackage{float} # keep figures where there are in the text
  - \floatplacement{figure}{H} # keep figures where there are in the text
---

# Цель работы

Основная цель работы — освоить синтаксис языка Julia для построения графиков.

# Выполнение лабораторной работы

##   Основные пакеты для работы с графиками в Julia

- Установила все необходимые пакеты для работы с графиками:

![Установка все необходимые пакеты для работы с графиками](image/2.png){width=70% height=70%}

- Задала исходную функцию и построил первый график, перевела надписи на русский язык

![График функции $f(x)=(3x^2+6x-9)e^{-0,3x}$, при помощи gr()](image/3.png){width=70% height=70%}

![График функции $f(x)=(3x^2+6x-9)e^{-0,3x}$, при помощи pyplot()](image/4.png){width=70% height=70%}

- Построение графика при помощи plotly(). В начале вызываю необходимую библиотеку и с помощью функции plot() строю график.

![График функции $f(x)=(3x^2+6x-9)e^{-0,3x}$, при помощи plotly()](image/5.png){width=70% height=70%}

- Построение графика при помощи unicodeplots(). Так как использование просто в качестве бэкенда не сработало, вызываю функции из пакета.

![График функции $f(x)=(3x^2+6x-9)e^{-0,3x}$, при помощи unicodeplot()](image/6.png){width=70% height=70%}

## Опции при построении графика

Построила график синисуоиды, разложение ее в ряд Тейлора и сравнила результаты и красиво всё оформила:

![График функции $sin(𝑥)$](image/7.png){width=70% height=70%}

![График функции разложения исходной функции в ряд Тейлора](image/8.png){width=70% height=70%}

![Графики исходной функции и её разложения в ряд Тейлора](image/9.png){width=70% height=70%}

![Вид графиков после добавления опций при их построении](image/10.png){width=70% height=70%}

![Вид графиков после добавления опций при их построении](image/taylor.png){width=70% height=70%}

![Сохранение построенного графика](image/11.png){width=70% height=70%}

## Точечный график

###  Простой точечный график

![ График десяти случайных значений на плоскости](image/12.png){width=70% height=70%}

### Точечный график с кодированием значения размером точки

![ График пятидесяти случайных значений на плоскости с различными опциями отображения](image/13.png){width=70% height=70%}

###  3-мерный точечный график с кодированием значения размером точки

![График пятидесяти случайных значений в пространстве с различными опциями отображения](image/14.png){width=70% height=70%}

##  Аппроксимация данных

![Пример функции](image/15.png){width=70% height=70%}

![Пример аппроксимации исходной функции полиномом 5-й степени](image/16.png){width=70% height=70%}

##  Две оси ординат

![Пример отдельно построенной траектории](image/17.png){width=70% height=70%}

![Пример двух траекторий на одном графике с двумя осями ординат](image/18.png){width=70% height=70%}

## Полярные координаты

![График функции, заданной в полярных координатах](image/19.png){width=70% height=70%}

## Параметрический график

###  Параметрический график кривой на плоскости

![Параметрический график кривой на плоскости](image/20.png){width=70% height=70%}

### Параметрический график кривой в пространстве

![Параметрический график кривой в пространстве](image/21.png){width=70% height=70%}

## График поверхности

![График поверхности использована функция surface()](image/22.png){width=70% height=70%}

![График поверхности использована функция plot()](image/23.png){width=70% height=70%}

![Сглаженный график поверхности](image/24.png){width=70% height=70%}

![График поверхности с изменённым углом зрения](image/25.png){width=70% height=70%}

## Линии уровня

![График поверхности, заданной функцией $g(x,y)=(3x+y^2)|sin(x)+cos(y)|$](image/26.png){width=70% height=70%}

![Линии уровня](image/27.png){width=70% height=70%}

![Линии уровня с заполнением](image/28.png){width=70% height=70%}

##  Векторные поля

![График функции $h(x,y)=x^3-3x+y^2$](image/29.png){width=70% height=70%}

![Линии уровня для функции $h(x,y)=x^3-3x+y^2$](image/30.png){width=70% height=70%}

![ Векторное поле функции $h(x,y)=x^3-3x+y^2$](image/31.png){width=70% height=70%}

![Векторное поле функции $h(x,y)=x^3-3x+y^2$ скорректирована область видимости](image/32.png){width=70% height=70%}

## Анимация

###  Gif-анимация

![Статичный график поверхности](image/33.png){width=70% height=70%}

![Анимированный график поверхности](image/34.png){width=70% height=70%}

### Гипоциклоида

![Большая окружность гипоциклоиды](image/35.png){width=70% height=70%}

![Половина пути гипоциклоиды](image/36.png){width=70% height=70%}

![Малая окружность гипоциклоиды](image/37.png){width=70% height=70%}

![Малая окружность гипоциклоиды с добавлением радиуса](image/38.png){width=70% height=70%}

![Анимация движения гипоциклоиды](image/39.png){width=70% height=70%}

![Анимация движения гипоциклоиды](image/40.png){width=70% height=70%}

## Errorbars

![График исходных значений](image/41.png){width=70% height=70%}

![График исходных значений с отклонениями](image/42.png){width=70% height=70%}

![Поворот графика](image/43.png){width=70% height=70%}

![Заполнение цветом](image/44.png){width=70% height=70%}

![График ошибок по двум осям](image/45.png){width=70% height=70%}

![График асимметричных ошибок по двум осям](image/46.png){width=70% height=70%}

## Использование пакета Distributions

![Установка пакета Distributions](image/47.png){width=70% height=70%}

![Гистограмма, построенная по массиву случайных чисел](image/48.png){width=70% height=70%}

![Гистограмма нормального распределения](image/49.png){width=70% height=70%}

![Гистограмма распределения людей по возрастам](image/50.png){width=70% height=70%}

## Подграфики

![Серия из 4-х графиков в ряд](image/51.png){width=70% height=70%}

![Серия из 4-х графиков в сетке](image/52.png){width=70% height=70%}

![Серия из 4-х графиков разной высоты в ряд](image/53.png){width=70% height=70%}

![Объединение нескольких графиков в одной сетке](image/54.png){width=70% height=70%}

![Разнообразные варианты представления данных](image/55.png){width=70% height=70%}

![Демонстрация применения сложного макета для построения графиков](image/56.png){width=70% height=70%}

##  Задания для самостоятельного выполнения

1. Постройте все возможные типы графиков (простые, точечные, гистограммы и т.д.) функции $y=sin(x), x=\overline {0,2\pi}$, Отобразите все графики в одном графическом окне.

![Разные типы графиков
](image/57.png){width=80% height=80%}

2. Постройте графики функции $y=sin(x), x=\overline {0,2\pi}$ со всеми возможными (сколько сможете вспомнить) типами оформления линий графика. Отобразите все графики в одном графическом окне

![Разные линии](image/58.png){width=80% height=80%}

![Разные линии](image/59.png){width=80% height=80%}


3. Постройте график функции $y(x)=\pi x^2ln(x)$, назовите оси соответственно. Пусть цвет рамки будет зелёным, а цвет самого графика — красным. Задайте расстояние между надписями и осями так, чтобы надписи полностью умещались в графическом окне. Задайте шрифт надписей. Задайте частоту отметок на осях координат

![График заданной функции](image/60.png){width=80% height=80%}

4. Задайте вектор $x=(-2,-1,0,1,2)$.  В одном графическом окне (в 4-х подокнах) изобразите графически по точкам $𝑥$ значения функции $y(x)=x^3-3x$ в виде: 
- точек,
- линий,
- линий и точек,
- кривой

![График заданного вектора](image/61.png){width=80% height=80%}

![График заданного вектора](image/figure_kim.png){width=80% height=80%}

Сохраните полученные изображения в файле ```figure_familiya.png```, где вместо familiya укажите вашу фамилию.

![Сохраните полученные изображения](image/87.png)

5. Задайте вектор $x=(3,3.1,3.2,...,,6)$. Постройте графики функций $y_1(x)=\pi x$ и $y_2(x)=exp(x)cos(x)$ в указанном диапазоне значений аргумента $𝑥$ следующим образом:

![График фунции](image/63.png){width=80% height=80%}

![График фунции с двумя осями координат](image/64.png){width=80% height=80%}

6. Постройте график некоторых экспериментальных данных (придумайте сами), учитывая ошибку измерения.

![Построение графика некоторых экспериментальных данных](image/65.png){width=80% height=80%}

7. Постройте точечный график случайных данных. Подпишите оси, легенду, название графика.

![Точечный график случайных данных](image/66.png){width=80% height=80%}

8. Постройте 3-мерный точечный график случайных данных. Подпишите оси, легенду, название графика.

![3D Точечный график случайных данных](image/67.png){width=80% height=80%}

9. Создайте анимацию с построением синусоиды. То есть вы строите последовательность графиков синусоиды, постпенно увеличивая значение аргумента. После соедините их в анимацию.

![Анимация Синусоида](image/68.png){width=80% height=80%}

10. Постройте анимированную гипоциклоиду для 2 целых значений модуля $𝑘$ и 2 рациональных значений модуля $𝑘$

![Гипоциклоида](image/69.png){width=80% height=80%}

![](image/71.png){width=80% height=80%}

![Гипоциклоидная анимация](image/70.png){width=80% height=80%}

![](image/72.png){width=80% height=80%}

![Гипоциклоидная анимация](image/73.png){width=80% height=80%}

![](image/74.png){width=80% height=80%}

![Гипоциклоидная анимация](image/75.png){width=80% height=80%}

![](image/76.png){width=80% height=80%}

![Гипоциклоидная анимация](image/hypocycloid.gif)

11. Постройте анимированную эпициклоиду для 2 целых значений модуля $𝑘$ и 2 рациональных значений модуля $𝑘$.

![Эпициклоида](image/78.png){width=80% height=80%}

![](image/79.png){width=80% height=80%}

![Эпициклоидная анимация](image/80.png){width=80% height=80%}

![](image/81.png){width=80% height=80%}

![Эпициклоидная анимация](image/82.png){width=80% height=80%}

![](image/83.png){width=80% height=80%}

![Эпициклоидная анимация](image/84.png){width=80% height=80%}

![](image/85.png){width=80% height=80%}

![Эпициклоидная анимация](image/epicycloid.gif)

# Листинги  программы

```julia
using Pkg
Pkg.add("Plots")
Pkg.add("PyPlot")
Pkg.add("Plotly")
Pkg.add("UnicodePlots")
# подключаем для использования Plots:
using Plots
Построение графика функции
# задание функции:
f(x) = (3x.^2 + 6x .- 9).*exp.(-0.3x)
# генерирование массива значений x в диапазоне от -5 до 10 с шагом 0,1
# (шаг задан через указание длины массива):
x = collect(range(-5,10,length=151))
# генерирование массива значений y:
y = f(x)
# указывается, что для построения графика используется gr():
gr()
# задание опций при построении графика
# (название кривой, подписи по осям, цвет графика):
plot(x,y,
    title="A simple curve",
    xlabel="Variable x",
    ylabel="Variable y",
    color="blue")
using Plots
# указывается, что для построения графика используется pyplot():
pyplot()
# задание опций при построении графика
# (название кривой, подписи по осям, цвет графика):
plot(x,y,
    title="Простая кривая",
    xlabel="Переменная x",
    ylabel="Переменная y",
    color="blue")
using Plots
# указывается, что для построения графика используется plotly():
plotly()
# задание опций при построении графика
# (название кривой, подписи по осям, цвет графика):
plot(x,y,
    title="Простая кривая",
    xlabel="Переменная x",
    ylabel="Переменная y",
    color="blue")
# using Plots
# unicodeplots()
using UnicodePlots #т.к. использование просто в качестве бэкенда не сработало, вызываю функции собственно пакета
# задание опций при построении графика
# (название кривой, подписи по осям, цвет графика):
lineplot(x, y,
    title="Простая кривая",
    xlabel="Переменная x",
    ylabel="Переменная y",
    color= :blue)
# рассмотрим дополнительные возможности пакетов для работы с графиками
using Plots
# указывается, что для построения графика используется pyplot():
pyplot()
# задание функции sin(x):
sin_theor(x) = sin(x)
​
# построение графика функции sin(x):
plot(sin_theor)
pyplot()
sin_taylor(x) = [(-1)^i*x^(2*i+1)/factorial(2*i+1) for i in 0:4] |> sum
# построение графика функции sin_taylor(x):
plot(sin_taylor)
# построение двух функций на одном графике:
plot(sin_theor)
plot!(sin_taylor)
plot(
    # функция sin(x):
    sin_taylor,
    # подпись в легенде, цвет и тип линии:
    label = "sin(x), разложение в ряд Тейлора",
    line=(:blue, 0.3, 6, :solid),
    # размер графика:
    size=(800, 500),
    # параметры отображения значений по осям
    xticks = (-5:0.5:5),
    yticks = (-1:0.1:1),
    xtickfont = font(12, "Times New Roman"),
    ytickfont = font(12, "Times New Roman"),
    # подписи по осям:
    ylabel = "у",
    xlabel = "x",
    # название графика:
    title = "Разложение в ряд Тейлора",
    # поворот значений, заданный по оси x:
    xrotation = rad2deg(pi/4),
    # заливка области графика цветом:
    fillrange = 0,
    fillalpha = 0.5,
    fillcolor = :lightgoldenrod,
    # задание цвета фона:
    background_color = :ivory
)
plot!(
    # функция sin_theor:
    sin_theor,
    # подпись в легенде, цвет и тип линии:
    label = "sin(x), теоретическое значение",
    leg=:topright,
    line=(:black, 1.0, 2, :dash)
)
# сохранение графика в файле в формате pdf или png:
Plots.savefig("taylor.pdf")
Plots.savefig("taylor.png")
# параметры распределения точек на плоскости:
x = range(1,10,length=10)
y = rand(10)
# параметры построения графика:
plot(x, y,
    seriestype = :scatter,
    title = "Точечный график", 
    xlabel = "x",
    ylabel = "у",
    # подпись в легенде, цвет и тип линии:
    label = "y1, теоретическое значение",
    leg = :topright
)
# параметры распределения точек на плоскости:
n = 50
x = rand(n)
y = rand(n)
ms = rand(50) * 30
# параметры построения графика:
scatter(x, y, 
    markersize=ms, 
    # подписи по осям:
    xlabel = "x",
    ylabel = "у",
    # подпись в легенде, цвет и тип линии:
    label = "y1, теоретическое значение",
    title = "Точечный график")
# параметры распределения точек в пространстве:
n = 50
x = rand(n)
y = rand(n)
z = rand(n)
ms = rand(50) * 30
# параметры построения графика:
scatter(x, y, z, 
    markersize=ms,
    xlabel = "x",
    ylabel = "у",
    zlabel = "z",
    # подпись в легенде, цвет и тип линии:
    label = "sin(x), теоретическое значение",
    title = "Точечный график")
5.2.4. Аппроксимация данных
# массив данных от 0 до 10 с шагом 0.01:
x = collect(0:0.01:9.99)
# экспоненциальная функция со случайным сдвигом значений:
y = exp.(ones(1000)+x) + 4000*randn(1000)
# построение графика:
scatter(x,y,markersize=3,alpha=.8,legend=false)
# определение массива для нахождения коэффициентов полинома:
A = [ones(1000) x x.^2 x.^3 x.^4 x.^5]
# решение матричного уравнения:
c = A\y
# построение полинома:
f1 = c[1]*ones(1000) + c[2]*x + c[3]*x.^2 + c[4]*x.^3 + c[5]*x.^4 + c[6]*x.^5
​
# построение графика аппроксимирующей функции:
plot!(x, f1, linewidth=3, color=:red)
using Plots.PlotMeasures
# пример случайной траектории
# (заданы обозначение траектории, легенда вверху справа, без сетки)
plot(randn(100),
    xlabel = "X",
    ylabel="y1",
    label = "1st path",
    leg=:topright,
    grid = :off,
    right_margin = 20mm
)
# пример добавления на график второй случайной траектории
# (задано обозначение траектории и её цвет, легенда снизу справа, без сетки)
# задана рамка графика
plot!(twinx(), randn(100)*10,
    c=:red,
    ylabel="y2",
    label = "2nd path",
    leg=:bottomright,
    grid = :off,
    box = :on,
    size=(600, 400)
)
# функция в полярных координатах:
r(tetha) = 1 + cos(tetha) * sin(tetha)^2
# полярная система координат:
tetha = range(0, stop=2π, length=50)
# график функции, заданной в полярных координатах:
plot(tetha, r.(tetha),
    proj=:polar,
    lims=(0,1.5)
)
# параметрическое уравнение:
x1(t) = sin(t)
y1(t) = sin(2t)
# построение графика:
plot(x1, y1, 0, 2π, leg=false, fill=(0,:orange))
# параметрическое уравнение
t = range(0, stop=10, length=1000)
x = cos.(t)
y = sin.(t)
z = sin.(5t)
# построение графика:
plot(x, y, z)
# построение графика поверхности:
f(x,y) = x^2 + y^2
x = -10:10
y = x
surface(x, y, f)
# построение графика поверхности:
f(x,y) = x^2 + y^2
x = -10:10
y = x
plot(x, y, f,
    linetype=:wireframe
)
f2(x,y) = x^2 + y^2
x = -10:0.1:10
y = x
plot(x, y, f2,
linetype = :surface
)
x = range(-2,stop=2,length=100)
y = range(sqrt(2),stop=2,length=100)
f3(x,y) = x*y-x-y+1
plot(x, y, f3,
    linetype = :surface,
    c=cgrad([:red,:blue]),
    camera=(-30,30),
)
5.2.9. Линии уровня
x = 1:0.5:20
y = 1:0.5:10
g(x, y) = (3x + y ^ 2) * abs(sin(x) + cos(y))
plot(x, y, g,
    linetype = :surface,
)
contour(x, y, g)
p = contour(x, y, g,
fill=true)
plot(p)
# определение переменных:
X0 = range(-2, stop=2, length=100)
Y0 = range(-2, stop=2, length=100)
# определение функции:
h(x, y) = x^3 - 3x + y^2
# построение поверхности:
plot(X0, Y0, h,
    linetype = :surface
)
# построение линий уровня:
contour(X0, Y0, h)
# градиент:
xs = range(-2, stop=2, length=12)
ys = range(-2, stop=2, length=12)
# производная от исходной функции:
dh(x, y) = [3x^2-3; 2y]/25
xxs = [x for x in xs for y in ys]
yys = [y for x in xs for y in ys]
​
quiver!(xxs, yys, quiver=dh, c=:blue)
# коррекция области видимости графика:
xlims!(-2, 2)
ylims!(-2, 2)
quiver!(xxs, yys, quiver=dh, c=:blue)
pyplot()
# построение поверхности:
i = 0
X = Y = range(-5,stop=5,length=40)
surface(X, Y, (x,y) -> sin(x+10sin(i))+cos(y))
# анимация:
X = Y = range(-5, stop=5, length=40)
@gif for i in range(0, stop=2π, length=100)
surface(X, Y, (x, y) -> sin(x + 10sin(i)) + cos(y))
end
# радиус малой окружности:
r1 = 1
# коэффициент для построения большой окружности:
k = 3
# число отсчётов:
n = 100
# массив значений угла tetha:
# theta from 0 to 2pi ( + a little extra)
tetha = collect(0:2*π/100:2*π+2*π/100)
# массивы значений координат:
X = r1*k*cos.(tetha)
Y = r1*k*sin.(tetha)
# задаём оси координат:
plt = plot(5, xlim=(-4,4), ylim=(-4,4), c=:red, aspect_ratio=1, 
legend=false, framestyle=:origin)
# большая окружность:
plot!(plt, X,Y, c=:blue, legend=false)
i = 50
t = tetha[1:i]
# гипоциклоида:
x = r1*(k-1)*cos.(t) + r1*cos.((k-1)*t)
y = r1*(k-1)*sin.(t) - r1*sin.((k-1)*t)
plot!(x,y, c=:red)
# малая окружность:
xc = r1*(k-1)*cos(t[end]) .+ r1*cos.(tetha)
yc = r1*(k-1)*sin(t[end]) .+ r1*sin.(tetha)
plot!(xc,yc,c=:black)
# радиус малой окружности:
xl = transpose([r1*(k-1)*cos(t[end]) x[end]])
yl = transpose([r1*(k-1)*sin(t[end]) y[end]])
plot!(xl, yl, markershape=:circle, markersize=4, c=:black)
scatter!([x[end]], [y[end]], c=:red, markerstrokecolor=:red)
anim = @animate for i in 1:n
# задаём оси координат:
plt=plot(5, xlim=(-4,4), ylim=(-4,4), c=:red, aspect_ratio=1, legend=false, framestyle=:origin)
# большая окружность:
plot!(plt, X, Y, c=:blue, legend=false)
t = tetha[1:i]
    
# гипоциклоида:
x = r1*(k-1)*cos.(t) + r1*cos.((k-1)*t)
y = r1*(k-1)*sin.(t) - r1*sin.((k-1)*t)
plot!(x,y, c=:red)
    
# малая окружность:
xc = r1*(k-1)*cos(t[end]) .+ r1*cos.(tetha)
yc = r1*(k-1)*sin(t[end]) .+ r1*sin.(tetha)
plot!(xc, yc, c=:black)
    
# радиус малой окружности:
xl = transpose([r1*(k-1)*cos(t[end]) x[end]])
yl = transpose([r1*(k-1)*sin(t[end]) y[end]])
plot!(xl,yl,markershape=:circle, markersize=4, c=:black)
scatter!([x[end]], [y[end]], c=:red, markerstrokecolor=:red)
end
​
gif(anim,"hypocycloid.gif")
using Statistics
sds = [1, 1/2, 1/4, 1/8, 1/16, 1/32]
n = 10
y = [mean(sd*randn(n)) for sd in sds]
errs = 1.96 * sds / sqrt(n)
plot(y,
    ylims = (-1,1),
)
plot(y,
ylims = (-1,1),
err = errs
)
plot(y, 1:length(y),
    xerr = errs,
    marker = stroke(3,:orange)
)
plot(y,
    ribbon=errs,
    fill=:cyan
)
n = 10
x = [(rand()+1) .* randn(n) .+ 2i for i in 1:5]
y = [(rand()+1) .* randn(n) .+ i for i in 1:5]
f(v) = 1.96std(v) / sqrt(n)
xerr = map(f, x)
yerr = map(f, y)
x = map(mean, x)
y = map(mean, y)
plot(x, y,
    xerr = xerr,
    yerr = yerr,
    marker = stroke(2, :orange)
)
plot(x, y,
    xerr = (0.5xerr,2xerr),
    yerr = (0.5yerr,2yerr),
    marker = stroke(2, :orange)
)
import Pkg
Pkg.add("Distributions")
using Distributions
pyplot()
ages = rand(15:55, 1000)
histogram(ages)
d = Normal(35.0, 10.0)
ages = rand(d, 1000)
histogram(
    ages,
    label="Распределение по возрастам (года)",
    xlabel = "Возраст (лет)",
    ylabel= "Количество"
)
plotly()
d1=Normal(10.0,5.0);
d2=Normal(35.0,10.0);
d3=Normal(60.0,5.0);
N=1000;
ages = (Float64)[];
ages = append!(ages,rand(d1,Int64(ceil(N/2))));
ages = append!(ages,rand(d2,N));
ages = append!(ages,rand(d3,Int64(ceil(N/3))));
histogram(
    ages,
    bins=50,
    label="Распределение по возрастам (года)",
    xlabel = "Возраст (лет)",
    ylabel= "Количество",
    title = "Распределение по возрастам (года)"
)
5.2.14. Подграфики
# подгружаем pyplot():
pyplot()
# построение серии графиков:
x=range(-2,2,length=10)
y = rand(10,4)
plot(x,y,
    layout=(4,1)
)
plot(x,y,
layout=4
)
plot(x,y,
    size=(600,300),
    layout = grid(4,1,heights=[0.2,0.3,0.4,0.15])
)
# график в виде линий:
p1 = plot(x,y)
# график в виде точек:
p2 = scatter(x,y)
# график в виде линий с оформлением:
p3 = plot(x,y[:,1:2],xlabel="Labelled plot of two columns",lw=2,title="Wide lines")
# 4 гистограммы:
p4 = histogram(x,y)
​
plot(
    p1,p2,p3,p4,
    layout=(2,2),
    legend=false,
    size=(800,600),
    background_color = :ivory
)
seriestypes = [:stephist, :sticks, :bar, :hline, :vline, :path]
titles =["stephist" "sticks" "bar" "hline" "vline" "path"]
plot(rand(20,1), st = seriestypes,
    layout = (2,3),
    ticks=nothing,
    legend=false,
    title=titles,
    m=3
)
l = @layout [ a{0.3w} [grid(3,3)
b{0.2h} ]]
plot(
    rand(10,11),
    layout = l, legend = false, seriestype = [:bar :scatter :path],
    title = ["($i)" for j = 1:1, i=1:11], titleloc = :right, titlefont = font(8)
)
f4(x) = sin.(x)
# сгенерируем масссив значений x в диапазоне от 0 до П
x = collect(range(0, 2*pi, length=200))
# зададим функцию
y = f4(x)
​
fig1 = plot(x, y, 
    title="Simple graphic", 
    xlabel="X", 
    ylabel="Y", 
    color="red")
fig2 = scatter(x, y, 
    title="Point graphic", 
    xlabel="X", 
    ylabel="Y", 
    color="red")
fig3 = histogram(f4(x), 
    title="Histogram", 
    xlabel="X", 
    ylabel="Y", 
    color="purple")
fig4 = histogram(f4(x),
    bins = 10,
    title="Histogram (bins=10)", 
    xlabel="X", 
    ylabel="Y", 
    color="green")
plot(fig1, fig2, fig3, fig4, layout=(2, 2), legends=false, size=(800, 600))
f4(x) = sin.(x)
# сгенерируем масссив значений x в диапазоне от 0 до П с шагом 0.1
x = collect(range(0, 2*pi, length=200))
# зададим функцию
y = f4(x)
​
fig1 = plot(x, y, 
    title="Solid Line",
    line = (:blue, 0.2, 5, :solid),
    xlabel="X", 
    ylabel="Y")
fig2 = plot(x, y, 
    title="Dash Line",
    line = (:blue, 0.2, 5, :dash),
    xlabel="X", 
    ylabel="Y")
fig3 = plot(x, y,
    line = (:green, 0.2, 5, :dot),
    title="Dot Line", 
    xlabel="X", 
    ylabel="Y")
fig4 = plot(x, y,
    line = (:green, 0.2, 5, :dashdot),
    title="Dash and Dot Line", 
    xlabel="X", 
    ylabel="Y")
fig5 = plot(x, y,
    line = (:blue, 0.2, 5, :scatter),
    title="Scatter Line", 
    xlabel="X", 
    ylabel="Y")
fig6 = plot(x, y,
    line = (:blue, 0.2, 5, :auto),
    title="Auto Line", 
    xlabel="X", 
    ylabel="Y")
plot(fig1, fig2, fig3, fig4, fig5, fig6, layout=(3, 2), 
legends=false, size=(800, 600))
using Plots.PlotMeasures
f5(x) = (pi*x.^2).*log.(x)
# сгенерируем масссив значений x в диапазоне от 0 до 2П
x = collect(range(0, 2*pi, length=200))
# зададим функцию
y = f5(x)
plotly()
plot(x,y, color="red", box = :on, foreground_color="green",
    xaxis = ("Ось x", (0, 6.5), 6.5:-0.5:0), yaxis = ("Ось y", 
    (0, 250), 250:-25:0),
    leg=:right,
    title="График функции (задание №3)", 
    titlefont = (15, "montserrat", :black),
    top_margin = 10mm,
    right_margin = 5mm,
    legendfontsize = 8, 
    guidefont = (12, "montserrat", :black), 
    tickfont = (8, "montserrat",:black),
    xrotation = 90)
# зададим функцию
f(x) = x.^3 - 3*x
x = [-2, -1, 0, 1, 2]
y = f(x)
using Plots.PlotMeasures
pyplot()
fig1 = scatter(x, y, 
    title="Point graphic", 
    xlabel="X", 
    ylabel="Y", 
    color="green")
fig2 = plot(x, y, 
    title="Sticks graphic",
    seriestype = :sticks,
    xlabel="X", 
    ylabel="Y", 
    color="red")
fig3 = plot(x, y, 
    title="Step graphic",
    marker = '.',
    seriestype = :step,
    xlabel="X", 
    ylabel="Y", 
    color="purple")
fig4 = plot(x, y,
    title="Simple graphic", 
    xlabel="X", 
    ylabel="Y", 
    color="blue")
plot(fig1, fig2, fig3, fig4, layout=(2, 2), legends=false, 
size=(800, 600))
# Сохраню полученное изображение
savefig("figure_solomko.png")

f_1(x) = pi*x
f_2(x) = exp.(x).*cos.(x)
x = [i for i in 3:0.1:6]
y_1 = f_1(x)
y_2 = f_2(x)
​
pyplot()
plot(x, y_1, 
    title="График функций (Задание №5)", 
    xlabel="X", 
    ylabel="Y", 
    leg=:topleft,  
    color="blue",  
    grid = (:y, :orange, :dot),
    right_margin = 20mm)
​
plot!(x, y_2, 
    color="purple", 
    leg=:bottomright, 
    grid = :on, 
    box = :on)
plot(x, y_1, 
    title="График функций (Задание №5)", 
    xlabel="X", 
    ylabel="Y1", 
    leg=:topleft,  
    color="blue",  
    grid = (:y, :orange, :dot),
    right_margin = 20mm)
​
plot!(twinx(), x, y_2, 
    ylabel = "Y2",
    color="purple", 
    leg=:bottomright, 
    grid = :on, 
    box = :on)

f_3(x) = x.^2 - 2*x
x = rand(20)
y_3 = f_3(x)
n = 20
error = 1.23 * y_3 / sqrt(n)
plot(y_3, ylims=(-5, 5), err = error)
x = rand(20)
y = rand(20)
scatter(x, y,
    title = "Точечный график случайных чисел",
    label = "Точки (x; y)",
    leg = :topright,
    xlabel="X", 
    ylabel="Y")
x = rand(50)
y = rand(50)
z = rand(50)
scatter(x, y, z,
    xlabel = "x",
    ylabel = "у",
    zlabel = "z",
    label = "Точки (x; y; z)",
    title = "Точечный 3D-график")
n = 300
x = collect(0*pi : 2*pi/100 : 10*pi+pi/100)
anim = @animate for i in 1:n
    fig = plot(1,
                xlim=(0, 10),
                ylim=(-2, 2), 
                c=:purple, 
                aspect_ratio=1,
                legend=false, 
                framestyle=:origin)
    step = x[1 : i]
    y = sin.(step)
    plot!(step, y)
end
#Сохранила анимацию в gif-файл
gif(anim, "sinusoida.gif")

function hypocycloid(x, r0, n)
    # радиус малой окружности:
    r0 = r0
    # коэффициент для построения большой окружности:
    k = x
    # число отсчётов:
    count = n
    # массив значений угла tetha:
    tetha = collect(0: 2*π/100 : 10*π+2*π/count)
    
    # массивы значений координат:
    x_1 = r0 * k * cos.(tetha)
    y_1 = r0 * k * sin.(tetha)
    #В конце сделаем анимацию получившегося изображения
    anim = @animate for i in 1:count
        # задаём оси координат:
        plt=plot(5, 
            xlim=(-k-1, k+1),
            ylim=(-k-1, k+1), 
            color=:red, 
            aspect_ratio=1,
            legend=false, 
            framestyle=:origin)
        # большая окружность:
        plot!(plt, x_1, y_1, c=:blue, legend=false)
        t = tetha[1 : i]
        
        # гипоциклоида:
        x = r0 * (k-1) * cos.(t) + r0 * cos.((k-1) * t)
        y = r0 * (k-1) * sin.(t) - r0 * sin.((k-1) * t)
        plot!(x,y, color=:purple)
        
        # малая окружность:
        x_r0 = r0*(k-1)*cos(t[end]) .+ r0*cos.(tetha)
        y_r0 = r0*(k-1)*sin(t[end]) .+ r0*sin.(tetha)
        plot!(x_r0, y_r0, color=:red)
        
        # радиус малой окружности:
        xl_r0 = transpose([r0*(k-1)*cos(t[end]) x[end]])
        yl_r0 = transpose([r0*(k-1)*sin(t[end]) y[end]])
        plot!(xl_r0, yl_r0, 
            markershape=:circle,
            markersize=4,
            color=:black)
        scatter!([x[end]],
            [y[end]],
            color=:red, 
            markerstrokecolor=:red)
    end
    gif(anim,"hypocycloid.gif")
end
# первый вариант
hypocycloid(4, 1, 100)
# второй вариант
hypocycloid(5, 1, 100)
# третий вариант
hypocycloid(1.5, 1, 200)
# четвертый вариант
hypocycloid(5.5, 1, 200)

function epicycloid(x, r0, n)
    # радиус малой окружности:
    r0 = r0
    # коэффициент для построения большой окружности:
    k = x
    # число отсчётов:
    count = n
    # массив значений угла tetha:
    tetha = collect(0: 2*π/100 : 10*π+2*π/count)
    
    # массивы значений координат:
    x_1 = r0 * k * cos.(tetha)
    y_1 = r0 * k * sin.(tetha)
    #В конце сделаем анимацию получившегося изображения
    anim = @animate for i in 1:count
        # задаём оси координат:
        plt=plot(5, 
            xlim=(-2*r0*k*2, 2*r0*k*2),
            ylim=(-2*r0*k*2, 2*r0*k*2), 
            color=:red, 
            aspect_ratio=1,
            legend=false, 
            framestyle=:origin)
        # большая окружность:
        plot!(plt, x_1, y_1, c=:blue, legend=false)
        t = tetha[1 : i]
        
        # гипоциклоида:
        x = r0 * (k + 1) * cos.(t) - r0 * cos.((k + 1) * t)
        y = r0 * (k + 1) * sin.(t) - r0 * sin.((k + 1) * t)
        plot!(x,y, color=:purple)
        
        # малая окружность:
        x_r0 = r0*(k + 1)*cos(t[end]) .- r0*cos.(tetha)
        y_r0 = r0*(k + 1)*sin(t[end]) .- r0*sin.(tetha)
        plot!(x_r0, y_r0, color=:red)
        
        # радиус малой окружности:
        xl_r0 = transpose([r0*(k + 1)*cos(t[end]) x[end]])
        yl_r0 = transpose([r0*(k + 1)*sin(t[end]) y[end]])
        plot!(xl_r0, yl_r0, 
            markershape=:circle,
            markersize=4,
            color=:black)
        scatter!([x[end]],
            [y[end]],
            color=:red, 
            markerstrokecolor=:red)
    end
    gif(anim,"epicycloid.gif")
end
# первый вариант
epicycloid(2, 1, 100)
# второй вариант
epicycloid(3, 1, 100)
# третий вариант
epicycloid(5.5, 1, 500)
# четвертый вариант
epicycloid(3.8, 1, 500)
# четвертый вариант
epicycloid(3.8, 1, 500)
```

# Вывод

Освоила синтаксис языка Julia для построения графиков.

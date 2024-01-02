---
## Front matter
title: "Отчёт по лабораторной работе №7"
subtitle: "Введение в работу с данными"
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

Основной целью работы является специализированных пакетов Julia для обработки данных.

# Выполнение лабораторной работы

##   Julia для науки о данных

###  Считывание данных

![Установка пакетов для будущей работы](image/1.png){width=80% height=80%}

![Примеры считывания данных](image/2.png){width=80% height=80%}

![Примеры считывания данных](image/3.png){width=80% height=80%}

###  Запись данных в файл

![Примеры записи данных в файл](image/4.png){width=80% height=80%}

###  Словари

![Примеры словаря](image/5.png){width=80% height=80%}

### DataFrames

![Примеры DataFrames](image/6.png){width=80% height=80%}

![Примеры DataFrames](image/7.png){width=80% height=80%}

###  RDatasets

![Примеры RDatesets](image/8.png){width=80% height=80%}

![Примеры RDatesets](image/9.png){width=80% height=80%}

### Работа с переменными отсутствующего типа (Missing Values)

![Примеры работы с Missing Values](image/10.png){width=80% height=80%}

![Примеры работы с Missing Values](image/11.png){width=80% height=80%}

### FileIO

![Установка пакет FileIO](image/12.png){width=80% height=80%}

![Примеры FileIO](image/13.png){width=80% height=80%}

##  Обработка данных: стандартные алгоритмы машинного обучения в Julia 

### Кластеризация данных. Метод k-средних

![Примеры кластеризации метода k-средних](image/14.png){width=80% height=80%}

![График цен на недвижимость в зависимости от площади](image/15.png){width=80% height=80%}

![График цен на недвижимость в зависимости от площади (исключены артефакты данных)](image/16.png){width=80% height=80%}

![Примеры кластеризации метода k-средних](image/17.png){width=80% height=80%}

![Примеры кластеризации метода k-средних](image/18.png){width=80% height=80%}

![Примеры кластеризации метода k-средних](image/19.png){width=80% height=80%}

![Пример кластеризации объектов недвижимости по географическому расположению](image/20.png){width=80% height=80%}

![Пример кластеризации объектов недвижимости по почтовому индексу](image/21.png){width=80% height=80%}

###  Кластеризация данных. Метод k ближайших соседей

![Примеры кластеризации метода k ближайших соседей](image/22.png){width=80% height=80%}

![График определение соседей объекта недвижимости](image/23.png){width=80% height=80%}

###  Обработка данных. Метод главных компонент

![Примеры метода главных компонент](image/24.png){width=80% height=80%}

![Примеры метода главных компонент](image/25.png){width=80% height=80%}

![Определение главных компонент для данных по объектам недвижимости](image/26.png){width=80% height=80%}

###  Обработка данных. Линейная регрессия

![Исходные данные](image/27.png){width=80% height=80%}

![Линейная регрессия](image/28.png){width=80% height=80%}

![Примеры линейная регрессия](image/29.png){width=80% height=80%}

## Задания для самостоятельного выполнения

###  Кластеризация

- Загрузка данных

![Загрузка данных](image/30.png){width=80% height=80%}

- Для кластеризации выбираются 2 атрибута - SepalLength и PetalLength и построение точечного графика их распределения в начале:

![График распределения признаков SepalLength и PetalLength](image/31.png){width=80% height=80%}

- Добавим данные в новый фрейм:

![Добавление данных в новый фрейм](image/32.png){width=80% height=80%}

- Преобразуем данные в матричный видб транспонируем и выдвигаем гипотезу, что эти признаки могут зависеть от типа радужной оболочки.
Поэтому подсчитаем количество уникальных видов и возьмем это количество кластеров.

![Преобразование данных и транспонирование](image/33.png){width=80% height=80%}

- Создание фрейма данных с указанием кластера, построение графика датафрейма с распределением цветов по кластерам и построение графиков с распределением цветов по самому виду Ирисов:

![Создание фрейма данных с указанием кластера](image/34.png){width=80% height=80%}

![График Iris с цветовой кодировкой по кластеру](image/35.png){width=80% height=80%}

![График Iris color-coded by species](image/36.png){width=80% height=80%}

###  Регрессия (метод наименьших квадратов в случае линейной регрессии)

**Часть 1**: Пусть регрессионная зависимость является линейной. Матрица наблюдений
факторов $𝑋$ имеет размерность $𝑁 × 3$ randn $(N, 3)$, массив результатов $𝑁 × 1$, регрессионная зависимость является линейной. Найдите МНК-оценку для линейной модели:

- Записываем данные, затем реализуем функцию linear_regression_model, которая изначально создает матрицу X2, состоящую из единиц. Далее присоединяю этот столбец к X. А затем решаю систему линейных уравнений.

![Данные и функция для решения систем уравнений](image/37.png){width=80% height=80%}

Результат решения линейных уравнений : $-0.000628618$.

- Сравню полученные результаты с результатами использования llsq из MultivariateStats.jl и с результатами использования регулярной регрессии наименьших квадратов из GLM.jl. После установки пакета создадим датафрейм, в который запишем y и разобьем X на 3 столбца - x1, x2 и x3.

![Установка необходимый пакет и создаем фрейм данных](image/38.png){width=80% height=80%}

Как мы видим результат практически идентичен и Результат Intercept во всех 3 случаях также одинаковое $-0.000628618$. 

**Часть 2**: Найдите линию регрессии, используя данные $(𝑋, 𝑦)$. Постройте график $(𝑋, 𝑦)$, используя точечный график. Добавьте линию регрессии, используя abline!. Добавьте заголовок «График регрессии» и подпишите оси $𝑥$ и $𝑦$.

![Линия регрессии](image/39.png){width=80% height=80%}

### Модель ценообразования биномиальных опционов

a) Пусть $S = 100, T = 1, n = 10000, 𝜎 = 0.3$ и  $𝑟 = 0.08$. Попробуйте построить траекторию курса акций. Функция rand () генерирует случайное число от 0 до 1:

![Решения и график](image/40.png){width=80% height=80%}

b) Создайте функцию createPath (S :: Float64, r :: Float64, sigma ::Float64, T :: Float64, n :: Int64), которая создает траекторию цены акции с учетом начальных параметров. Используйте createPath, чтобы создать 10 разных траекторий и построить их все на одном графике:
 
![Функция createPath](image/41.png){width=80% height=80%}

![График 10 разных траекторий](image/42.png){width=80% height=80%}

c) Распараллельте генерацию траектории. Можете использовать ```Threads.@threads, pmap``` и ```@parallel```.

![Распараллеливание генерации траектории](image/43.png){width=80% height=80%}

# Листинги  программы

```julia
# Обновление окружения:
using Pkg
Pkg.update
# Установка пакетов:
using Pkg
for p in ["CSV", "DataFrames", "RDatasets", "FileIO"]
    Pkg.add(p)
end
using CSV, DataFrames, DelimitedFiles
# Считывание данных и их запись в структуру:
P = CSV.File("programminglanguages.csv") |> DataFrame
# Функция определения по названию языка программирования года его создания:
function language_created_year(P,language::String)
    loc = findfirst(P[:,2].==language)
    return P[loc,1]
end
# Пример вызова функции и определение даты создания языка Python:
print(language_created_year(P,"Python"))
# Пример вызова функции и определение даты создания языка Julia:
language_created_year(P,"Julia")
language_created_year(P,"julia")
# Функция определения по названию языка программирования
# года его создания (без учёта регистра):
function language_created_year_v2(P,language::String)
    loc = findfirst(lowercase.(P[:,2]).==lowercase.(language))
    return P[loc,1]
end
# Пример вызова функции и определение даты создания языка julia:
language_created_year_v2(P,"julia")
# Построчное считывание данных с указанием разделителя:
Tx = readdlm("programminglanguages.csv", ',')
# Запись данных в CSV-файл:
CSV.write("programming_languages_data2.csv", P)
# Пример записи данных в текстовый файл с разделителем ',':
writedlm("programming_languages_data.txt", Tx, ',')
# Пример записи данных в текстовый файл с разделителем '-':
writedlm("programming_languages_data2.txt", Tx, '-')
# Построчное считывание данных с указанием разделителя:
P_new_delim = readdlm("programming_languages_data2.txt", '-')
# Инициализация словаря:
dict = Dict{Integer,Vector{String}}()
# Инициализация словаря:
dict2 = Dict()
# Заполнение словаря данными:
for i = 1:size(P,1)
    year,lang = P[i,:]
    if year in keys(dict)
        dict[year] = push!(dict[year],lang)
    else
        dict[year] = [lang]
    end
end
# Пример определения в словаре языков программирования, созданных в 2003 году:
dict[2003]
# Подгружаем пакет DataFrames:
using DataFrames
# Задаём переменную со структурой DataFrame:
df = DataFrame(year = P[:,1], language = P[:,2])
# Вывод всех значения столбца year:
df[!,:year]
# Получение статистических сведений о фрейме:
describe(df)
# Подгружаем пакет RDatasets:
using RDatasets
# Задаём структуру данных в виде набора данных:
iris = dataset("datasets", "iris")
# Определения типа переменной:
typeof(iris)
describe(iris)
# Отсутствующий тип:
a = missing
typeof(a)
# Пример операции с переменной отсутствующего типа:
a + 1
# Определение перечня продуктов:
foods = ["apple", "cucumber", "tomato", "banana"]
# Определение калорий:
calories = [missing,47,22,105]
# Определение типа переменной:
typeof(calories)
# Подключаем пакет Statistics:
using Statistics
# Определение среднего значения:
mean(calories)
# Определение среднего значения без значений с отсутствующим типом:
mean(skipmissing(calories))
# Задание сведений о ценах:
prices = [0.85,1.6,0.8,0.6]
# Формирование данных о калориях:
dataframe_calories = DataFrame(item=foods,calories=calories)
# Формирование данных о ценах:
dataframe_prices = DataFrame(item=foods,price=prices)
# Объединение данных о калориях и ценах:
DF = innerjoin(dataframe_calories,dataframe_prices,on=:item)
# Подключаем пакет FileIO:
using FileIO
# Подключаем пакет ImageIO:
import Pkg
Pkg.add("ImageIO")
# Загрузка изображения:
X1 = load("julialogo.png")
# Определение типа и размера данных:
@show typeof(X1);
@show size(X1);
# Загрузка пакетов:
import Pkg
Pkg.add("DataFrames")
Pkg.add("Statistics")
using DataFrames
using CSV
import Pkg
Pkg.add("Plots")
# Загрузка данных:
houses = CSV.File("houses.csv") |> DataFrame
# Построение графика:
using Plots
plot(size=(500,500),leg=false)
x = houses[!,:sqft]
y = houses[!,:price]
scatter(x,y,markersize=3)
# Фильтрация данных по заданному условию:
filter_houses = houses[houses[!,:sqft].>0,:]
# Построение графика:
x = filter_houses[!,:sqft]
y = filter_houses[!,:price]
scatter(x,y)
# Подключение пакета Statistics:
using Statistics
# Определение средней цены для определённого типа домов:
combine(groupby(filter_houses,:type),filter_houses->
        mean(filter_houses[!,:price]))
# Подключение пакета Clustering:
import Pkg
Pkg.add("Clustering")
using Clustering
# Добавление данных :latitude и :longitude в новый фрейм:
X = filter_houses[!, [:latitude,:longitude]]
# Конвертация данных в матричный вид:
X = Matrix{Float64}(X)
# Транспонирование матрицы с данными:
X = X'
# Задание количества кластеров:
k = length(unique(filter_houses[!,:zip]))
# Определение k-среднего:
C = kmeans(X,k)
# Формирование фрейма данных:
df = DataFrame(cluster = C.assignments,city = filter_houses[!,:city],
    latitude = filter_houses[!,:latitude],longitude = 
        filter_houses[!,:longitude],zip = filter_houses[!,:zip])
clusters_figure = plot(legend = false)
for i = 1:k
    clustered_houses = df[df[!,:cluster].== i,:]
    xvals = clustered_houses[!,:latitude]
    yvals = clustered_houses[!,:longitude]
    scatter!(clusters_figure,xvals,yvals,markersize=4)
end
xlabel!("Latitude")
ylabel!("Longitude")
title!("Houses color-coded by cluster")
display(clusters_figure)
unique_zips = unique(filter_houses[!,:zip])
zips_figure = plot(legend = false)
for uzip in unique_zips
    subs = filter_houses[filter_houses[!,:zip].==uzip,:]
    x = subs[!,:latitude]
    y = subs[!,:longitude]
    scatter!(zips_figure,x,y)
end
xlabel!("Latitude")
ylabel!("Longitude")
title!("Houses color-coded by zip code")
display(zips_figure)
# Подключение пакета NearestNeighbors:
import Pkg
Pkg.add("NearestNeighbors")
using NearestNeighbors
knearest = 10
id = 70
point = X[:,id]
# Поиск ближайших соседей:
kdtree = KDTree(X)
idxs, dists = knn(kdtree, point, knearest, true)
# Все объекты недвижимости:
x = filter_houses[!,:latitude];
y = filter_houses[!,:longitude];
scatter(x,y)
# Соседи:
x = filter_houses[idxs,:latitude];
y = filter_houses[idxs,:longitude];
scatter!(x,y)
# Фильтрация по районам соседних домов:
cities = filter_houses[idxs,:city]
# Фрейм с указанием площади и цены недвижимости:
F = filter_houses[!, [:sqft,:price]]
# Конвертация данных в массив:
F = Matrix{Float64}(F)'
# Подключение пакета MultivariateStats:
import Pkg
Pkg.add("MultivariateStats")
using MultivariateStats
# Приведение типов данных к распределению для PCA:
M = fit(PCA, F)
# Выделение значений главных компонент в отдельную переменную:
y = MultivariateStats.transform(M, F)
​
Xr = reconstruct(M, y)
# Построение графика с выделением главных компонент:
scatter(F[1,:],F[2,:])
scatter!(Xr[1,:],Xr[2,:])
xvals = repeat(1:0.5:10,inner=2)
yvals = 3 .+ xvals + 2*rand(length(xvals)) .- 1
scatter(xvals,yvals,color=:black,leg=false)
function find_best_fit(xvals,yvals)
    meanx = mean(xvals)
    meany = mean(yvals)
    stdx = std(xvals)
    stdy = std(yvals)
    r = cor(xvals,yvals)
    a = r*stdy/stdx
    b = meany - a*meanx
    return a,b
end
a,b = find_best_fit(xvals,yvals)
ynew = a * xvals .+ b
plot!(xvals,ynew)
xvals = 1:100000;
xvals = repeat(xvals,inner=3);
yvals = 3 .+ xvals + 2*rand(length(xvals)) .- 1;
@show size(xvals)
@show size(yvals)
@time a,b = find_best_fit(xvals,yvals)
import Pkg
Pkg.add("PyCall")
Pkg.add("Conda")
using PyCall
using Conda
py"""
import numpy
def find_best_fit_python(xvals,yvals):
    meanx = numpy.mean(xvals)
    meany = numpy.mean(yvals)
    stdx = numpy.std(xvals)
    stdy = numpy.std(yvals)
    r = numpy.corrcoef(xvals,yvals)[0][1]
    a = r*stdy/stdx
    b = meany - a*meanx
    return a,b
"""
find_best_fit_python = py"find_best_fit_python"
xpy = PyObject(xvals)
ypy = PyObject(yvals)
@time a,b = find_best_fit_python(xpy,ypy)
import Pkg
Pkg.add("BenchmarkTools")
using BenchmarkTools
@btime a,b = find_best_fit_python(xvals,yvals)
@btime a,b = find_best_fit(xvals,yvals)
Задания для самостоятельного выполнения
Кластеризация
using RDatasets
iris = dataset("datasets", "iris")
plot(size=(600, 600), leg=false)
​
x = iris[!, :SepalLength]
y = iris[!, :PetalLength]
scatter(x, y, markersize=3, title="Распределение признаков 
        SepalLength и PetalLength",
    xlabel="SepalLength", ylabel="PetalLength", leg=false)
X = iris[!, [:SepalLength, :PetalLength]]
X = Matrix(iris[!, [:SepalLength, :PetalLength]])
# Транспонирование матрицы с данными:
X = X'
k = length(unique(iris[!, :Species]))
C = kmeans(X,k)
iris_new = DataFrame(cluster = C.assignments,
    SepalLength=iris[!, :SepalLength], PetalLength=iris[!, :PetalLength], 
                    Spicies = iris[!, :Species])
cluster_figure = plot(legend = false)
for i = 1:k
    iris_new_clustered = iris_new[iris_new[!, :cluster].==i,:]
    xvals = iris_new_clustered[!, :SepalLength]
    yvals = iris_new_clustered[!, :PetalLength]
    scatter!(cluster_figure, xvals, yvals, markersize=4)
end
xlabel!("SepalLength")
ylabel!("PetalLength")
title!("Iris color-coded by cluster")
display(cluster_figure)
unique_species = unique(iris[!, :Species])
species_figure = plot(legend=false)
for uspecies in unique_species
    iris_sp = iris[iris[!, :Species].==uspecies,:]
    x = iris_sp[!, :SepalLength]
    y = iris_sp[!, :PetalLength]
    scatter!(species_figure, x, y)
end
xlabel!("SepalLength")
ylabel!("PetalLength")
title!("Iris color-coded by species")
display(species_figure)
Регрессия (метод наименьших квадратов в случае линейной регрессии)
# Часть 1
X = randn(1000, 3)
a0 = rand(3)
print(a0)
y = X * a0 + 0.1 * randn(1000);
function linear_regression_model(X,y)
    X2 = ones(1000)
    X = hcat(X,X2)
    return X \ y
end
a = linear_regression_model(X,y)
print(a)
using MultivariateStats
# using llsq
a = llsq(X,y)
print(a)
Pkg.add("GLM")
using GLM, DataFrames
X1 = X[:, 1]
X2 = X[:, 2]
X3 = X[:, 3]
​
data = DataFrame(y=y, x1=X1, x2=X2, x3=X3);
​
lm(@formula(y ~ x1 + x2 + x3), data)
# Часть 2
X = rand(100);
y = 2X + 0.1 * randn(100);
a, b = find_best_fit(X,y)
ynew = a * X .+ b
scatter(X, y, title="График регрессии", xlabel="X", 
        ylabel="y", color=:lightblue, leg=false, line=:scatter)
Plots.abline!(a, b, line=:solid)
Модель ценообразования биномиальных опционов
S = 100
T = 1
n = 10000
sigma = 0.3
r = 0.08
​
h = T / n # длина одного периода;
u = exp(r*h + sigma * sqrt(h))
d = exp(r*h - sigma * sqrt(h))
p = (exp(r*h) - d)/(u - d)
​
j = 0
stockTree = []
append!(stockTree, S)
for i in 1:n
    k = rand()
    if k < p
        append!(stockTree, S * (u^(i - j)) * (d ^ j))
    else
        j = j + 1
        append!(stockTree, S * (u^(i - j)) * (d ^ j))
    end
end
using Plots
plot(stockTree, title="Траектория курса акций", 
    xlabel="Длина биномиального дерева в годах",
    ylabel="Курс акций", leg=false)
function createPath(S::Float64, T::Float64, n::Int64, sigma::Float64, r::Float64) 
    # S - начальная цена акции;
    # T - длина биномиального дерева в годах;
    # n - длина одного периода;
    # sigma - волатильность акции;
    # 𝑟 — годовая процентная ставка;
    
    h = T / n # длина одного периода;
    u = exp(r*h + sigma * sqrt(h))
    d = exp(r*h - sigma * sqrt(h))
    p = (exp(r*h) - d)/(u - d)
    stockTree = []
    append!(stockTree, S)
    j = 0
​
    for i in 1:n
        k = rand()
        if k < p
            append!(stockTree, S * (u^(i - j)) * (d ^ j))
        else
            j = j + 1
            append!(stockTree, S * (u^(i - j)) * (d ^ j))
        end
    end
    return stockTree
end
for i in 1:10
    IJulia.clear_output(true)
    traj = createPath(100.0, 1.0, 10000, 0.3, 0.08)
    if i == 1
        p = plot(traj, title="Траектория курса акций", 
            xlabel="Длина биномиального дерева в годах",
            ylabel="Курс акций", leg=false)
    end
    p = plot!(traj)
    display(p)
end
using Base.Threads
Threads.@threads for i in 1:10
    IJulia.clear_output(true)
    traj = createPath(100.0, 1.0, 10000, 0.3, 0.08)
    if i == 1
        g = plot(traj, title="Траектория курса акций", 
            xlabel="Длина биномиального дерева в годах",
            ylabel="Курс акций", leg=false)
    end
    g = plot!(traj)
    display(g)
end
```

# Вывод

Я специализировала пакетов Julia для обработки данных.

# &emsp;<span style="color:green"> Библиотека math </span>

## &emsp;<span style="color:green"> Округление </span>

<span style="color:ForestGreen"> **int(x)** </span> округляет число в сторону нуля. Это стандартная функция, для ее использования не нужно подключать модуль math.

<span style="color:ForestGreen">**round(x)**</span>  округляет число до ближайшего целого. Если дробная часть числа равна 0.5, то число округляется до ближайшего четного числа.

<span style="color:ForestGreen">**round(x, n)**</span> 	округляет число x до n знаков после точки. Это стандартная функция, для ее использования не нужно подключать модуль math.

<span style="color:ForestGreen">**floor(x)**</span>  округляет число вниз («пол»), при этом floor(1.5) == 1, floor(-1.5) == -2

<span style="color:ForestGreen">**ceil(x)**</span> 	округляет число вверх («потолок»), при этом ceil(1.5) == 2, ceil(-1.5) == -1

<span style="color:ForestGreen">**abs(x)**</span> 	модуль (абсолютная величина). Это — стандартная функция.

## &emsp;<span style="color:green"> Корни, логарифмы

<span style="color:ForestGreen">**sqrt(x)**</span> 	квадратный корень. Использование: sqrt(x)

<span style="color:ForestGreen">**log(x)**</span> 	натуральный логарифм. При вызове в виде log(x, b) возвращает логарифм по основанию b.
e	основание натуральных логарифмов e = 2,71828...

## &emsp;<span style="color:green"> Тригонометрия

<span style="color:ForestGreen">**sin(x)**</span> 	синус угла, задаваемого в радианах

<span style="color:ForestGreen">**cos(x)**</span> 	косинус угла, задаваемого в радианах

<span style="color:ForestGreen">**tan(x)**</span> 	тангенс угла, задаваемого в радианах

<span style="color:ForestGreen">**asin(x)**</span> 	арксинус, возвращает значение в радианах

<span style="color:ForestGreen">**acos(x)**</span> 	арккосинус, возвращает значение в радианах

<span style="color:ForestGreen">**atan(x)**</span> 	арктангенс, возвращает значение в радианах

<span style="color:ForestGreen">**atan2(y, x)**</span> 	полярный угол (в радианах) точки с координатами (x, y).

<span style="color:ForestGreen">**degrees(x)**</span> 	преобразует угол, заданный в радианах, в градусы.

<span style="color:ForestGreen">**radians(x)**</span> 	преобразует угол, заданный в градусах, в радианы.

<span style="color:ForestGreen">**pi**</span>  	константа π = 3.1415...
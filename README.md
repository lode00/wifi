В рамках работы  __"Исследование особенностей позиционирования посредством технологии Wi-Fi"__  было проведено исследование алгоритмов машинного обучения, подходящих для пассивного позиционирования в помещениях. Предложенные модели протестированы на реальных данных, полученных в одной из хоровых студий города Санкт-Петербурга.
Результатом работы являются методика, позволяющая использовать алгоритмы машинного обучения для позиционирования в помещениях, на основе данных об уровне принимаемого сигнала. Данный проект используется для изучения проблемы классификации с использованием набора данных для машинного обучения и демонстрации использования различных моделей классификации в наборе данных.
Для этого проекта были выбраны 3 модели классификации: K-ближайшие соседи (K-NN), метод опорных векторов (SVM) и случайный лес (RF).  
 
 Что нам нужно?
-----------
В проекте используются записные книжки Jupyter с установленным Python 3.6 для реализации модельных архитектур.
Вспомогательные библиотеки:
pandas для структурирования данных;
numpy для линейной алгебры (в основном имеет дело с матрицами);
sklearn для кодирования и выборки данных;
matplotlib для построения качественных показателей и графиков.

 
 Почему Anaconda и Jupyter Notebook?
-----------
Дистрибутив Anaconda с открытым исходным кодом - это самый простой способ выполнения Python/R data science и машинного обучения на Linux, Windows и Mac OS X. Anaconda предоставляет инструменты, необходимые для легкого:
- собирать данные из файлов и баз данных,
- управлять средами с помощью Conda,
- делиться, сотрудничать и воспроизводить проекты.
Jupyter Notebook - это веб-приложение с открытым исходным кодом, которое позволяет создавать и обмениваться документами, содержащими живой код, уравнения, визуализации и описательный текст. Области применения включают: очистку и преобразование данных, численное моделирование, статистическое моделирование, визуализацию данных и машинное обучение. Он обеспечивает простоту выполнения и обучения моделей нейронных сетей.

 Данные 
-----------
Набор данных был создан на основе показаний RSSI от 8 точек доступа.Данные были собраны с помощью приложения Homedale. Измерения RSSI представляют собой отрицательные значения. 
Большие значения RSSI указывают на более близкое расположение к данной Wi-FI точке (например, RSSI -30 означает, что объект находится в нескольких метрах от точки по сравнению с RSS -50).
- Для Wi-Fi точек, находящихся вне зоны действия сети, RSSI обозначается значением -100.
- Координаты, связанные со значениями RSSI, состоят как из номеров квадратов, так и x, y и z координат.
- В [Analysis.ipynb](https://github.com/lode00/wifi/blob/main/Analysis.ipynb) показана работа алгоритмов, а также используется визуализация набора данных.
- В [Data_indoor.xlsx](https://github.com/lode00/wifi/blob/main/Data_indoor.xlsx) создана база отпечатков пальцев RSSI и сопоставлены соответствующие координаты.
- В [Data_route.xlsx](https://github.com/lode00/wifi/blob/main/Data_route.xlsx) показаны сырые данные маршрутов №1 и №2.
- В [Experiment_napravl.xlsx](https://github.com/lode00/wifi/blob/main/Experiment_napravl.xlsx) показаны результаты сбора уровня RSSI при разных положениях смартфона (Сравнение мощности принимаемого сигнала при разных положениях смартфона)

Заключение
-----------

Основываясь на окончательных результатах точности трех моделей классификатора, можно сделать вывод, что метод K-NN дал наилучшую производительность для данной задачи классификации.

Видео-эксперимент 
-----------
В данном видео сопоставлен реальный маршрут, пройденный с видеокамерой и маршрут, смоделированный в программе Sweet Home 3d. В качестве алгоритма позиционирования для модели выбран алгоритм KNN,так как он показал наилучшие результаты во время обучения.
https://youtu.be/QiAcEDXIFmg)

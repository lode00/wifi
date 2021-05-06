В рамках работы  "Исследование особенностей позиционирования посредством технологии Wi-Fi"   было проведено исследование алгоритмов машинного обучения, подходящих для пассивного позиционирования в помещениях. Предложенные модели протестированы на реальных данных, полученных в одной из хоровых студий города Санкт-Петербурга.Результатом работы являются методика, позволяющая использовать алгоритмы машинного обучения для позиционирования в помещениях, на основе данных об уровне принимаемого сигнала. Данный проект используется для изучения проблемы классификации с использованием набора данных для машинного обучения и демонстрации использования различных моделей классификации в наборе данных.
Для этого проекта были выбраны 3 модели классификации: K-ближайшие соседи (K-NN), метод опорных векторов (SVM) и случайный лес (RF).  
Что нам нужно?
-----------

В проекте используются записные книжки Jupyter с установленным Python 3.6 для реализации модельных архитектур.
Вспомогательные библиотеки:
pandas для структурирования данных
numpy для линейной алгебры (в основном имеет дело с матрицами)
sklearn для кодирования и выборки данных
matplotlib для построения качественных показателей и графиков

 Данные 
-----------
Набор данных был создан на основе показаний RSSI от 8 точек доступа.Данные были собраны с помощью приложения Homedale. Измерения RSSI представляют собой отрицательные значения. 
Большие значения RSSI указывают на более близкое расположение к данной Wi-FI точке (например, RSSI -30 означает, что объект находится в нескольких метрах от точки по сравнению с RSS -50).
- Для Wi-Fi точек, находящихся вне зоны действия сети, RSSI обозначается значением -100.
- Координаты, связанные со значениями RSSI, состоят как из номеров квадратов, так и x, y и z координат.

3.Заключение
Основываясь на окончательных результатах точности трех моделей классификатора, можно сделать вывод, что метод K-NN дал наилучшую производительность для данной задачи классификации.

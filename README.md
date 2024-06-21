# rental-cost-estimate  
Это проект по предобработке данных для создания модели машинного обучения, которая будет оценивать квартиры и предлагать релевантную стоимость аренды.  
  
В качестве региона выбрана Москва.  
  
На основании [датасета](https://drive.google.com/drive/folders/1fiFYfUzHqdt8ASeYIprfGAWNXn4TAPfO) включающего более 23 тысяч записей реальных объявлений  
работа по подготовке будет происходить в три этапа:  
  
### 1. Разведочный анализ данных - Exploratory Data Analysis, сформированный из EDA.ipynb.
  
*состав репозитория на данном релизе:*  
README.md описание задачи, состав участников  
EDA.html - отчет из графиков и текстового описания  
EDA.ipynb - jupyter notebook, в котором изучали данные  
  
### 2. Результаты очистки данных от пропусков.  
  
*состав репозитория дополняется:*  
preprocessing.ipynb - jupyter notebook файл, где показан процесс обработки данных  
data.csv - отвечающий критериям:  
названия колонок на английском языке в одно/несколько слов с нижним подчёркиванием  
в каждой колонке должны отсутствовать пропущенные значения (NaN, None и т.д.)  
  
### 3. Финальный. Коммит данных с новыми фичами, отрефакторенный с прошлого релиза и файл data.csv c новыми колонками.  
  
*в составе репозитория изменения:*  
README.md добавлены основные выводы и иллюстрации  
data.csv - полностью отвечающий предыдущим и новым критериям:  
все значения внутри данных должны быть только численного типа (int или float)  
отсутствуют полные дубликаты объявлений, только уникальные объявления  
preprocessing.ipynb - jupyter notebook файл, где показан весь процесс обработки данных с комментариями, которые объясняют мотивацию принятия тех или иных решений в ходе работы

**Над проектом работали:**  
*Поляков Константин*  
*Крушиницкая Ольга*  
*Чебурашкин-Антипов Дмитрий*  
  
## Выводы:  
  
В результате обработки данных и построения матрицы корреляций были выявлены признаки, которые в бОльшей степени влияют на стоимость аренды  
а именно:  
* Количество комнат
* Площадь
* Адрес
  
Ниже приведены:  
* Матрица корреляций
* Точечные распределения признаков с коэффициентом Пирсона более 0.5
* Гистограмма распределения стоимости аренды

![corr_matrix](src/matrix.png)
![scatter](src/scatter.png)
![hist](src/hist.png)

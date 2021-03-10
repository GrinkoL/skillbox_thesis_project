# Дипломный проект.
Проект реализован в среде Google Colab.

В данном проекте решена задача классификации изображений лиц на девять классов (девять эмоций) с категориальной точностью на приватной выборке 0.45360. 

Данные для воспроизведения обучения модели вы можете загрузить с [kaggle](https://www.kaggle.com/c/skillbox-computer-vision-project/data)

Поскольку разработанная в данном проекте модель достаточно тяжеловесная (1.34Gb), то разместить её на Github не представлялось возможным. Архив модели доступен для скачивания по [ссылке](https://drive.google.com/uc?id=1-HDQxtpZKGuKWQhsiDANyc41SL_CwHdU).

## Версии используемых библиотек:
 * Tensorflow 2.4.1
 * Keras 2.4.0

## Загрузка модели:
```
! pip install install import-ipynb
! git clone https://github.com/GrinkoL/skillbox_thesis_project.git
from skillbox_thesis_project.Import_model import Model
model = Model()
```
## Запуск предсказания модели:
```
# Замените имя файла с изображением на нужное
model.predict('test/25.jpg')
```

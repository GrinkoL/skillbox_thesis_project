# Дипломный проект.
Проект реализован в среде Google Colab.

В данном проекте решена задача классификации изображений лиц на девять классов (девять эмоций) с категориальной точностью на приватной выборке (на соответственном [kaggle сompetition](https://www.kaggle.com/c/skillbox-computer-vision-project)) 0.45360. Время инференса на одном jpg изображении ~ 60ms 

Данные для воспроизведения обучения модели вы можете загрузить с [kaggle соревнования](https://www.kaggle.com/c/skillbox-computer-vision-project/data)
Прымые сслыки для загрузки данных через python библиотеку gdown:
* Test data https://drive.google.com/uc?id=1bGHeWeWYXj5biL9s-qTc9gyv91WNAbWE
* Train data  https://drive.google.com/uc?id=1QdhIxh1QUEuLgRb7DWa7RA7CA08ybNRJ

В проекте выполена аугментация данных. Аугментированный теренеровочный набор изображений доступен по ссылке:
* Aug_train data: 'https://drive.google.com/uc?id=1ZHqymPmcdUoR0XF3V1wz-kTCKKLz0_SX'

Поскольку разработанная в данном проекте модель достаточно тяжеловесная (1.34Gb), то разместить её на Github не представлялось возможным. Архив модели доступен для скачивания по [ссылке](https://drive.google.com/uc?id=1-HDQxtpZKGuKWQhsiDANyc41SL_CwHdU).

В прокте используется технология finetuning. В качестве базовой модели выбрана модель VGG16. Данная модель (совместимая с Keras) с весами полученными при обучении на датасете VGGFace1 доступна в  [проекте](https://github.com/rcmalli/keras-vggface)

## Версии используемых библиотек:
 * Tensorflow 2.4.1
 * Keras 2.4.0

## Загрузка модели:
```
# Установка пакета для импорта ipynb файлов
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

# Дипломный проект.
Проект реализован в среде Google Colab.

В данном проекте решена задача классификации изображений лиц на девять классов (девять эмоций) с категориальной точностью на приватной выборке 0.45360. 

Данные для воспроизведения обучения модели вы можете загрузить с [kaggle](https://www.kaggle.com/c/skillbox-computer-vision-project/data)

Поскольку разработанная в данном проекте модель достаточно тяжеловесная (1.2Gb), то разместить её на Github не представлялось возможным. Архив модели доступен для скачивания по [ссылке](https://drive.google.com/uc?id=1-HDQxtpZKGuKWQhsiDANyc41SL_CwHdU).

## Версии используемых библиотек:
 * Tensorflow 2.4.1
 * Keras 2.4.0

## Закрузка модели:
```
# Устанавливаем и импортируем модуль для загрузки
! pip install gdown
import gdown
# Загружаем архив
gdown.download('https://drive.google.com/uc?id=1-HDQxtpZKGuKWQhsiDANyc41SL_CwHdU', 'model.zip', False)
# Распаковываем в текущую директорию
! unzip model.zip -d .
```
## Импорт модели:
```
from tensorflow.keras import models
model = models.load_model('model')
```
## Предобработка изображений:
```
# Модель разработана на основе VGG модели, поэтому предобработка аналогичная.
# Для этого, скачиваем и устанавливаем сторонний модуль keras-vggface
! pip install git+https://github.com/rcmalli/keras-vggface.git > /dev/null
# Для дальнейшей работы с keras-vggface необходим модуль keras_apllications. Установим его.
! pip install keras_applications > /dev/null

from keras_vggface import utils
from tensorflow.keras.preprocessing import image
# Измените путь до изображения на нужный
img = image.load_img('.../image.jpg', target_size=(224,224))
img = image.img_to_array(img)
img = img[None, ...]
img = utils.preprocess_input(img)
```
## Предсказание и декодирование:
```

```

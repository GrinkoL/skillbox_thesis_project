# Дипломный проект.
Проект реализован в среде Google Colab.

В данном проекте решена задача классификации изображений лиц на девять классов (девять эмоций) с категориальной точностью на приватной выборке (на соответственном [kaggle соревновании](https://www.kaggle.com/c/skillbox-computer-vision-project)) 0.45360. Время инференса на одном jpg изображении ~ 60ms.

Поскольку разработанная в данном проекте модель достаточно тяжеловесная (1.34Gb), то разместить её на Github не представлялось возможным. Архив модели доступен для скачивания по [ссылке](https://drive.google.com/uc?id=1-HDQxtpZKGuKWQhsiDANyc41SL_CwHdU).

Данные для воспроизведения обучения модели, а также для проверки точности её работы вы можете загрузить с [kaggle соревнования](https://www.kaggle.com/c/skillbox-computer-vision-project/data)
Прымые сслыки для загрузки данных через python библиотеку gdown:
* Test data https://drive.google.com/uc?id=1bGHeWeWYXj5biL9s-qTc9gyv91WNAbWE
* Train data  https://drive.google.com/uc?id=1QdhIxh1QUEuLgRb7DWa7RA7CA08ybNRJ

В проекте выполена аугментация данных. Аугментированный, теренировочный набор изображений доступен по ссылке:
* Aug_train data: 'https://drive.google.com/uc?id=1ZHqymPmcdUoR0XF3V1wz-kTCKKLz0_SX'

В прокте используется технология finetuning. В качестве базовой модели выбрана модель VGG16. Данная модель (совместимая с Keras) с весами полученными при обучении на датасете VGGFace1 доступна в  [проекте](https://github.com/rcmalli/keras-vggface)

## Версии используемых библиотек:
 * Tensorflow 2.4.1
 * Keras 2.4.0

## Запуск предсказания модели:
Создайте новый .ipynb файл. Склонируйте проект !git clone https://github.com/GrinkoL/skillbox_thesis_project.git и запустите файл run_prediction_of_model.ipynb
Загрузите модель и передайте путь до файла методу predict как это сделано в файле run_prediction_of_model.ipynb, расположенном в корне проекта.

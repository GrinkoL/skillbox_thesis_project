# Дипломный проект.
Проект реализован в среде Google Colab. Для воспроизведения результатов все ноутбуки следует запускать в Google Colab кроме одного, run_model_with_OpenCV.ipynb, он требует доступа к камере, поэтому его стоит запускать локально в среде Jupyter Notebook.

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
Запустите файл run_prediction_of_model.ipyn. В нём показано как использовать модель для инференса на примере одного из тестовых изображений.

## Запуск предсказания эмоции в реальном времени:
Загрузите проект в корневую директорию Jupyter Notebook.

Внимание(!), убедитесь, что файл с проектом называться skillbox_thesis_project!

Запустите в среде Jupyter Notebook файл run_model_with_OpenCV.ipynb. 

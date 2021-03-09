# Skillbox_thesis_project
В данном проекте решена задача классификации изображений лиц на девять классов (девять эмоций) с категориальной точностью на приватной выборке 0.45360. 

Данные для воспроизведения обучения модели вы можете загрузить с [kaggle](https://www.kaggle.com/c/skillbox-computer-vision-project/data)

Поскольку разработанная в данном проекте модель достаточно тяжеловесная (1.2Gb), то разместить её на Github не представляется возможным. Архив модели доступен для скачивания по [ссылке](https://drive.google.com/uc?id=1-HDQxtpZKGuKWQhsiDANyc41SL_CwHdU).

## Закрузка модели в среде Google Colab:
```
# Устанавливаем и импортируем модуль для загрузки
! pip install gdown
import gdown
# Загружаем архив
gdown.download('https://drive.google.com/uc?id=1-HDQxtpZKGuKWQhsiDANyc41SL_CwHdU', 'model.zip', False)
# Распаковываем в текущую директорию
! unzip model.zip -d .
```

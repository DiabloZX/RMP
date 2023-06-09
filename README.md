# Проект для дисциплины "Разработка мобильных приложений"
Данное приложение разработано на `kotlin'е` с использованием `Jetpack compose`.
Программа имеет интерактивную карту, созданную на основе `OpenStreetMap`, базу данных, в которой сохраняются введённые данные пользователя и использует открытое API `nominatim.openstreetmap` для геокодинга.

Принцип работы приложения в следующем:
пользователь может создавать заметки, связанные с местоположением и временем. Напрмиер, он создает метку на карте в районе поликлиники и отмечает время, в описании он может написать "*Приём у врача*", потом в списке меток он может найти эту заметку и понять, куда сегодня и во сколько должен идти и что там будет происходить.

# Build
Для сборки приложения используйте команду (из корневой папки проекта):
```shell
./gradlew assembleDebug
```

Результат сборки находится в:
```shell
MapMark/app/build/outputs/apk/debug
```


# Монетизация
Монетизация приложения возможна при помощи урезания функционала (количественного) и предоставлении пользователю расширить этот функционал за покупки внутри приложения. 
Например, максимальное количетсво заметок в бд будет ограниченно, или же можно ограничить количество новых заметок в день.

# Публикация
Приложение планируется опубликовать в Play Market, так как это большая платформа с миллионами пользователей. После публикации, можно запустить рекламу, чтобы заявить о существовании приложения.

# Руководство пользователя
Приложение состоит из 3 основных элементов:
- Карта
- Добавление новых заметок
- Список заметок

## Карта
На карте вы можете рассматривать географическое положение существующих заметок
Также, на карте вы можете выбирать место для новой заметки

<img src="https://github.com/DiabloZX/RMP/assets/74893461/b4aa84ea-91a7-4f40-a536-3b866eb8e5ad" height="600" width="300">
<img src="https://github.com/DiabloZX/RMP/assets/74893461/f9220993-7dbc-4572-9fa4-592b045a42cd" height="600" width="300">

## Добавление новых заметок
Добавление заметок происходит следующим образом:
Пользователь нажимает на кнопку "Add bookmark" (Добавить заметку) вверху экарана 

![image](https://github.com/DiabloZX/RMP/assets/74893461/36cb97f8-8a20-4b9d-9576-ec86aa3e1ebb)

После чего на карте появляется метка для выбора геопозиции метки. Метка движется за центром экрана.

![image](https://github.com/DiabloZX/RMP/assets/74893461/1e18dbdf-e9da-4818-8f7e-7fd8bff434f9)

Также появляются кнопки для добавления выбранной заметки, если пользователь уверен ("Add") или отмены ("Cancel"). 
Ниже кнопок есть поле для ввода названия заметки (например: "Встреча с друзьями").

![image](https://github.com/DiabloZX/RMP/assets/74893461/68c8843b-b637-48da-891b-adc13c6faf7e)

Когда же пользователь подтверждает создание заметки, ему предлагается выбрать время для заметки. По умолчанию выбрано текущее время и текущая дата

![image](https://github.com/DiabloZX/RMP/assets/74893461/b9b9ebf0-beaa-4530-9327-ac4bccbcb208)
![image](https://github.com/DiabloZX/RMP/assets/74893461/6c191f05-aa5c-442b-87ca-4fbac7236fca)

Когда же время с датой будут выбраны, создасться новая заметка, которая будет отображаться на карте и в списке заметок.

## Список заметок
Потянув нижнюю шторку, пользователю откроется список текущих заметок.
Здесь представлена такая информация, как:
- Наименование заметки
- Местоположение (название здания или места)
- Время заметки
Заметки разделены между собой чертой-разделителем

<img src="https://github.com/DiabloZX/RMP/assets/74893461/0ea4f9f6-865c-4b7e-8c8b-ecf573fb0e21" height="600" width="300">

При необходимости, не нужные заметки можно удалить, нажав крестик рядом с ними.
После этого заметка удалится из списка и карты, а остальные заметки заного загрузятся в списке.

![image](https://github.com/DiabloZX/RMP/assets/74893461/938a4392-f696-4ce8-bea6-53404de69ef4)

# ВАЖНО
При включенной на телефоне темной теме весь текст становится белым, как цвет кнопок, и ничего не различимо. 
Рекомендуется установить светлую тему для комфортного пользования приложением. В дальнейших идеях по разрабокте приложения планируется устранить этот изъян




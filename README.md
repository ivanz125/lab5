## Лабораторна робота №5
### Розпізнавання монет

Алгоритм дій:
1. Завантажити зображення монет для тренування детектора (10-15 штук)
Зображення присутні в папці /img

2. Створити набір даних (.xml файл) з посиланнями на зображення (через imglab)
Файли створені в папці /tools/imglab/build/Debug

3. Виділити області з монетами на зображеннях (файли вже розмічені)
Команда консолі (виконувати з /tools/imglab/build/Debug):
```
imglab coins50.xml
```

4. Запустити тренування детектора для конкретного набору даних (виконувати з /src/build/Debug):
```
train_object_detector -tv coins50.xml
```

5 Перевірити необхідне фото
```
train_object_detector image.jpg
```


### Компіляція програми
Компіляція самої програми:
```
mkdir dlib/src/build
cd dlib/src/build
cmake ..
cmake --build .
```

Компіляція інструменту для фото:
```
mkdir dlib/tools/imglab/build
cd dlib/tools/imglab/build
cmake ..
cmake --build .
```

Програма та imglab вже скомпільовані

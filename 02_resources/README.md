# Домашнее задание к занятию «1.2. Ресурсы, View и ViewGroup»

В качестве результата пришлите ссылки на ваш GitHub-проект в личном кабинете студента на сайте [netology.ru](https://netology.ru).

**Важно**: ознакомьтесь со ссылками, представленными на главной странице [репозитория с домашними заданиями](../README.md).

**Важно**: если у вас что-то не получилось, то оформляйте Issue [по установленным правилам](../report-requirements.md).

## Как сдавать задачи

1. Откройте ваш проект с предыдущего ДЗ
1. Сделайте необходимые коммиты
1. Сделайте пуш (удостоверьтесь, что ваш код появился на GitHub)
1. Ссылку на ваш проект отправьте в личном кабинете на сайте [netology.ru](https://netology.ru)
1. Задачи, отмеченные, как необязательные, можно не сдавать, это не повлияет на получение зачета (в этом ДЗ все задачи являются обязательными)

## Задача Launcher Icon

### Легенда

Что нужно делать первым делом после "Hello, World"? Первым делом нужно установить своему приложению красивую иконку, чтобы это был не логотип Android, а красивая кастомная иконка.

Для этого мы будем использовать [логотип Нетологии](assets/netology.svg), который уже рассматривали на лекции.

Для создания иконок используется Image Asset Studio, который входит в состав Android Studio. Asset Studio позволяет вам выбрать изображение и сам разместит необходимые файлы в каталогах `res/mipmap-<density>`.

Начиная с Android 8.0, применяется подход адаптивных иконок запуска, которые разделяют подложку иконки (background) и непосредственно foreground часть (чаще всего логотип), позволяя в зависимости от устройства менять форму подложки.

![](pic/launcher01.gif)

![](pic/launcher02.gif)

Примечание: изображения с developer.android.com

### Задача

Замените иконку вашего приложения из предыдущего ДЗ на [логотип Нетологии](assets/netology.svg).

1\. Кликните правой кнопкой мыши (или Alt + Insert) на каталоге `mipmap` и выберите пункт `Image Asset`:

![](pic/asset01.png)

2\. Выберите изображение (1) и перемещайте ползунок Resize (2) до тех пор, пока логотип не станет попадать целиком в границы (отмечены серым цветом):

![](pic/asset02.png)

3\. Перейдите на вкладку Background Layer (1), выберите Asset Type - Color (2) и поставьте цвет - FFFFFF (3):

![](pic/asset03.png)

4\. (Необязательно) Перейдите на вкладку Options - вы увидите, что по умолчанию настройки выставлены в генерацию иконок (т.е. будут сгенерированы изображения для тех версий Android, что не поддерживают адаптивные иконки):

![](pic/asset04.png)

5\. Подтвердите генерацию файлов:

![](pic/asset05.png)

6\. Удалите "старые файлы" (с иконкой Android):

![](pic/asset06.png)

7\. Запустите ваше приложение в эмуляторе и удостоверьтесь, что иконка приложения изменилась

![](pic/asset07.png)

Если при сборке возникают ошибки, нажмите два раза Ctrl и выполните `gradlew clean` и соберите заново

<details>
<summary>Под капотом</summary>

Иконка указывается в манифесте:

```xml
```

Эти значения ведут на файлы `mipmap/ic_launcher` и (`mipmap/ic_launcher_round`) соответственно. В зависимости от версии платформы это будут либо сгенерированные изображения в формате png, либо xml, в которых стоят ссылки на `foreground` и `background` ресурсы.
</details>

Опубликуйте изменения в вашем проекте на GitHub. Удостоверьтесь, что apk собирается с помощью GitHub Actions и при установке в эмуляторе иконка приложения также соответствует установленной вами.

В качестве результата пришлите ссылку на ваш GitHub-проект в личном кабинете студента на сайте [netology.ru](https://netology.ru).

## Задача Translations

### Легенда

Мы договорились, что всё будем делать на двух языках: русском и английском.

По аналогии с лекцией добавьте файлы переводов в своё приложение.

Переводиться должны:
1. Название приложения (пусть на русском будет "НМедиа")
1. Текст (пусть на русском будет "НМедиа!")

### Задача

1. Создайте файл переводов по аналогии с лекцией
1. Убедитесь, что при изменении языка перевод отображается корректно

Опубликуйте изменения в вашем проекте на GitHub. Удостоверьтесь, что apk собирается с помощью GitHub Actions и при установке в эмуляторе приложение работает корректно.

В качестве результата пришлите ссылку на ваш GitHub-проект в личном кабинете студента на сайте [netology.ru](https://netology.ru).

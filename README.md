# Шпаргалка по работе с Git
## Cодержание
- [Установка Git](https://github.com/v1lezz/Git-Learner#%D1%83%D1%81%D1%82%D0%B0%D0%BD%D0%BE%D0%B2%D0%BA%D0%B0-git)
- [Проверка наличия Git в системе и ее версии](https://github.com/v1lezz/Git-Learner#%D0%BF%D1%80%D0%BE%D0%B2%D0%B5%D1%80%D0%BA%D0%B0-%D0%BD%D0%B0%D0%BB%D0%B8%D1%87%D0%B8%D1%8F-git-%D0%B2-%D1%81%D0%B8%D1%81%D1%82%D0%B5%D0%BC%D0%B5-%D0%B8-%D0%B5%D0%B5-%D0%B2%D0%B5%D1%80%D1%81%D0%B8%D0%B8)
- [Настройка Git](https://github.com/v1lezz/Git-Learner#%D0%BD%D0%B0%D1%81%D1%82%D1%80%D0%BE%D0%B9%D0%BA%D0%B0-git)
- [Команды для работы с репозиторием](https://github.com/v1lezz/Git-Learner#%D0%BD%D0%B0%D1%81%D1%82%D1%80%D0%BE%D0%B9%D0%BA%D0%B0-git)
	
## Установка Git
### Windows	
### MacOS
#### 1 способ - через консоль:
Откройте консоль и выполните команду `/usr/bin/git`. Она запустит установщик. Нажмите **Install** и дождитесь окончания установки.

![alt-текст](./data/macos.png "Текст заголовка логотипа 1")

#### 2 способ - использование Homebrew:
- Перейдите [на официальный сайт Homebrew](https://brew.sh/).
- Скопируйте команду для установки — справа от неё есть символ для копирования. Нажмите на него, чтобы команда попала в буфер обмена.

![alt-текст](./data/homebrew.png "Текст заголовка логотипа 1")

- Найдите программу Terminal в поиске Spotlight или в списке программ. Вставьте скопированный текст в окно терминала и нажмите `Enter`.

### Linux

Для установки Git на Linux нужно использовать терминал. Найдите программу Terminal в поиске или в списке программ. Перейдите на [официальный сайт Git](https://git-scm.com/download/linux) и выберите команду установки для своей версии Linux. Скопируйте её в программу Terminal и нажмите `Enter`. 

## Проверка наличия Git в системе и ее версии
`git version` - при наличии системы контроля версий выводит ее версию (ниже пример на Fedora Linux).

![alt-текст](./data/gitversion.png "Текст заголовка логотипа 1")

## Настройка Git
`git config` - настройка параметров (для конкретизациия параметров используются флаги). Зачастую рекомендуют указать хотя бы никнейм и адрес электронной почты. Это необходимо для того, чтобы было понятно, кто и какие изменения вносил.
Пример элементарной настройки:

![alt-текст](./data/gitconfig.png "Текст заголовка логотипа 1")

## Команды для работы с репозиторием
- `git init` - инициализация репозитория</br>
- `rm -rf .git` - удаление репозитория (команда удаляет папку .git, можно сделать и через обычный менеджер файлов)</br>
- `git status` - проверка статуса репозитория (выводит название текущей ветки, а также информацию о трекинге файлов в репозитории и коммитах)</br>
- `git add` - добавление/обновление файла для последующего коммита (с помощью `git add --all` или `git add .` можно добавить всю текущую папку с учетом файла .gitignore, в котором прописаны все файлы, которые должны быть проигнорированы)</br>
- `git commit -m "Сообщение"` - коммит изменений (выводится информация о ветке, идентификаторе коммита, а также о количестве новых/измененных файлов)</br>
- `git log` - просмотр истории коммитов c информацией о авторе, дате и сообщении коммита (коммиты выводятся по правилу стэка - LIFO)
- `git remote add origin git@github.com:%ИМЯ_АККАУНТА%/%НАЗВАНИЕ_УДАЛЕННОГО РЕПОЗИТОРИЯ%.git` - привязка локального репозитория к удаленному
- `git push -u origin main` - отправка изменений на удаленный сервер (флаг `-u` и параметры `origin main` стоит использовать при первой отправке изменений для связи текущей ветки с одноименной на удаленном сервере, в последующие разы достаточно команды `git push`)
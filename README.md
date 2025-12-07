# my-first-devops.

1.Подготовка стенда для работы:
  1.Развернуть образ ubuntu на WM 
  2.Скачать ssh-server командой:apt install openssh-server -y 
  3.Узнать IP-адрес хоста командой:ip a 
  4.Открыть Putty и в окне Name-Host\IP указать ip хоста(Предварительно пройти аутентификацию для дальнейшей работы)

2.Работа с Git&GitHub
  1.Скачать GitHub командой:sudo apt install git-all
  2.Проверка версии git после скачивания: git --version
  3.Авториоваться в GitHub(Если нет аккаунта то пройти регистрацию)
  4.Нажать на кнопку New repository(Предварительно указав все параметры для его создания) 
  4.Создать новый SSH-ключ для github командой:ssh-keygen -t rsa -b 4096 -C "email"
  5.Запустить ssh-agent и добавить приватный ключ:eval"$(ssh-agent -s)" (запуск агента), ssh-add /root/.ssh/id_rsa (Добавление ключа)
  6.Скопировать значение публичного ключа и добавить в раздел SSH and GPG keys: cat /root/.ssh/id_rsa.pub(Чтение содержимого в открытого ключа) 
  7.Проверка корректности настройки GitHub-key: ssh -T git@gihub.com(Если корректно все настроено то высветиться приветствие при от github)
  8.Для клонирования репозитория ввести команду:git clone git@github.com:<user_name>/<repository_name>
  9.Переход в репозиторий:cd <repository_name>(при клонировании репозиторий добавляется в ту же директория в которой находиться и пользователь) 

3.Работа с Docerk 
  1.При установка dockera следует опираться на официальную инструкцию 
  2.Запуск и проверка версии командой:systemctl start docker, docker --version 
  3.Запуск контейнера hello-world командой:docker run hello-world(В ответ получим приветствие от docekr)

4.Создание собственного контейнера 
  1.Создать докер-файл командой:nano dockerfile(указываем тело файла используя источник dockerhub)
  2.Создать python-скрипт командой:nano script.py(Используем команду print(для вывода текста), указываем файл скрипта в dockerfile в параметр COPY и CMD)
  3.Загрузить docekrfile командой:docker build -t <name>:<tag> <путь до файла>
  4.Запустить контейнер с нашим образом:docker run <name>

Сложности:
1.В определенных местах при выполнении ТЗ возникали незначительные вопросы 

Решение:
1.Сбор нужной информации в интернете

![Hello devops] (https://github.com/user-attachments/assets/1232c6f6-346f-4692-bbf6-da7c06384ef2)
![Hello from Docker] (https://github.com/user-attachments/assets/cb2d9ad8-1514-4b88-a8a6-24b3da894017)


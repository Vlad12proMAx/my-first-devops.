# my-first-devops.

1.Подготовка стенда для работы:
  1.Развернуть образ ubuntu на WM 
  2.Скачать ssh-server командой:apt install openssh-server -y 
  3.Узнать IP-адрес хоста командой:ip a 
  4.Открыть Putty и в окне Name-Host\IP указать ip хоста(Предворительно пройти аунтотификацию)

2.Работа с Git&GitHub
  1.Скачивать GitHub командой:sudo apt install git-all
  2.Проверка версии git после скачивания: git --version
  3.Авториоваться в GitHub(Если нет акаунта то пройти регистрацию)
  4.Нажать на кнопку New repository(Предварительно указав все параметры для его создания) 
  4.Создать новый SSH-ключ для github командой:ssh-keygen -t rsa -b 4096 -C "email"
  5.Запустить ssh-agent и добавить приватный ключ:eval"$(ssh-agent -s)" (запуск агента), ssh-add /root/.ssh/id_rsa (Добавление)
  6.Скопировать значение публичного ключа и добавить в раздел SSH and GPG keys: cat /root/.ssh/id_rsa.pub(Чтение содержимого в открытом ключе) 
  7.Проверка корректности настройки GitHub-key: ssh -T git@gihub.com(Если корректно все настроенно то высветиться приветсвия от github)
  8.Для кланирования репозитория ввести команду:git clone git@github.com:<user_name>/<repository_name>

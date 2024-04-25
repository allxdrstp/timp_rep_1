
Laboratory work I

Данная лабораторная работа посвещена изучению утилит для разработки проектов
Tasks

    1. Ознакомиться со ссылками учебного материала
    2. Выполнить инструкцию учебного материала
    3. Составить отчет и отправить ссылку личным сообщением в Slack

Выполнение работы
```Console
alexandra@alexandra-virtual-machine:~/Рабочий стол/lab1$ export GITHUB_USERNAME=allxdrstp
alexandra@alexandra-virtual-machine:~/Рабочий стол/lab1$ export GIST_TOKEN=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
alexandra@alexandra-virtual-machine:~/Рабочий стол/lab1$ alias edit=nano


alexandra@alexandra-virtual-machine:~/Рабочий стол/lab1$ mkdir -p ${GITHUB_USERNAME}/workspace
alexandra@alexandra-virtual-machine:~/Рабочий стол/lab1$ cd ${GITHUB_USERNAME}/workspace
alexandra@alexandra-virtual-machine:~/Рабочий стол/lab1/allxdrstp/workspace$ pwd
/home/alexandra/Рабочий стол/lab1/allxdrstp/workspace
alexandra@alexandra-virtual-machine:~/Рабочий стол/lab1/allxdrstp/workspace$ cd ..
alexandra@alexandra-virtual-machine:~/Рабочий стол/lab1/allxdrstp$ pwd
/home/alexandra/Рабочий стол/lab1/allxdrstp


alexandra@alexandra-virtual-machine:~/Рабочий стол/lab1/allxdrstp$ mkdir -p workspace/tasks/
alexandra@alexandra-virtual-machine:~/Рабочий стол/lab1/allxdrstp$ mkdir -p workspace/projects/
alexandra@alexandra-virtual-machine:~/Рабочий стол/lab1/allxdrstp$ mkdir -p workspace/reports/
alexandra@alexandra-virtual-machine:~/Рабочий стол/lab1/allxdrstp$ cd workspace

alexandra@alexandra-virtual-machine:~/Рабочий стол/lab1/allxdrstp/workspace$ wget https://nodejs.org/dist/v6.11.5/node-v6.11.5-linux-x64.tar.xz
--2024-04-25 17:33:55--  https://nodejs.org/dist/v6.11.5/node-v6.11.5-linux-x64.tar.xz
Распознаётся nodejs.org (nodejs.org)… 104.20.22.46, 104.20.23.46, 2606:4700:10::6814:172e, ...
Подключение к nodejs.org (nodejs.org)|104.20.22.46|:443... соединение установлено.
HTTP-запрос отправлен. Ожидание ответа… 200 OK
Длина: 9356460 (8,9M) [application/x-xz]
Сохранение в: ‘node-v6.11.5-linux-x64.tar.xz’

node-v6.11.5-linux-x64.tar.xz             100%[====================================================================================>]   8,92M  32,9MB/s    за 0,3s    

2024-04-25 17:33:59 (32,9 MB/s) - ‘node-v6.11.5-linux-x64.tar.xz’ сохранён [9356460/9356460]

alexandra@alexandra-virtual-machine:~/Рабочий стол/lab1/allxdrstp/workspace$ tar -xf node-v6.11.5-linux-x64.tar.xz
alexandra@alexandra-virtual-machine:~/Рабочий стол/lab1/allxdrstp/workspace$ rm -rf node-v6.11.5-linux-x64.tar.xz
alexandra@alexandra-virtual-machine:~/Рабочий стол/lab1/allxdrstp/workspace$ mv node-v6.11.5-linux-x64 node


alexandra@alexandra-virtual-machine:~/Рабочий стол/lab1/allxdrstp/workspace$ ls node/bin
node  npm
alexandra@alexandra-virtual-machine:~/Рабочий стол/lab1/allxdrstp/workspace$ echo ${PATH}
/home/linuxbrew/.linuxbrew/bin:/home/linuxbrew/.linuxbrew/sbin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/games:/usr/local/games:/snap/bin
alexandra@alexandra-virtual-machine:~/Рабочий стол/lab1/allxdrstp/workspace$ export PATH=${PATH}:"pwd"/node/bin
alexandra@alexandra-virtual-machine:~/Рабочий стол/lab1/allxdrstp/workspace$ echo ${PATH}
/home/linuxbrew/.linuxbrew/bin:/home/linuxbrew/.linuxbrew/sbin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/games:/usr/local/games:/snap/bin:pwd/node/bin
alexandra@alexandra-virtual-machine:~/Рабочий стол/lab1/allxdrstp/workspace$ mkdir scripts
alexandra@alexandra-virtual-machine:~/Рабочий стол/lab1/allxdrstp/workspace$ cat > scripts/activate<<EOF
> export PATH=\${PATH}:"pwd"/node/bin
> EOF
alexandra@alexandra-virtual-machine:~/Рабочий стол/lab1/allxdrstp/workspace$ source scripts/activate

alexandra@alexandra-virtual-machine:~/Рабочий стол/lab1/allxdrstp/workspace$ gem install gist
Successfully installed gist-6.0.0
Parsing documentation for gist-6.0.0
Done installing documentation for gist after 0 seconds
1 gem installed

alexandra@alexandra-virtual-machine:~/Рабочий стол/lab1/allxdrstp/workspace$ (umask 0077 && echo ${GIST_TOKEN} > ~/.gist)

Report

alexandra@alexandra-virtual-machine:~/Рабочий стол/lab1/allxdrstp/workspace$ export LAB_NUMBER=01
alexandra@alexandra-virtual-machine:~/Рабочий стол/lab1/allxdrstp/workspace$ git clone https://github.com/tp-labs/lab${LAB_NUMBER} tasks/lab${LAB_NUMBER}
Клонирование в «tasks/lab01»...
remote: Enumerating objects: 74, done.
remote: Counting objects: 100% (3/3), done.
remote: Compressing objects: 100% (3/3), done.
remote: Total 74 (delta 0), reused 1 (delta 0), pack-reused 71
Получение объектов: 100% (74/74), 945.07 КиБ | 3.41 МиБ/с, готово.
Определение изменений: 100% (20/20), готово.
alexandra@alexandra-virtual-machine:~/Рабочий стол/lab1/allxdrstp/workspace$ mkdir reports/lab${LAB_NUMBER}
alexandra@alexandra-virtual-machine:~/Рабочий стол/lab1/allxdrstp/workspace$ cp tasks/lab${LAB_NUMBER}/README.md reports/lab${LAB_NUMBER}/REPORT.md
alexandra@alexandra-virtual-machine:~/Рабочий стол/lab1/allxdrstp/workspace$ cd reports/lab${LAB_NUMBER}
alexandra@alexandra-virtual-machine:~/Рабочий стол/lab1/allxdrstp/workspace/reports/lab01$ edit REPORT.md
alexandra@alexandra-virtual-machine:~/Рабочий стол/lab1/allxdrstp/workspace/reports/lab01$ gist REPORT.md
```

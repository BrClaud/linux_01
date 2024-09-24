# Отчет по проекту D01_Linux
## Ник: dorothyz

## Contents
1. [Part 1](#part-1)
2. [Part 2](#part-2)
3. [Part 3](#part-3)
4. [Part 4](#part-4)
5. [Part 5](#part-5)
6. [Part 6](#part-6)
7. [Part 7](#part-7)
8. [Part 8](#part-8)
9. [Part 9](#part-9)
10. [Part 10](#part-10)
11. [Part 11](#part-11)
12. [Part 12](#part-12)
13. [Part 13](#part-13)
14. [Part 14](#part-14)
15. [Part 15](#part-15)

## Part 1
Установил **Ubuntu 20.04 Server LTS** через **VirtualBox** 

проверил версию установленной системы

![1](materials/1.jpg)

## Part 2
создал нового пользователя от имени суперпользователя
![2.1](materials/2.1.jpg)

проверил его наличие, он находится в самом низу
![2.2](materials/2.2.jpg)

## Part 3
#### Cмена имени машины:
узнаем текущее имя

![3.1](materials/3.1.jpg)

меняем имя в **ВИМ**е

![3.2](materials/3.2.jpg)

Чтобы все сервисы начали использовать новое имя, вводим следующую команду

![3.3](materials/3.3.jpg)

перезагружаем VirtualBox? получаем новое имя машины

![3.5](materials/3.5.png)

меняем часовой пояса

![3.6](materials/3.6.jpg)

проверяем сетевые интерфейсы:

Один из самых основных виртуальных интерфейсов - lo. Это локальный интерфейс, который позволяет программам обращаться к этому компьютеру. Используя консольную команду получить ip адрес устройства, на котором вы работаете, от DHCP сервера.

DHCP - это клиент-серверный протокол динамической конфигурации хоста (Dynamic Host Configuration Protocol), с помощью которого в ИТ-инфраструктуре сетевые параметры каждого нового устройства прописываются автоматически.

![3.7](materials/3.7.jpg)

Определить и вывести на экран внешний ip-адрес шлюза (ip) и внутренний IP-адрес шлюза, он же ip-адрес по умолчанию (gw):
![3.8](materials/3.8.jpg)
![3.9](materials/3.9.jpg)

Зададим статичные (заданные вручную, а не полученные от DHCP сервера) настройки ip, gw, dns (использовать публичный DNS серверы, например 1.1.1.1 или 8.8.8.8).

![3.10](materials/3.10.jpg)
![3.11](materials/3.11.jpg)
![3.12](materials/3.12.jpg)

проверим изменения и пропингуем адреса
![3.13](materials/3.13.jpg)
![3.12](materials/3.14.jpg)
![3.12](materials/3.15.jpg)

## Part 4
обновим систему
![4ю1](materials/4.1.jpg)

## Part 5

выдаем права доступа для пользовыателя созданного в Part 2
![5.1](materials/5.1.jpg)

сменим hostname от имени нового пользователя

![alt text](materials/5..2.png)

## Part 6

Настроить службу автоматической синхронизации времени.
![alt text](materials/6.1.jpg)

## Part 7

Установка текстовых редакторов    
![alt text](materials/7.1.jpg)

создадим файл test_vim.txt, выход ESC + :wq

![alt text](materials/7.2.jpg)

создадим файл test_nano.txt, выход CTRL + O + X 

![alt text](materials/7.3.jpg)

создадим файл test_mcedit.txt, выход F2 + F10 

![alt text](materials/7.4.jpg)

изменим файл test_vim.txt, чтобы выйти без сохранения ESC + : q!

![alt text](materials/7.5.jpg)

изменим файл test_nano.txt, чтобы выйти без сохранения CTRL + X + N

![alt text](materials/7.6.jpg)

изменим файл test_mcedit.txt, чтобы выйти без сохранения  F10  + No

![alt text](materials/7.7.jpg)

выполним поиск по файлам

vim:
поиск
![alt text](materials/7.8.jpg)

замена 
![alt text](materials/7.9.jpg)

nano: поиск ^W
![alt text](materials/7.10.jpg)

замена  ^\\
![alt text](materials/7.11.jpg)

mcedit: поиск F7

![alt text](materials/7.12.jpg)

замена F4
![alt text](materials/7.13.jpg)

## Part 8

![alt text](materials/7.14.jpg)
![alt text](materials/7.15.jpg)
не получилось, решаем проблему
![alt text](materials/7.16.jpg)
проблема решилась
![alt text](materials/7.17.jpg)

![alt text](materials/7.18.jpg)
![alt text](materials/7.119.jpg)
![alt text](materials/7.19.jpg)
![alt text](materials/7.20.jpg)
Используя команду ps, показать наличие процесса sshd. Для этого к команде нужно подобрать ключи.
![alt text](materials/7.21.jpg)
-tan:

t-по протоколу TCP

a-Отображение всех подключений и ожидающих портов.

n- Отображение адресов и номеров портов в числовом формате.

Cтолбцы:

Recv-Q -количество запросов в очередях на приём на данном узле/компьютере

Send-Q -количество запросов в очередях на отправку на данном узле/компьютере

Local Address - адрес и номер локального конца сокета

Foreign Address - адрес и номер порта удаленного порта сокета

State - состояние сокета

Если в качестве адреса отображается 0.0.0.0 , то это означает - "любой адрес", т. е в соединении могут использоваться все IP-адреса существующие на данном компьютере.
![alt text](materials/7.22.jpg)
ps -aux | grep sshd output:

ps-выводит список текущих процессов на вашем сервере в виде таблицы

a-выбрать все процессы, кроме фоновых;

u-выбрать процессы пользователя.

x-заставляет ps перечислить все процессы, принадлежащие вам

## Part 9

### Top
![alt text](materials/9.1.jpg)

uptime
![alt text](materials/9.2.jpg)

кол-во пользователей
![alt text](materials/9.3.jpg)

загрузка системы
![alt text](materials/9.4.jpg)

кол-во процессов
![alt text](materials/9.5.jpg)

загрузка CPU
![alt text](materials/9.6.jpg)

Загрузка памяти
![alt text](materials/9.7.jpg)

сортировка процессов по количеству занимаемой памяти
![alt text](materials/9.8.jpg)

сортировка процесов процессорному времени
![alt text](materials/9.9.jpg)

### Htop

Pid
![alt text](materials/9.10.jpg)

CPU
![alt text](materials/9.11.jpg)

MEM
![alt text](materials/9.12.jpg)

TIME
![alt text](materials/9.13.jpg)

sshd
![alt text](materials/9.14.jpg)

hostname, time, uptime
![alt text](materials/9.15.jpg)


## Part 10

запустить утилиту fdisk -l
![alt text](materials/10.1.jpg)

имяБ размер 10 Gb
![alt text](materials/10.2.jpg)

количество секторов 20971520
![alt text](materials/10.3.jpg)

## Part 11

### df
для корневого раздела
![alt text](materials/11.1.jpg)
размер раздела 1028772

размер занятого пространства 4515276

размер свободного пространства 5162824

процент использованной памяти 47%

df -Th для корневого раздела 
![alt text](materials/11.2.jpg)

размер раздела 9.8

используется 4.4 

доступно 5.0

прцент использованной памяти 47%

Tип файловой системы для раздела-ext4

## Part 12
Вывести размер папок /home, /var, /var/log (в байтах)
![alt text](materials/12.1.jpg)
![alt text](materials/12.2.jpg)

Вывести размер всего содержимого в /var/log (не общее, а каждого вложенного элемента, используя *)

![alt text](materials/12.4.jpg)
![alt text](materials/12.3.jpg)

## Part 13
установим утилиту ncdu
проверим /home /var /var/log
![alt text](materials/13.1.jpg)
![alt text](materials/13.2.jpg)
![alt text](materials/13.3.jpg)

## Part 14
dmesg
![alt text](materials/14.1.jpg)
syslog
![alt text](materials/14.2.jpg)
auth
![alt text](materials/14.3.jpg)

время последней успешной авторизации- 2024-06-25 02:41:14

имя пользователя-user-1

метод входа в систему-sudo

Перезапустить службу SSHd.
![alt text](materials/14.4.jpg)

## Part 15
запишем команду в расписание crontab
![alt text](materials/15.0.jpg)

проверим ее работу по syslog
![alt text](materials/15.1.jpg)

удалим все записи и проверим их наличие
![alt text](materials/15..2.jpg)
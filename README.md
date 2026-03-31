# Домашнее задание к занятию "`Docker. Часть 2`" - `Анастасиев Дмитрий`


### Инструкция по выполнению домашнего задания

   1. Сделайте `fork` данного репозитория к себе в Github и переименуйте его по названию или номеру занятия, например, https://github.com/имя-вашего-репозитория/git-hw или  https://github.com/имя-вашего-репозитория/7-1-ansible-hw).
   2. Выполните клонирование данного репозитория к себе на ПК с помощью команды `git clone`.
   3. Выполните домашнее задание и заполните у себя локально этот файл README.md:
      - впишите вверху название занятия и вашу фамилию и имя
      - в каждом задании добавьте решение в требуемом виде (текст/код/скриншоты/ссылка)
      - для корректного добавления скриншотов воспользуйтесь [инструкцией "Как вставить скриншот в шаблон с решением](https://github.com/netology-code/sys-pattern-homework/blob/main/screen-instruction.md)
      - при оформлении используйте возможности языка разметки md (коротко об этом можно посмотреть в [инструкции  по MarkDown](https://github.com/netology-code/sys-pattern-homework/blob/main/md-instruction.md))
   4. После завершения работы над домашним заданием сделайте коммит (`git commit -m "comment"`) и отправьте его на Github (`git push origin`);
   5. Для проверки домашнего задания преподавателем в личном кабинете прикрепите и отправьте ссылку на решение в виде md-файла в вашем Github.
   6. Любые вопросы по выполнению заданий спрашивайте в чате учебной группы и/или в разделе “Вопросы по заданию” в личном кабинете.
   
Желаем успехов в выполнении домашнего задания!
   
### Дополнительные материалы, которые могут быть полезны для выполнения задания

1. [Руководство по оформлению Markdown файлов](https://gist.github.com/Jekins/2bf2d0638163f1294637#Code)

---

### Задание 1

**Напишите ответ в свободной форме, не больше одного абзаца текста.**

Установите Docker Compose и опишите, для чего он нужен и как может улучшить лично вашу жизнь.

### Решение 1
Docker Compose нужен для автоматизации запуска многоконтейнерных приложений.
Вся конфигурация описывается в файле в формате YAML и может хранится в системе контроля версий. Поможет в разработке, тестировании и демонстрации сложных приложений в изолированной среде. 

---

### Задание 2 

**Выполните действия и приложите текст конфига на этом этапе.** 

Создайте файл docker-compose.yml и внесите туда первичные настройки: 

 * version;
 * services;
 * volumes;
 * networks.

При выполнении задания используйте подсеть 10.5.0.0/16.
Ваша подсеть должна называться: <ваши фамилия и инициалы>-my-netology-hw.
Все приложения из последующих заданий должны находиться в этой конфигурации.

### Решение 2

[docker-compose.yml](https://github.com/Dmitry-Anastasiev/homework-6.4_/blob/main/Task2/docker-compose.yml)

---

### Задание 3 

**Выполните действия:** 

1. Создайте конфигурацию docker-compose для Prometheus с именем контейнера <ваши фамилия и инициалы>-netology-prometheus. 
2. Добавьте необходимые тома с данными и конфигурацией (конфигурация лежит в репозитории в директории [6-04/prometheus](https://github.com/netology-code/sdvps-homeworks/tree/main/lecture_demos/6-04/prometheus) ).
3. Обеспечьте внешний доступ к порту 9090 c докер-сервера.

### Решение 3

[docker-compose.yml](https://github.com/Dmitry-Anastasiev/homework-6.4_/blob/main/Task3/docker-compose.yml)

[prometheus.yml](https://github.com/Dmitry-Anastasiev/homework-6.4_/blob/main/Task3/prometheus.yml)

---

### Задание 4 

**Выполните действия:**

1. Создайте конфигурацию docker-compose для Pushgateway с именем контейнера <ваши фамилия и инициалы>-netology-pushgateway. 
2. Обеспечьте внешний доступ к порту 9091 c докер-сервера.

### Решение 4

[docker-compose.yml](https://github.com/Dmitry-Anastasiev/homework-6.4_/blob/main/Task4/docker-compose.yml)

[prometheus.yml](https://github.com/Dmitry-Anastasiev/homework-6.4_/blob/main/Task4/prometheus.yml)

---

### Задание 5 

**Выполните действия:** 

1. Создайте конфигурацию docker-compose для Grafana с именем контейнера <ваши фамилия и инициалы>-netology-grafana. 
2. Добавьте необходимые тома с данными и конфигурацией (конфигурация лежит в репозитории в директории [6-04/grafana](https://github.com/netology-code/sdvps-homeworks/blob/main/lecture_demos/6-04/grafana/custom.ini).
3. Добавьте переменную окружения с путем до файла с кастомными настройками (должен быть в томе), в самом файле пропишите логин=<ваши фамилия и инициалы> пароль=netology.
4. Обеспечьте внешний доступ к порту 3000 c порта 80 докер-сервера.

### Решение 5

[docker-compose.yml](https://github.com/Dmitry-Anastasiev/homework-6.4_/blob/main/Task5/docker-compose.yml)

[prometheus.yml](https://github.com/Dmitry-Anastasiev/homework-6.4_/blob/main/Task5/prometheus.yml)

[grafana.ini](https://github.com/Dmitry-Anastasiev/homework-6.4_/blob/main/Task5/grafana.ini)

---

### Задание 6 

**Выполните действия.**

1. Настройте поочередность запуска контейнеров.
2. Настройте режимы перезапуска для контейнеров.
3. Настройте использование контейнерами одной сети.
5. Запустите сценарий в detached режиме.

### Решение 6

[docker-compose.yml](https://github.com/Dmitry-Anastasiev/homework-6.4_/blob/main/Task6/docker-compose.yml)

[prometheus.yml](https://github.com/Dmitry-Anastasiev/homework-6.4_/blob/main/Task6/prometheus.yml)

[grafana.ini](https://github.com/Dmitry-Anastasiev/homework-6.4_/blob/main/Task6/grafana.ini)

---

### Задание 7 

**Выполните действия.**
1. Выполните запрос в Pushgateway для помещения метрики <ваши фамилия и инициалы> со значением 5 в Prometheus: ```echo "<ваши фамилия и инициалы> 5" | curl --data-binary @- http://localhost:9091/metrics/job/netology```.
2. Залогиньтесь в Grafana с помощью логина и пароля из предыдущего задания.
3. Cоздайте Data Source Prometheus (Home -> Connections -> Data sources -> Add data source -> Prometheus -> указать "Prometheus server URL = http://prometheus:9090" -> Save & Test).
4. Создайте график на основе добавленной в пункте 5 метрики (Build a dashboard -> Add visualization -> Prometheus -> Select metric -> Metric explorer -> <ваши фамилия и инициалы -> Apply.

В качестве решения приложите:

* docker-compose.yml **целиком**;
* скриншот команды docker ps после запуске docker-compose.yml;
* скриншот графика, постоенного на основе вашей метрики.

### Решение 7

[docker-compose.yml](https://github.com/Dmitry-Anastasiev/homework-6.4_/blob/main/Task7/docker-compose.yml)

[prometheus.yml](https://github.com/Dmitry-Anastasiev/homework-6.4_/blob/main/Task7/prometheus.yml)

[grafana.ini](https://github.com/Dmitry-Anastasiev/homework-6.4_/blob/main/Task7/grafana.ini)

Скриншот docker ps смотрите в решении 8

<img width="1133" height="571" alt="image" src="https://github.com/Dmitry-Anastasiev/Homework-6.4/blob/main/Task7/image1.png" />

<img width="1915" height="1003" alt="image" src="https://github.com/Dmitry-Anastasiev/Homework-6.4/blob/main/Task7/image2.png" />

---

### Задание 8

**Выполните действия:** 

1. Остановите и удалите все контейнеры одной командой.

В качестве решения приложите скриншот консоли с проделанными действиями.

### Решение 8

<img width="1214" height="454" alt="image" src="https://github.com/Dmitry-Anastasiev/Homework-6.4/blob/main/Task8/image3.png" />

---

## Дополнительные задания* (со звёздочкой)

Их выполнение необязательное и не влияет на получение зачёта по домашнему заданию. Можете их решить, если хотите лучше разобраться в материале.

---

### Задание 9* 

**Выполните действия:** 

1. Создайте конфигурацию docker-compose для Alertmanager с именем контейнера <ваши фамилия и инициалы>-netology-alertmanager. 
2. Добавьте необходимые тома с данными и [конфигурацией](https://github.com/netology-code/sdvps-homeworks/tree/main/6-04/alertmanager), сеть, режим и очередность запуска.
3. Обновите конфигурацию Prometheus (необходимые изменения ищите в презентации или документации) и перезапустите его. 
4. Обеспечьте внешний доступ к порту 9093 c докер-сервера.

В качестве решения приложите скриншот с событием из Alertmanager.

### Решение 9

<img width="1279" height="800" alt="image" src="https://github.com/Dmitry-Anastasiev/Homework-6.4/blob/main/Task9/image4.png" />

---

### Задание 10* 

Запустите свой сценарий на чистом железе без предзагруженных образов.

**Ответьте на вопросы в свободной форме:**

1. Опишите выполненный вами процесс развертывания сценария.
2. Как вы думаете зачем может понадобиться такой способ развертывания?

### Решение 10

Процесс равертывания осуществляется одной командой и не занимает много времени, что влияет на повторное развертывание и масштабирование решения.
Таким образом можно быстро развернуть готовое решение до рабочего состояния.

<img width="1111" height="810" alt="image" src="https://github.com/Dmitry-Anastasiev/Homework-6.4/blob/main/Task10/image5.png" />

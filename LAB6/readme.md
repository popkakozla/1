# Лабораторная работа номер 6 — Bash скрипты на Raspberry Pi

## Цель работы
Подключиться к Raspberry Pi по протоколу SSH, создать и запустить bash-скрипты.

---

## Подключение по SSH

Для подключения использовалась команда:

```bash
ssh user@192.168.129.150

## Скрипты:
#!/bin/bash

echo $(date)

echo "Ostapenko"

read -p "Input your birth year: " age

year=$(date +%Y)

if (( year - age > 17 )); then
    echo "You are adult"
else
    echo "You are not adult"
fi

#!/bin/bash

# Запрашиваем фамилию пользователя
read -p "Введите вашу фамилию: " lastname

# Запрашиваем дату рождения
read -p "Введите дату рождения (дд.мм.гггг): " birthdate

# Получаем день из даты
day=$(echo "$birthdate" | cut -d'.' -f1)

# Получаем месяц из даты
month=$(echo "$birthdate" | cut -d'.' -f2)

# Получаем год из даты
year=$(echo "$birthdate" | cut -d'.' -f3)

# Получаем текущий год
current_year=$(date +%Y)

# Получаем текущий месяц
current_month=$(date +%m)

# Получаем текущий день
current_day=$(date +%d)

# Вычисляем возраст
age=$((current_year - year))

# Проверяем, был ли день рождения в этом году
if [[ $current_month -lt $month ]] || ([[ $current_month -eq $month ]] && [[ $current_day -lt $day ]]); then
    age=$((age - 1))
fi

# Выводим итоговое сообщение
echo "Привет, $lastname, тебе $age"

Для подключения использовалась команда:

```bash
ssh user@192.168.129.150

---

<img width="1365" height="767" alt="1" src="https://github.com/user-attachments/assets/8e80141a-101c-4e73-a639-12ea79729c9f&quot; />


# Лабораторная работа №6 — Bash-скрипты на Raspberry Pi

## Цель работы
Подключиться к Raspberry Pi по протоколу SSH, создать и запустить bash-скрипты.

---

# Подключение по SSH

Для подключения использовалась команда:

```bash
ssh user@192.168.129.150
```

После ввода пароля был получен доступ к Raspberry Pi.

---

# Скрипт №1

## Код скрипта

```bash
#!/bin/bash

echo $(date)

echo "Ostapenko"

read -p "Input your birth year: " age

year=$(date +%Y)

if (( year - age > 17 )); then
    echo "You are adult"
else
    echo "You are not adult"
fi
```

---

# Скрипт №2

## Код скрипта с комментариями

```bash
#!/bin/bash

# Запрашиваем фамилию пользователя
read -p "Введите вашу фамилию: " lastname

# Запрашиваем дату рождения
read -p "Введите дату рождения (дд.мм.гггг): " birthdate

# Получаем день из даты
day=$(echo "$birthdate" | cut -d'.' -f1)

# Получаем месяц из даты
month=$(echo "$birthdate" | cut -d'.' -f2)

# Получаем год из даты
year=$(echo "$birthdate" | cut -d'.' -f3)

# Получаем текущий год
current_year=$(date +%Y)

# Получаем текущий месяц
current_month=$(date +%m)

# Получаем текущий день
current_day=$(date +%d)

# Вычисляем возраст
age=$((current_year - year))

# Проверяем, был ли день рождения в этом году
if [[ $current_month -lt $month ]] || ([[ $current_month -eq $month ]] && [[ $current_day -lt $day ]]); then
    age=$((age - 1))
fi

# Выводим итоговое сообщение
echo "Привет, $lastname, тебе $age"
```

---

# Используемые команды

```bash
nano script.sh
chmod +x script.sh
./script.sh

nano comments.sh
chmod +x comments.sh
./comments.sh
```

---




# Результат

В ходе лабораторной работы было выполнено:

- подключение к Raspberry Pi по SSH
- создание bash-скриптов
- запуск bash-скриптов
- работа с условиями, переменными и пользовательским вводом

<img width="1365" height="767" alt="Скриншот выполнения лабораторной работы" src="https://github.com/user-attachments/assets/8e80141a-101c-4e73-a639-12ea79729c9f" />

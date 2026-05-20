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


# Лабораторная работа — Bash скрипты на Raspberry Pi

## Цель работы
Подключиться к Raspberry Pi по протоколу SSH, создать и запустить bash-скрипты.

---

## Подключение по SSH

Для подключения использовалась команда:

```bash
ssh user@192.168.129.150

<img width="1365" height="767" alt="1" src="https://github.com/user-attachments/assets/8e80141a-101c-4e73-a639-12ea79729c9f" />

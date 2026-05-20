# Лабораторная работа №7 — Работа с процессами в Linux

## Цель работы
Изучить управление процессами в Linux, работу foreground/background процессов и мониторинг системы.

---

# Подключение по SSH

```bash
ssh user@192.168.129.150
```

---

# Основные команды

## Запуск процесса

```bash
sleep 1000
```

## Запуск в фоне

```bash
sleep 1000 &
```

## Просмотр фоновых задач

```bash
jobs
```

## Возврат процесса

```bash
fg 1
```

## Возврат процесса в фон

```bash
bg 1
```

---

# Работа с процессами

## Просмотр процессов

```bash
ps aux
```

## Поиск процесса

```bash
ps aux | grep sleep
```

## Получение PID

```bash
pgrep sleep
```

## Завершение процесса

```bash
kill PID
```

## Завершение всех sleep

```bash
pkill sleep
```

---

# Команда nohup

```bash
nohup sleep 10000 &
```

---

# Мониторинг системы

## Диспетчер задач

```bash
top
```

## Просмотр памяти

```bash
free -h
```

## Время работы системы

```bash
uptime
```

---

# Работа с screen

## Запуск

```bash
screen
```

## Отсоединение

```text
Ctrl + A
D
```

## Возврат

```bash
screen -r
```

---

# Результат

В ходе лабораторной работы были изучены:
- foreground и background процессы
- команды управления процессами
- мониторинг системы Linux
- работа с screen и nohup

<img width="819" height="460" alt="1" src="https://github.com/user-attachments/assets/2bee6e98-2090-4b8f-b921-6fcc089d9b00" />

<img width="1364" height="766" alt="2" src="https://github.com/user-attachments/assets/70cbe064-5410-4b70-9f97-00deb4bebe2a" />

<img width="1365" height="766" alt="3" src="https://github.com/user-attachments/assets/b3d85d0e-6e76-45a1-ae62-f6b871bd95eb" />

<img width="1365" height="766" alt="4" src="https://github.com/user-attachments/assets/c84679a6-e46b-4f01-a08c-094b3ff0b610" />

<img width="1365" height="766" alt="5" src="https://github.com/user-attachments/assets/c7a56fda-32cc-44a0-855f-602d9323d53a" />

<img width="1365" height="766" alt="6" src="https://github.com/user-attachments/assets/f41a78ee-1283-4220-93c9-b8c787f37f90" />

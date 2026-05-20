# Лабораторная работа №5 — Подключение к Raspberry Pi по VNC

## Цель работы
Подключиться к Raspberry Pi по протоколам VNC, RDP и SSH, а также выполнить копирование файлов с помощью SCP.

---

# Подключение по VNC

Для подключения использовалась программа TigerVNC.

IP-адрес Raspberry Pi:

```text
192.168.129.150
```

Данные для входа:

```text
Логин: user
Пароль: 123
```

---

# Подключение по RDP

Для подключения использовалась утилита «Подключение к удаленному рабочему столу».

IP-адрес:

```text
192.168.129.150
```

---

# Подключение по SSH

```bash
ssh user@192.168.129.150
```

---

# Копирование файлов через SCP

## Загрузка файла на Raspberry Pi

```bash
scp vnc.png user@192.168.129.150:"Kirill Ostapenko/"
```

```bash
scp rdp.png user@192.168.129.150:"Kirill Ostapenko/"
```

---

# Скачивание файла с Raspberry Pi

```bash
scp user@192.168.129.150:letunov/file.txt .
```

---

# Использованные команды

```bash
ssh user@192.168.129.150

scp file.txt user@192.168.129.150:/path/

scp user@192.168.129.150:file.txt .
```

---

# Результат

В ходе лабораторной работы было выполнено:

- подключение к Raspberry Pi по VNC
- подключение по RDP
- подключение по SSH
- копирование файлов через SCP
- работа с удаленным рабочим столом Linux
<img width="1365" height="767" alt="1" src="https://github.com/user-attachments/assets/45af5231-c8c2-446c-8d7e-d9976bd91cac" />


<img width="1365" height="767" alt="2" src="https://github.com/user-attachments/assets/ba3d914c-d7d5-40c6-8fdf-a41ff40b3244" />


<img width="1365" height="520" alt="image-20-05-26-10-05" src="https://github.com/user-attachments/assets/fc1031b2-2bd9-467d-b72b-5df240edb54d" />

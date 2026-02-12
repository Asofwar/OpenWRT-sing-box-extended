# 📦 sing-box-extended Installer

Автоматический установщик и обновлятор [sing-box-extended](https://github.com/shtorm-7/sing-box-extended) для OpenWrt.

## ✨ Возможности

- 🔄 **Автообновление** — скачивает последнюю версию с GitHub
- 🧠 **Умная проверка** — пропускает обновление, если уже стоит последняя версия
- 🏗 **Мультиархитектура** — поддержка ARM, x86, MIPS, RISC-V и других платформ
- 🔧 **Автовыбор клиента** — использует `curl` если доступен, иначе `wget`
- 📦 **Совместимость** — работает с сервисами `podkop` и `sing-box`
- 💾 **Экономия RAM** — адаптивный выбор рабочей директории в зависимости от свободной памяти

## 🚀 Использование

### Однострочная установка

```sh
sh <(wget -O - https://raw.githubusercontent.com/EikeiDev/OpenWRT-sing-box-extended/refs/heads/main/install.sh)
```

Или через `curl`:

```sh
sh <(curl -fsSL https://raw.githubusercontent.com/EikeiDev/OpenWRT-sing-box-extended/refs/heads/main/install.sh)
```

### Ручной запуск

```sh
wget -O install.sh https://raw.githubusercontent.com/EikeiDev/OpenWRT-sing-box-extended/refs/heads/main/install.sh
sh install.sh
```

## 🖥 Поддерживаемые архитектуры

| Архитектура | Платформы |
|---|---|
| `aarch64` | Raspberry Pi 4/5, Xiaomi, большинство современных роутеров |
| `armv7` | Raspberry Pi 2/3, старые роутеры |
| `armv6` | Raspberry Pi 1/Zero |
| `x86_64` | ПК, виртуальные машины, серверы |
| `i386 / i686` | Старые x86 системы |
| `mips` | TP-Link, старые роутеры (big-endian) |
| `mipsle` | Некоторые роутеры Xiaomi, Netgear (little-endian) |
| `mips64 / mips64le` | Высокопроизводительные MIPS-устройства |
| `riscv64` | RISC-V платы |
| `s390x` | IBM zSeries |

## 📋 Пример вывода

**Обновление доступно:**
```
[*] Проверяю обновления...
[*] Текущая: 1.12.16-extended-1.5.2 | Последняя: v1.12.17-extended-1.5.3
[*] Скачиваю и устанавливаю...
[+] Готово: 1.12.16-extended-1.5.2 -> 1.12.17-extended-1.5.3
```

**Уже последняя версия:**
```
[*] Проверяю обновления...
[*] Текущая: 1.12.17-extended-1.5.3 | Последняя: v1.12.17-extended-1.5.3
[+] Уже установлена последняя версия. Обновление не требуется.
```

## ⚙️ Требования

- OpenWrt (или любой Linux)
- `wget` или `curl`
- Доступ в интернет (GitHub API + GitHub Releases)

## 📄 Благодарности

https://github.com/shtorm-7/sing-box-extended

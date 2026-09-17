# mia-1 backup

Конфигурация сервера ProCloud MIA-1 (84.75.220.37).

## Что здесь

- `config.json` — конфиг Xray (`/usr/local/x-ui/bin/config.json`)
- `x-ui.db` — база панели 3x-ui (`/etc/x-ui/x-ui.db`), содержит инбаунды и клиентов
- `sysctl.conf` — BBR, UDP-буферы
- `sshd_config` — root запрещён, пароли отключены
- `olcrtc-config.yaml` — конфиг olcRTC (эксперимент, отложен)

## Восстановление

1. Поставить 3x-ui
2. `systemctl stop x-ui`
3. Положить `x-ui.db` в `/etc/x-ui/`
4. `systemctl start x-ui` — конфиг Xray сгенерится из базы

## Внимание

Репозиторий приватный. В базе — UUID клиентов и приватные ключи Reality.

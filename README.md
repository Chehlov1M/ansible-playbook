# Отчёт по ДЗ: Работа с roles

## Репозитории
- vector-role: https://github.com/Chehlov1M/vector-role
- lighthouse-role: https://github.com/Chehlov1M/lighthouse-role
- playbook: https://github.com/Chehlov1M/ansible-playbook

## Описание решения
- ClickHouse: роль из Galaxy (AlexeySetevoi), версия 1.13.
- Vector: собственная роль, собирает логи nginx и отправляет в ClickHouse.
- LightHouse: собственная роль, разворачивает статический UI через nginx.

## Ключевые моменты
- Переменные разнесены: публичные — в `defaults`, внутренние — в `vars`.
- Конфиги вынесены в `templates`.
- Версии ролей зафиксированы семантическими тегами (1.0.0).
- В плейбуке зависимости LightHouse реализованы через `pre_tasks`.

# Контейнеры mihomo для RouterOS
- Mihomo это форк открытого проекта Clash с дополнительными уникальными функциями.
# Общее описание контейнеров:
RouterOS не поддерживает nftables, контейнеры собраны на базе alpine linux 3.18 где по умолчанию используется iptables-legacy, это необходимо для работы переменной auto-redirect: true на tun интерфейсе, которая сильно ускоряет обработку tcp трафика. Установлена переменная окружения DISABLE_NFTABLES=1 для mihomo отключающая nftables.
# Контейнеры:
- 📦 [`mihomo`](https://github.com/vanes32/mihomo/pkgs/container/mihomo%2Fmihomo) Контейнер настраивается через конфиг-файл.
- 📦 [`stupid_tun`](https://github.com/vanes32/mihomo/pkgs/container/mihomo%2Fstupid_tun) Контейнер настраивается переменными env.

📚 [Примеры использования в Wiki](https://github.com/vanes32/mihomo/wiki)
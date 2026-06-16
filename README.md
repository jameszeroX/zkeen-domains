## Список доменов выборочной маршрутизации для проекта XKeen
> [!WARNING]
> Данный материал подготовлен в научно-технических и ознакомительных целях. Автор не несёт ответственности за иное использование предоставленного материала. Перед использованием убедитесь, что ваши действия соответствуют законодательству вашей страны. Использование в противоправных целях строго запрещено. Коммерческая эксплуатация предоставленного материала не допускается.

Подробнее о проекте XKeen <https://forum.keenetic.ru/topic/16899-xkeen/>

Форк XKeen <https://github.com/jameszeroX/XKeen>

Telegram <https://t.me/+8Cvh7oVf6cE0MWRi>

FAQ <https://jameszero.net/faq-xkeen.htm>

ZKeen в первую очередь рекомендован для роутеров Keenetic с малым объемом оперативной памяти, но может быть использован и в топовых мощных моделях.

С помощью данного списка вы можете получить доступ к сайтам, которые ограничили доступ для пользователей из России и не только.

Рекомендую использовать ZKeen совместно со списком IP-подсетей - <https://github.com/jameszeroX/zkeen-ip>

Для тестирования подключения в сборку включены следующие ресурсы:
- <https://ip.me> - определение вашего IP-адреса
- <https://browserleaks.com> - комплексное тестирование
- <https://nperf.com> - замер скорости

## Ссылка для загрузки актуальной версии

- <https://github.com/jameszeroX/zkeen-domains/releases/latest/download/zkeen.dat>

### Пример маршрутизации
Применены все возможные категорий zkeen.dat и zkeenip.dat

```json
{
  "routing": {
    "rules": [
      {
        "network": "udp",
        "port": "443",
        "ip": [
          "ext:zkeenip.dat:!ru"
        ],
        "outboundTag": "block"
      },
      {
        "ip": [
          "ext:zkeenip.dat:discord"
        ],
        "network": "udp",
        "port": "19200-19400,50000-50100",
        "outboundTag": "vless-reality"
      },
      {
        "domain": [
          "ext:zkeen.dat:domains",
          "ext:zkeen.dat:other",
          "ext:zkeen.dat:politic",
          "ext:zkeen.dat:youtube"
        ],
        "outboundTag": "vless-reality"
      },
      {
        "ip": [
          "ext:zkeenip.dat:akamai",
          "ext:zkeenip.dat:amazon",
          "ext:zkeenip.dat:arelion",
          "ext:zkeenip.dat:azure",
          "ext:zkeenip.dat:bunnycdn",
          "ext:zkeenip.dat:cdn77",
          "ext:zkeenip.dat:cloudflare",
          "ext:zkeenip.dat:colocrossing",
          "ext:zkeenip.dat:contabo",
          "ext:zkeenip.dat:digitalocean",
          "ext:zkeenip.dat:fastly",
          "ext:zkeenip.dat:frantech",
          "ext:zkeenip.dat:gcore",
          "ext:zkeenip.dat:google",
          "ext:zkeenip.dat:hetzner",
          "ext:zkeenip.dat:leaseweb",
          "ext:zkeenip.dat:linode",
          "ext:zkeenip.dat:liquidweb",
          "ext:zkeenip.dat:mega",
          "ext:zkeenip.dat:melbicom",
          "ext:zkeenip.dat:meta",
          "ext:zkeenip.dat:oracle",
          "ext:zkeenip.dat:ovh",
          "ext:zkeenip.dat:scaleway",
          "ext:zkeenip.dat:telegram",
          "ext:zkeenip.dat:vodafone",
          "ext:zkeenip.dat:vultr",
          "ext:zkeenip.dat:youtube"
        ],
        "outboundTag": "vless-reality"
      },
      {
        "network": "tcp,udp",
        "outboundTag": "direct"
      }
    ]
  }
}

## Источники
- https://github.com/dartraiden/no-russia-hosts
- https://github.com/itdoginfo/allow-domains
- https://community.antifilter.download
- Собственные наблюдения

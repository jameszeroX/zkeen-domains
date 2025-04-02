## Список доменов выборочной маршрутизации для проекта XKeen
> [!WARNING]
> Данный материал подготовлен в научно-технических целях.
> Автор не несёт ответственности за иное использование предоставленного материала.
> **Исходники dat-файла не публикуются.** Подразумевается, что его нужно использовать "как есть", а не копаться в нём.
> Коммерческая эксплуатация не допускается. При нарушении данного условия, публичное обновление проекта прекратится.
> Если Вы не согласны с вышеуказанным, немедленно удалите со всех своих устройств любой загруженный из даннного репозитория материал.

Подробнее о проекте XKeen по ссылке <https://forum.keenetic.ru/topic/16899-xkeen/>

Telegram <https://t.me/+SZWOjSlvYpdlNmMy>

FAQ <https://jameszero.net/faq-xkeen.htm>

ZKeen в первую очередь рекомендован для роутеров Keenetic с малым объемом оперативной памяти, но может быть использован и в топовых мощных моделях.

С помощью данного списка вы можете получить доступ к сайтам, которые ограничили доступ для пользователей из России и не только.

Рекомендую использовать ZKeen совместно со списком IP-подсетей - <https://github.com/jameszeroX/zkeen-ip>

Для тестирования в сборку включены следующие ресурсы:
- <https://ip.me> - определение вашего IP-адреса
- <https://browserleaks.com> - комплексное тестирование
- <https://nperf.com> - замер скорости

## Зеркала для загрузки крайней версии

- <https://github.com/jameszeroX/zkeen-domains/releases/latest/download/zkeen.dat>
- <https://cdn.jsdelivr.net/gh/jameszeroX/zkeen-domains@master/zkeen.dat>

## Пример маршрутизации

```json
{
  "routing": {
    "rules": [
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
        "network": "tcp,udp",
        "outboundTag": "direct"
      }
    ]
  }
}
```

## Самостоятельная сборка `zkeen.dat`

- Установите `golang` и `git` (например `apt install golang git` для Ubuntu 20+)
- Клонируйте код проекта: `git clone https://github.com/jameszeroX/zkeen-domains.git`
- Перейдите в корневую директорию проекта: `cd zkeen-domains`
- Установите зависимости проекта: `go mod download`
- Отредактируйте по необходимости файлы в директории `/data/`
- Выполните сборку командой: `go run ./`
- Используйте созданный в корневой директории проекта файл `zkeen.dat`
- Be happy!

## Источники
- https://github.com/dartraiden/no-russia-hosts
- https://github.com/itdoginfo/allow-domains
- https://community.antifilter.download
- Собственные наблюдения

## Поддержка
Желающие угостить меня пивом) могут сделать это в кошельке Telegram
- Монета USDT, сеть TRC20:
```
TB9dLwzNdLB6QeKV6w4FjCACSarePb32Dg
```
- Монета USDT, сеть TON:
```
UQDHmmyz0e1K07Wf7aTVtdmcGzCPfo4Pf7uBi_Id8TDI6Da6
```


# T-Tech Autofollow SDK

[![PyPI](https://img.shields.io/gitlab/v/release/240?gitlab_url=https%3A%2F%2Fopensource.tbank.ru)](https://opensource.tbank.ru/invest/invest-autofollow/-/packages)
[![PyPI - Python Version](https://img.shields.io/python/required-version-toml?tomlFilePath=https://opensource.tbank.ru/invest/invest-autofollow/-/raw/master/pyproject.toml)](https://www.python.org/downloads/)
![Opensource](https://img.shields.io/gitlab/license/240?gitlab_url=https%3A%2F%2Fopensource.tbank.ru)
<!-- ![PyPI - Downloads](https://img.shields.io/pypi/dm/ttech-autofollow-sdk) -->

Данный репозиторий предоставляет клиент для взаимодействия ведущих стратегий автоследования с API [Т-Инвестиций]((https://developer.tbank.ru/invest/intro/intro)) на языке Python.

- [Документация по API](https://developer.tbank.ru/invest/services/autofollow/head-autofollow)

## Начало работы

<!-- terminal -->

```
$ pip install ttech-autofollow-sdk --index-url https://opensource.tbank.ru/api/v4/projects/240/packages/pypi/simple
```

## Возможности

- REST клиент;
- получить список инструментов, доступных для автоследования;
- получить список стратегий автора;
- создать новый сигнал;
- создать отложенный сигнал;
- получить позицию портфеля для заданной стратегии;
- получить активные и отложенные сигналы;
- снять активные и отложенные сигналы.

## Как пользоваться

### Получить список стратегий автора

```python
from ttech_autofollow import Client

TOKEN = 'token'

with Client(access_token=TOKEN) as client:
    print(client.strategy_api.get_autofollow_strategies())
```

> :warning: **Не публикуйте токены в общедоступные репозитории**<br/><br/>
> Один из вариантов сохранения токена - использование [environment variables](https://opensource.tbank.ru/invest/invest-autofollow/-/blob/master/examples/get_strategies.py).

Остальные примеры доступны в [examples](https://opensource.tbank.ru/invest/invest-autofollow/-/tree/master/examples).


## License

Лицензия [The Apache License](https://opensource.tbank.ru/invest/invest-autofollow/-/blob/master/LICENSE).

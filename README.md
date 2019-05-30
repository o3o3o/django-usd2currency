# Convert value from usd to currency

Simple and free usd2currency convert utils,
by caching free-limited-api from apilayer.com

## Quick start

* Install::

``` 
   pip install django-usd2currency
```

* Add `APILAYER_ACCESS_KEY` to your setting like this::

```
   # Get free api from https://currencylayer.com/signup/free
   APILAYER_ACCESS_KEY = 'xxxxxxxxxxx'
```

* Start to use it in code

```
   from django_usd2currency.utils import usd2currency
   print(usd2currency(1, currency='CNY'))

   from django_usd2currency.utils import get_rate_from_usd
   print(get_rate_from_usd(currency='JPY'))
```

1. Use [redis as cache backend](https://niwinz.github.io/django-redis/latest/#_configure_as_cache_backend) to lock in the multiprocess env.


## Settings

* `APILAYER_ACCESS_KEY`: *required*
*
* `APILAYER_CURRENCIES`: target currencies
    Default is `['CNY', 'EUR', 'JPY', 'KRW']`


## TODO:

* write test

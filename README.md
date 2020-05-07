# Django Channel set
## 1. Add INSTALLED_APPS
```python
INSTALLED_APPS = [
    ...
    'channels',
    ...
]
```
## 2. set ASGI_APPLICATION
```python
ASGI_APPLICATION = "hada_backed.routing.application"
```
## 3. redis set
```python
CHANNEL_LAYERS = {
    'default': {
        'BACKEND': 'channels_redis.core.RedisChannelLayer',
        'CONFIG': {
            "hosts": [('127.0.0.1', 6379)],
        },
    },
}
```
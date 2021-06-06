# celery_docker_demo
Basic Celery and Docker code

Runs on the same network:
- A Redis instance
- A RedisInsight instance
- A Celery application managing the workers

Afterwards, you can call Celery from a python interpreter on the same network with:
```
from app.tasks import add
result = add.delay(4, 4)
print(result.get())
```

## Celery란
- 파이썬에서 비동기 작업을 처리하기 위한 도구
- 특히, 복잡한 작업을 배경에서 실행하고 결과를 나중에 받아올 때 유용하게 활용된다
- 예를 들어, 이메일 발송, 파일 처리, 데이터 분석 등 시간이 오래 걸리는 작업들을 메인 프로그램의 흐름을 방해하지 않고 처리할 수 있다.

## RabbiMQ
- RabbitMQ는 Celery와 함께 자주 사용되는 메시지 브로커이다.
- 메시지 브로커라는 작업을 수행해야 할 워커들에게 작업을 분배하고, 작업 결과를 수집하는 역할을 한다
- Celery는 RabbitMQ 이외도, Redis, Amazon SQS 등 다양한 메시지 브로커를 지원하지만, RabbitMQ가 가장 일반적으로 사용되는 메시지 브로커이다

## Celery 장점
- 비동기 처리
    - 메인 프로그램의 흐름을 방해하지 않고 작업을 수행할 수 있다 
- 분산 처리
    - 여러 워커를 사용하여 작업을 분산 처리할 수 있다
- 오류 처리
    - 작업 실패 시 재시도, 에러 알림 등 다양한 오류 처리 기능을 제공 
- 확장성
    - 시스템 부하에 따라 워커를 추가하거나 제거하여 시스템을 확장할 수 있다
    
## Celery 사용 예시
```python
from celery import Celery

app = Celery('tasks', broker='amqp://guest@localhost//')

@app.task
def add(x, y):
    return x + y

result = add.delay(4, 5)
print(result.get())  # 결과 출력: 9
```

## Celery 주요 개념
- Task: 실행할 작업을 정의하는 단위입니다.
- Worker: 작업을 수행하는 프로세스입니다.
- Broker: 메시지를 중개하는 서버입니다. (예: RabbitMQ)
- Backend: 작업의 상태를 저장하고 결과를 저장하는 저장소입니다. (예: Redis, Database)

## Celery와 RabbitMQ가 함께 작동하는 방식
- 작업 생성:
파이썬 코드에서 Celery의 @task 데코레이터를 사용하여 작업을 정의합니다.
작업이 호출되면, Celery는 작업 정보를 RabbitMQ에 메시지로 보냅니다.

- 작업 소비:
RabbitMQ에서 메시지를 받은 워커는 해당 작업을 실행합니다.
작업이 완료되면, 결과를 다시 RabbitMQ에 보냅니다.

- 결과 수집:
원래 작업을 호출한 코드는 RabbitMQ에서 결과 메시지를 받아 처리합니다.
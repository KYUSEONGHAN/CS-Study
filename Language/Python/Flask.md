## Flask란?
- 파이썬으로 작성된 경량 웹 프레임워크
- Django처럼 무겁고 복잡한 기능들을 모두 포함하고 있지는 않지만, 필요한 기능만을 간결하게 구현하여 빠르고 유연하게 웹 개발을 가능하게 한다

## 특징
- 간결함
- 유연성
    - 다양한 확장 모듈을 통해 필요한 기능을 추가할 수 있다
- Pythonic
    - 파이썬의 장점을 최대한 활용하여 개발 생산성을 높인다
- Werkzeug
    - 강력한 WSGI 툴킷을 기반으로 안정적이 웹 서버 기능을 제공
- Jinja2
    - 파워풀한 템플릿 엔진을 통해 동적인 웹 페이지를 생성
    
## Flask 기본 구조
```python
from flask import Flask

app = Flask(__name__)

@app.route('/')
def hello():
    return 'Hello, World!'

if __name__ == '__main__':
    app.run()
```
- Flask(__name__): Flask 애플리케이션 객체 생성
- @app.route('/'): URL과 함수를 연결
- return: 클라이언트에게 전달할 응답

## Flask 주요 기능
- Routing: URL과 함수를 연결하여 요청을 처리합니다.
- Templates: Jinja2 템플릿 엔진을 사용하여 동적인 웹 페이지를 생성합니다.
- Request and Response: HTTP 요청과 응답을 처리합니다.
- Session: 사용자 세션 관리를 지원합니다.
- Database: SQLAlchemy 등 다양한 ORM을 통해 데이터베이스를 연결합니다.

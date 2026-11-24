# my_projects
CI/CD를 위한 프로젝트. 간단한 대시보드 구성

# 사용 소프트웨어
    - 백엔드    : fastapi, uvicorn
    - 프런트    : 부트스트랩 기반 adminlte 제품 4.0.0 버전 사용
    - db 서버 x / web 서버 x

# 로컬 PC에 python 가상환경 구성

```
# 가상환경 구성
python -m venv dev
# 가상환경 활성화
.\dev\Scripts\activate.bat
or
source dev/bin/activate

# 가상환경 진입 형태
(dev) >

# 패키지 설치
 (dev) > pip install -r requirements.txt
...

# 코드 작성
- main.py

# 서버 가동

```
# uvicorn 모듈명(엔트리포인트):<FastAPI명> 옵션
@ --reload L 코드 수정 => 저장 => 감지 => 재가동 : 수정된  내용을 자동으로 반영하는 옵션

uvicorn main:app --reload
```
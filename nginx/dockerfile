# 베이스 이미지 -> 경량버전 조정
FROM python:3.14.0-slim

# 워킹 디렉토리 지정(컨테이너 특정 경로)
WORKDIR /app

# 웹개발시 사용했던 패키지 목록 파일 카피
# 도커 파일 옆에 있는 requirements.txt 파일을 컨테이너 워킹 디렉토리에 카피
COPY requirements.txt .

# 패키지 설치
RUN pip install --no-cache-dir --upgrade -r requirements.txt

# 웹개발시 개발한 모든 소스/리소스 카피
# main.py만 카피됨
# COPY . . + .dockerignore(제외될 리소스등 기술, 필터링)
COPY main.py .

# 도커 컴포즈에서 컨트롤
# 데몬 구동 -> 서버 가동 (통상 uvicorn 사용)
#CMD ["fastapi", "run", "app/main.py", "--port", "80"]
# 포트는 기본값 8000번
#CMD ["uvicorn", "app.main:app", "--host", "0.0.0.0"]
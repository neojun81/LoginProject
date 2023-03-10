# syntax=docker/dockerfile:1

# 원본이미지
FROM python:3.8-slim-buster

# 작업디렉토리
WORKDIR /app

# pip 패키지목록
COPY requirements.txt requirements.txt
# 패키지모록내용 설치
RUN pip3 install -r requirements.txt
# 이미지 기본 미국 시간설정 내용 삭제
RUN rm -rf /etc/localtime
# 이미지 한국 시간 설정
RUN ln -s /usr/share/zoneinfo/Asia/Seoul /etc/localtime

COPY . .
# 플라스크 실행
CMD ["python3", "-m", "flask", "run", "--host=0.0.0.0"]
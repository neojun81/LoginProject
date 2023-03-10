# syntax=docker/dockerfile:1

FROM postgres:13.8

#로케이션 시간 설정
RUN rm -rf /etc/localtime
RUN ln -s /usr/share/zoneinfo/Asia/Seoul /etc/localtime

FROM nginx:latest

#설정파일 복사
COPY default.conf /etc/nginx/conf.d/default.conf

#시간설정
RUN rm -rf /etc/localtime
RUN ln -s /usr/share/zoneinfo/Asia/Seoul /etc/localtime

#데몬실행
CMD ["nginx", "-g", "daemon off;"]
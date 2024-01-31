FROM openjdk:17-alpine AS builder
WORKDIR /nginx_dockerfile
COPY target/*.jar /nginx_dockerfile/app.jar
RUN mkdir /app-resources && unzip /nginx_dockerfile/app.jar -d /app-resources

FROM nginx
COPY --from=builder /app-resources/BOOT-INF/classes/static/ /usr/share/nginx/html
COPY nginx-conf/nginx.conf /etc/nginx/conf.d/default.conf
CMD ["nginx", "-g", "daemon off;"]
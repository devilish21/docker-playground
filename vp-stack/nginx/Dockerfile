FROM nginx:stable
LABEL Author=DevOps
RUN  rm -rf /etc/nginx/conf.d/default.conf
COPY ./appv1.conf /etc/nginx/conf.d/appv1.conf

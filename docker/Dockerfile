FROM node:14.17.6 AS build_base

RUN mkdir -p /code/ && npm set registry https://registry.npm.taobao.org/
WORKDIR /code
COPY package.json package.json
RUN npm install --force

RUN echo $PWD
ADD /var/jenkins_home/workspace/frontend_test  /code
RUN npm run build

FROM nginx AS deploy

RUN mkdir -p /data/wwwroot/onlineditor
WORKDIR /data/wwwroot/onlineditor
COPY --from=build_base /code/dist /data/wwwroot/onlineditor
COPY ./docker/nginx.conf /etc/nginx/nginx.conf

EXPOSE 80

ENTRYPOINT ["nginx", "-g", "daemon off;"]

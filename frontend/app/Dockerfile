FROM node:14.16.0 as builder
WORKDIR '/build'
COPY app ./app
COPY resources ./resources
COPY third_party ./third_party

WORKDIR '/build/app'

RUN npm config set registry http://registry.cnpmjs.org/
RUN npm config set strict-ssl false
RUN npm install
# RUN npm rebuild node-sass
RUN npm run build

RUN ls /build/app/dist

FROM nginx
EXPOSE 80
COPY --from=builder /build/app/dist /usr/share/nginx/html



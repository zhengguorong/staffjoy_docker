FROM node:14.16.0 as builder

WORKDIR '/build'
COPY myaccount ./myaccount
COPY resources ./resources
COPY third_party ./third_party

WORKDIR '/build/myaccount'

# RUN yarn config set registry http://registry.npm.taobao.org/
RUN npm config set registry http://registry.cnpmjs.org/
RUN npm config set strict-ssl false
RUN npm install
# RUN npm rebuild node-sass
RUN npm run build

RUN ls /build/myaccount/dist

FROM nginx
EXPOSE 80
COPY --from=builder /build/myaccount/dist /usr/share/nginx/html


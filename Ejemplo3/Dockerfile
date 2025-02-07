FROM node:20.18-alpine3.21 AS builder
LABEL stage=builder
RUN apk add git
WORKDIR /web
RUN git clone https://github.com/Pesp05/PopFilms.git .
RUN npm install -g @angular/cli
RUN npm install
RUN ng build --configuration production --aot

FROM nginx:alpine
WORKDIR /web
COPY --from=builder /web/dist/pop-films/* .
RUN mv ./* /usr/share/nginx/html/
#RUN ln -s /web /usr/share/nginx/html
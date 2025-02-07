FROM node:20.10-alpine3.19 AS builder
RUN apk add git
WORKDIR /web
RUN git clone https://github.com/Pesp05/PopFilms.git .
RUN npm install -g @angular/cli
RUN npm install
RUN ng build --configuration production --aot


FROM nginx:alpine
WORKDIR /web
COPY --from=builder /web/dist/pop-films/* .
#RUN mv ./* /usr/share/nginx/html/  Este funciona
#RUN ln -s /web /usr/share/nginx/html 
RUN cd /usr/share/nginx/html/ && ln -s /web/ .
#Se queda cargando la pagina
 
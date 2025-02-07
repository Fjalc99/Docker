FROM httpd:2.4-alpine
LABEL mainteiner="alcantarilla.cafra24@triana.salesianos.edu"
LABEL version="3.0"
RUN apk add git
WORKDIR /web  
RUN git clone https://github.com/Fjalc99/lenguage-de-marcas.git .
RUN mv ./* /usr/local/apache2/htdocs/




#COPY index.html /usr/local/apache2/htdocs/
#WORKDIR es una mezcla de cd y mkdir
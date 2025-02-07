FROM httpd:2.4-alpine
LABEL maintainer="gamero.rofra24@triana.salesianos.edu"
RUN apk add git
WORKDIR /web
RUN git clone https://github.com/lmlopezmagana/git-exam-ubeda-interesa.git .
RUN mv ./* /usr/local/apache2/htdocs/
#COPY index.html /usr/local/apache2/htdocs/

## Sin WORKDIR

#FROM httpd:2.4-alpine
#LABEL maintainer="gamero.rofra24@triana.salesianos.edu"
#RUN apk add git
#RUN git clone https://github.com/lmlopezmagana/git-exam-ubeda-interesa.git ./web
#RUN mv ./web/* /usr/local/apache2/htdocs/
#COPY index.html /usr/local/apache2/htdocs/

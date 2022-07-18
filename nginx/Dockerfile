FROM nginx:mainline-alpine

COPY nginx.conf /etc/nginx/
COPY mime.types /etc/nginx/
RUN mkdir -p /etc/nginx/conf.d/directive-only/ /etc/nginx/conf.d/location/ /etc/nginx/conf.d/fastcgi/
COPY conf.d/ /etc/nginx/conf.d/
# RUN mkdir /etc/nginx/h5bp/
COPY h5bp/ /etc/nginx/h5bp/
COPY certs/ /etc/nginx/certs/
RUN mkdir /etc/nginx/sites-enabled/
COPY sites-enabled/ /etc/nginx/sites-enabled/

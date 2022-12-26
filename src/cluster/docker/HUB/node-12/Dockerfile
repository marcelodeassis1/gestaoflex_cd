FROM alpine:3.11.3

LABEL version="12" description="Gestao Flex" maintainer="Gestao Flex"

ENV NODE_VERSION 12.15.0

# Criar Grupo Gflex, Usuario app, instalar node e npm. 
# Se tiver o módulo Bcrypt, é necessário deixar a ultima linha
RUN apk upgrade --update \
    && addgroup -g 1515 app \
    && adduser -u 1515 -G app -s /bin/sh -D -S app \
    && apk add --no-cache nodejs npm git yarn ca-certificates \
    && apk add --no-cache --virtual .builds-deps build-base python \
    && apk del .builds-deps \
    && npm install -g pm2

WORKDIR /home/app

CMD ["/bin/sh"]

# docker run -it --name node gestaoflex/node:12
FROM node:carbon

ARG NODE_USER 
ARG DATA_DIR

RUN useradd -s /bin/false -m ${NODE_USER} \
  && mkdir -p /var/app \
  && chown -R ${NODE_USER}:${NODE_USER} /var/app

USER ${NODE_USER}
ENV PATH $PATH:./node_modules/.bin
WORKDIR ${DATA_DIR}
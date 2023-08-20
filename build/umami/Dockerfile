FROM node:18.17.1

ARG DATABASE_URL
ENV DATABASE_URL $DATABASE_URL

RUN git clone https://github.com/umami-software/umami.git

WORKDIR /umami

# install the dependencies
RUN yarn install

# build umami
RUN ["yarn", "build"]

# start the server
CMD ["yarn", "start"]

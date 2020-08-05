FROM ruby:2.7.1-alpine
WORKDIR /usr/src/app
RUN apk update && apk --no-cache add \
    build-base \
    npm \
    sqlite-dev \
    yarn \
    vim
RUN apk --no-cache add tzdata && \
    cp /usr/share/zoneinfo/Asia/Tokyo /etc/localtime
#    cp /usr/share/zoneinfo/Asia/Tokyo /etc/localtime && \
#    apk del tzdata
RUN gem install \
    bundler \
    sqlite3 \
    rails
RUN export LANG="ja_JP.UTF-8"
ENV HOST 0.0.0.0

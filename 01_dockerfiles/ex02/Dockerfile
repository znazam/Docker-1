FROM ruby

ENV PORT 3000

EXPOSE $PORT

WORKDIR /opt/

RUN gem install rails

RUN curl -sS https://dl.yarnpkg.com/debian/pubkey.gpg | apt-key add -

RUN echo "deb https://dl.yarnpkg.com/debian/ stable main" | tee /etc/apt/sources.list.d/yarn.list

RUN apt-get update -qq && apt-get install -yf nodejs yarn

RUN rails new app

WORKDIR /opt/app/

#docker build -t ex02 .
#run docker run -rm --name last -p 3000:3000 last

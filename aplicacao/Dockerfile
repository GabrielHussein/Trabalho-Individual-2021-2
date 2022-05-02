FROM ruby:3.0.0

WORKDIR /app

COPY Gemfile Gemfile.lock ./

RUN bundle config build.nokogiri --use-system-libraries

RUN gem install bundler && bundle install

COPY package.json yarn.lock ./

COPY . .

EXPOSE 3000

CMD ["rails", "server", "-b", "0.0.0.0"]

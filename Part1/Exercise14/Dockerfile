FROM ruby:2.6.0
COPY . .
RUN chmod 1777 /tmp
RUN curl -sL https://deb.nodesource.com/setup_10.x | bash
RUN apt-get install -y nodejs
RUN gem install bundler
RUN bundle install
EXPOSE 3000
RUN rails db:migrate
CMD ["rails", "s"]

FROM ruby:3.1.1-alpine

ENV RAILS_ENV development

RUN apk --no-cache upgrade && \
    apk --no-cache add \
      npm \
      git \
      nodejs \
      yarn \
      build-base\
      postgresql-dev\
      tzdata

COPY Gemfile* ./
RUN bundle install
COPY . ./
EXPOSE 3000

# Configure the main process to run when running the image
CMD ["bin/rails", "server", "-b", "0.0.0.0"]
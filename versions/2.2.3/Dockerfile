FROM gliderlabs/alpine:3.2
MAINTAINER Adrian B. Danieli "https://github.com/sickp"

RUN \
  apk-install ca-certificates ruby ruby-dev && \
  gem install bundler --no-document

CMD ["irb"]

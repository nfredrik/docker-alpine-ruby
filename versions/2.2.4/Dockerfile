FROM gliderlabs/alpine:3.3
MAINTAINER Adrian B. Danieli "https://github.com/sickp"

RUN \
  apk-install ca-certificates ruby ruby-dev ruby-io-console ruby-irb && \
  gem install bundler --no-document

CMD ["irb"]

### Alpine Linux Ruby

A [Ruby][ruby] [Docker image][alpine_ruby] built on top of [Glider Labs's Alpine Linux][gliderlabs_alpine] Docker image.


#### Supported tags and `Dockerfile` links

* [`2.2.2`][dockerfile_2_2_2], [`2.2`][dockerfile_2_2_2], [`2`][dockerfile_2_2_2], [`latest`][dockerfile_2_2_2] ([Dockerfile][dockerfile_2_2_2])


### About

This image installs [Bundler][bundler] and Ruby development headers.


```ash
$ docker run --rm sickp/alpine-ruby ruby -v && bundler -v

ruby 2.2.2p95 (2015-04-13 revision 50295) [x86_64-linux-musl]
Bundler version 1.10.6
```

### History

- 2015-12-11 Initial version.

[alpine_ruby]:       https://hub.docker.com/r/sickp/alpine-ruby/
[bundler]:           http://bundler.io
[dockerfile_2_2_2]:  https://github.com/sickp/docker-alpine-ruby/tree/master/versions/2.2.2/Dockerfile
[gliderlabs_alpine]: https://hub.docker.com/r/gliderlabs/alpine/
[ruby]:              https://www.ruby-lang.org/

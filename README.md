### Alpine Linux Ruby

A lightweight [Ruby][ruby] [Docker image][dockerhub_project] built atop [Alpine Linux][gliderlabs_alpine]. Available on [GitHub][github_project].

Tags ending with the suffix `-k8s` are build on [Alpine-Kubernetes][alpine_kubernetes], an image for Kubernetes and other Docker cluster environments that use DNS-based service discovery. It adds the necessary `search` domain support for DNS resolution.

#### Supported tags and Dockerfile links

* `2.2.4`, `2.2`, `2`, `latest` (Ruby 2.2.4p230, 2015-12-16, [Dockerfile][dockerfile])
* `2.2.4-k8s` ([Dockerfile][dockerfile_k8s] for Kubernetes)
* `2.2.3` (Ruby 2.2.3p173, 2015-08-18)
* `2.2.2` (Ruby 2.2.2p95, 2015-04-13)


### About

This image installs [Bundler][bundler] and Ruby development headers.

```bash
$ docker run --rm -it sickp/alpine-ruby:2.2.4 # irb
irb(main):001:0>

$ docker run --rm sickp/alpine-ruby:2.2.4 ruby -v
ruby 2.2.4p230 (2015-12-16 revision 53155) [x86_64-linux-musl]

$ docker run --rm sickp/alpine-ruby:2.2.4 bundler -v
Bundler version 1.11.2

$ docker run --rm sickp/alpine-ruby:2.2.4 openssl version
OpenSSL 1.0.2g  1 Mar 2016

$ docker run --rm sickp/alpine-ruby:2.2.4 cat /etc/alpine-release
3.3.3
```

### History

- 2016-04-06 - Update to Alpine Linux 3.3.3, OpenSSL 1.0.2g.
- 2016-02-09 - Added support for ALPINE_NO_RESOLVER in Kubernetes version.
- 2016-01-27 - Added Kubernetes versions (-k8s), until Alpine Linux/musl adds DNS search support.
- 2015-01-05 - Added `ruby-irb` and `ruby-io-console` packages, updated to Bundler 1.11.2.
- 2015-12-23 - Updated to Alpine Linux 3.3 / Ruby 2.2.4p230.
- 2015-12-11 - Initial version.

[alpine_kubernetes]: https://hub.docker.com/r/janeczku/alpine-kubernetes/
[bundler]:           http://bundler.io
[dockerhub_project]: https://hub.docker.com/r/sickp/alpine-ruby/
[dockerfile]:        https://github.com/sickp/docker-alpine-ruby/tree/master/versions/2.2.4/Dockerfile
[dockerfile_k8s]:    https://github.com/sickp/docker-alpine-ruby/tree/master/versions/2.2.4-k8s/Dockerfile
[github_project]:    https://github.com/sickp/docker-alpine-ruby/
[gliderlabs_alpine]: https://hub.docker.com/r/gliderlabs/alpine/
[ruby]:              https://www.ruby-lang.org/

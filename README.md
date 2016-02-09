### Alpine Linux Ruby

A lightweight [Ruby][ruby] [Docker image][dockerhub_project] built atop [Alpine Linux][gliderlabs_alpine]. Available on [GitHub][github_project].

Tags ending with the suffix `-k8s` are build on [Alpine-Kubernetes][alpine_kubernetes], an image for Kubernetes and other Docker cluster environments that use DNS-based service discovery. It adds the necessary `search` domain support for DNS resolution.


#### Supported tags and Dockerfile links

* [`2.2.4`][dockerfile_2_2_4], [`2.2`][dockerfile_2_2_4], [`2`][dockerfile_2_2_4], [`latest`][dockerfile_2_2_4] (Ruby 2.2.4p230, 2015-12-16)
* [`2.2.4-k8s`][dockerfile_2_2_4_k8s] (Kubernetes)
* [`2.2.3`][dockerfile_2_2_3] (Ruby 2.2.3p173, 2015-08-18)
* [`2.2.2`][dockerfile_2_2_2] (Ruby 2.2.2p95, 2015-04-13)


### About

This image installs [Bundler][bundler] and Ruby development headers.

```bash
$ docker run --rm -it sickp/alpine-ruby # irb
irb(main):001:0>

$ docker run --rm sickp/alpine-ruby ruby -v
ruby 2.2.4p230 (2015-12-16 revision 53155) [x86_64-linux-musl]

$ docker run --rm sickp/alpine-ruby bundler -v
Bundler version 1.11.2

$ docker run --rm sickp/alpine-ruby openssl version
OpenSSL 1.0.2f  28 Jan 2016 (Library: OpenSSL 1.0.2e 3 Dec 2015)

$ docker run --rm sickp/alpine-ruby cat /etc/alpine-release
3.3.1
```

### History

- 2016-02-09 - Added support for ALPINE_NO_RESOLVER in Kubernetes version.
- 2016-01-27 - Added Kubernetes versions (-k8s), until Alpine Linux/musl adds DNS search support.
- 2015-01-05 - Added `ruby-irb` and `ruby-io-console` packages, updated to Bundler 1.11.2.
- 2015-12-23 - Upgraded to Alpine Linux 3.3 / Ruby 2.2.4p230.
- 2015-12-11 - Initial version.

[alpine_kubernetes]:    https://hub.docker.com/r/janeczku/alpine-kubernetes/
[bundler]:              http://bundler.io
[dockerhub_project]:    https://hub.docker.com/r/sickp/alpine-ruby/
[dockerfile_2_2_2]:     https://github.com/sickp/docker-alpine-ruby/tree/master/versions/2.2.2/Dockerfile
[dockerfile_2_2_3]:     https://github.com/sickp/docker-alpine-ruby/tree/master/versions/2.2.3/Dockerfile
[dockerfile_2_2_4]:     https://github.com/sickp/docker-alpine-ruby/tree/master/versions/2.2.4/Dockerfile
[dockerfile_2_2_4_k8s]: https://github.com/sickp/docker-alpine-ruby/tree/master/versions/2.2.4-k8s/Dockerfile
[github_project]:       https://github.com/sickp/docker-alpine-ruby/
[gliderlabs_alpine]:    https://hub.docker.com/r/gliderlabs/alpine/
[ruby]:                 https://www.ruby-lang.org/

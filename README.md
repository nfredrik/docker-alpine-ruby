### Alpine Linux Ruby

A lightweight [Ruby][ruby] [Docker image][dockerhub_project] built atop [Alpine Linux][gliderlabs_alpine]. Available on [GitHub][github_project].

> If you're running Kubernetes 1.2.0 or later on all your cluster nodes, you should now use the non-`k8s` tags below. These tags are built on Alpine Linux 3.4, which adds the necessary DNS search support for service discovery. Kubernetes defaults to `dnsPolicy=ClusterFirst` in pod specs, and defines a single `nameserver` in `/etc/resolv.conf`. This means things should finally work correctly for Alpine Linux images without modification.

#### Ruby Tags

* `2.3.1`, `2.3`, `2`, `latest` (Ruby 2.3.1p112, 2016-04-26, [Dockerfile][dockerfile])
* `2.2.4` (Ruby 2.2.4p230, 2015-12-16)
* `2.2.3` (Ruby 2.2.3p173, 2015-08-18)
* `2.2.2` (Ruby 2.2.2p95, 2015-04-13)

#### Kubernetes <1.2.0

Tags with the `-k8s` suffix are built on [Alpine-Kubernetes 3.3][alpine_kubernetes], an image for Kubernetes and other Docker cluster environments that use DNS-based service discovery. It adds the necessary `search` domain support for DNS resolution.

* `2.2.4-k8s` (Ruby 2.2.4p230, 2015-12-16)

### Basic Usage

```bash
$ docker run --rm -it sickp/alpine-ruby:2.3.1 # irb
irb(main):001:0>
```

### About

$ docker run --rm sickp/alpine-ruby:2.3.1 ruby -v
ruby 2.3.1p112 (2016-04-26 revision 54768) [x86_64-linux]

$ docker run --rm sickp/alpine-ruby:2.3.1 bundle -v
Bundler version 1.12.5

$ docker run --rm sickp/alpine-ruby:2.3.1 cat /etc/alpine-release
3.4.0
```

### History

- 2016-06-16 - Added Ruby 2.3.1, Bundler 1.12.5, Alpine Linux 3.4.0.
- 2016-04-06 - Updated to Alpine Linux 3.3.3, OpenSSL 1.0.2g.
- 2016-02-09 - Added support for ALPINE_NO_RESOLVER in Kubernetes version.
- 2016-01-27 - Added Kubernetes versions (-k8s), until Alpine Linux/musl adds DNS search support.
- 2015-01-05 - Added `ruby-irb` and `ruby-io-console` packages, updated to Bundler 1.11.2.
- 2015-12-23 - Updated to Alpine Linux 3.3 / Ruby 2.2.4p230.
- 2015-12-11 - Initial version.

[alpine_kubernetes]: https://hub.docker.com/r/janeczku/alpine-kubernetes/
[bundler]:           http://bundler.io
[dockerhub_project]: https://hub.docker.com/r/sickp/alpine-ruby/
[dockerfile]:        https://github.com/sickp/docker-alpine-ruby/tree/master/versions/2.3.1/Dockerfile
[github_project]:    https://github.com/sickp/docker-alpine-ruby/
[gliderlabs_alpine]: https://hub.docker.com/r/gliderlabs/alpine/
[ruby]:              https://www.ruby-lang.org/

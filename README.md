### Alpine Linux Ruby

A lightweight [Ruby][ruby] [Docker image][dockerhub_project] built from source atop [Alpine Linux][alpine]. Available on [GitHub][github_project].

These images are heavily based on the [official Ruby Alpine image][official_ruby] (`2.x.x-alpine`), except for a modified tag format formed from the Ruby version `{major}.{minor}.{teeny}` plus an image revision `-r{revision}`. The image revision changes whenever the underlying [Bundler gem][bundler], [RubyGems][rubygems], or [Alpine Linux][alpine] release changes. This is the familiar scheme that Linux package managers use, and allows you to lock to an immutable Alpine + Ruby + RubyGems + Bundler combination.

    $ docker run --interactive --tty --rm sickp/alpine-ruby:2.4.2-r1  # default command is `irb`
    irb(main):001:0> Time.now.yday  # day of the year (at the Royal Observatory in Greenwich, London)

### Tags

##### `2.5.0-r1`, `2.5.0`, `2.5`, `preview`

[Dockerfile](https://github.com/sickp/docker-alpine-ruby/tree/master/versions/2.5.0-r1/Dockerfile) / 2017-10-10

    $ docker run --rm sickp/alpine-ruby:2.5.0-r1 about
    * Ruby 2.5.0preview1 (2017-10-10 trunk 60153) [x86_64-linux]
    * RubyGems 2.6.14
    * Bundler 1.15.4
    * Alpine Linux 3.6.2

##### `2.4.2-r1`, `2.4.2`, `2.4`, `2`, `latest`

[Dockerfile](https://github.com/sickp/docker-alpine-ruby/tree/master/versions/2.4.2-r1/Dockerfile) / 2017-09-14

    $ docker run --rm sickp/alpine-ruby:2.4.2-r1 about
    * Ruby 2.4.2p198 (2017-09-14 revision 59899) [x86_64-linux]
    * RubyGems 2.6.14
    * Bundler 1.15.4
    * Alpine Linux 3.6.2

##### `2.4.1-r3`, `2.4.1`

[Dockerfile](https://github.com/sickp/docker-alpine-ruby/tree/master/versions/2.4.1-r3/Dockerfile) / 2017-08-02

    $ docker run --rm sickp/alpine-ruby:2.4.1-r3 about
    * Ruby 2.4.1p111 (2017-03-22 revision 58053) [x86_64-linux]
    * RubyGems 2.6.12
    * Bundler 1.15.3
    * Alpine Linux 3.6.2

##### `2.4.1-r2`

[Dockerfile](https://github.com/sickp/docker-alpine-ruby/tree/master/versions/2.4.1-r2/Dockerfile) / 2017-06-12

    $ docker run --rm sickp/alpine-ruby:2.4.1-r2 about
    * Ruby 2.4.1p111 (2017-03-22 revision 58053) [x86_64-linux]
    * RubyGems 2.6.12
    * Bundler 1.15.1
    * Alpine Linux 3.6.0

##### `2.4.1-r1`

[Dockerfile](https://github.com/sickp/docker-alpine-ruby/tree/master/versions/2.4.1-r1/Dockerfile) / 2017-03-23

    $ docker run --rm sickp/alpine-ruby:2.4.1-r1 about
    * Ruby 2.4.1p111 (2017-03-22 revision 58053) [x86_64-linux]
    * RubyGems 2.6.11
    * Bundler 1.14.6
    * Alpine Linux 3.4.6

##### `2.4.0-r2`

[Dockerfile](https://github.com/sickp/docker-alpine-ruby/tree/master/versions/2.4.0-r2/Dockerfile) / 2017-03-16

    $ docker run --rm sickp/alpine-ruby:2.4.0-r2 about
    * Ruby 2.4.0p0 (2016-12-24 revision 57164) [x86_64-linux]
    * RubyGems 2.6.10
    * Bundler 1.14.6
    * Alpine Linux 3.4.6

##### `2.4.0-r1`

[Dockerfile](https://github.com/sickp/docker-alpine-ruby/tree/master/versions/2.4.0-r1/Dockerfile) / 2017-03-01

    $ docker run --rm sickp/alpine-ruby:2.4.0-r1 about
    * Ruby 2.4.0p0 (2016-12-24 revision 57164) [x86_64-linux]
    * RubyGems 2.6.10
    * Bundler 1.14.5
    * Alpine Linux 3.4.6

### History

    2017-10-20 Added 2.5.0-r1: Ruby 2.5.0 preview1.
    2017-10-12 Added 2.4.2-r1: Ruby 2.4.2p198, RubyGems 2.6.14, Bundler 1.15.4, Alpine Linux 3.6.2.
    2017-08-02 Added 2.4.1-r3: Ruby 2.4.1p111, RubyGems 2.6.12, Bundler 1.15.3, Alpine Linux 3.6.2.
    2017-06-12 Added 2.4.1-r2: Ruby 2.4.1p111, RubyGems 2.6.12, Bundler 1.15.1, Alpine Linux 3.6.0.
    2017-03-23 Added 2.4.1-r1. Ruby 2.4.1p111, RubyGems 2.6.11.
    2017-03-16 Added 2.4.0-r2. Bundler 1.14.6.
    2017-03-01 Introduced new tag format. Ruby 2.4.0p0, RubyGems 2.6.10, Bundler 1.14.5, Alpine Linux 3.4.6.
    2016-06-16 Added Ruby 2.3.1, Bundler 1.12.5, Alpine Linux 3.4.0.
    2016-04-06 Updated to Alpine Linux 3.3.3, OpenSSL 1.0.2g.
    2016-02-09 Added support for ALPINE_NO_RESOLVER in Kubernetes version.
    2016-01-27 Added Kubernetes versions (-k8s), until Alpine Linux/musl adds DNS search support.
    2015-01-05 Added `ruby-irb` and `ruby-io-console` packages, updated to Bundler 1.11.2.
    2015-12-23 Updated to Alpine Linux 3.3 / Ruby 2.2.4p230.
    2015-12-11 Initial version.

[alpine]:            https://alpinelinux.org
[bundler]:           https://bundler.io
[dockerhub_project]: https://hub.docker.com/r/sickp/alpine-ruby/
[github_project]:    https://github.com/sickp/docker-alpine-ruby/
[official_ruby]:     https://store.docker.com/images/0f900dcb-7e32-45e4-b095-6dfa2f5b597b
[ruby]:              https://www.ruby-lang.org/
[rubygems]:          https://rubygems.org/pages/download

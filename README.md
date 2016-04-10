[slack-irc][slack-irc], dockerised
==================================

This repository contains a Dockerfile which can be used to run a Slack-to-IRC
two-way bridge, namely [slack-irc][slack-irc], in a Docker container.

[slack-irc]: https://github.com/ekmartin/slack-irc

Usage
-----

You must provide a configuration file in JSON format, which must be bind-mounted
into the running container at `/etc/slack-irc.json`. See [slack-irc's
documentation](https://github.com/ekmartin/slack-irc#example-configuration) for
more about this file.

For example, if you have created a `config.json` file on the host in the current
working directory:

    docker run -v $PWD/config.json:/etc/slack-irc.json nickstenning/slack-irc

License
-------

As far as this project contains licensable code, it is licensed under the BSD
2-clause (AKA FreeBSD) license, a copy of which is provided in `LICENSE`.

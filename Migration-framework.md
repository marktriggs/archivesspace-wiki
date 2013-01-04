*Note:* Import is now available from the web interface as well; this is documentation for using the command line migration toolset.

Before following the [instructions in `migrations/README.md`](https://github.com/archivesspace/archivesspace/blob/master/migrations/README.md) you will need to install [RVM](https://rvm.io) and execute these commands.

```sh
rvm install jruby-1.7
rvm use jruby-1.7
export JRUBY_OPTS=--1.9
gem install nokogiri json-schema psych json
```
# Searchyou

Welcome to your new gem! In this directory, you'll find the files you need to be able to package up your Ruby library into a gem. Put your Ruby code in the file `lib/searchyou`. To experiment with that code, run `bin/console` for an interactive prompt.

TODO: Delete this and the text above, and describe your gem

## Installation

Add this line to your application's Gemfile:

```ruby
gem 'searchyou'
```

And then execute:

    $ bundle

Or install it yourself as:

    $ gem install searchyou

Alternatively, if you would like to test locally, you can clone the project and add this to your Jekyll sites' `Gemfile`:

```
gem 'searchyou', path: "/path/to/searchyll/"
```

## Usage

You'll need to add an Elasticsearch section to your Jekll site's `_config.yml` like so:

```
elasticsearch:
  url: "http://localhost:9200/" # Required. Supports auth and SSL: https://user:pass@someurl.com
  number_of_shards: 1           # Optional. Default is 1 primary shard.
  number_of_replicas: 1         # Optional. Default is 0 replicas.
  index_name: "jekyll"          # Optional. Default is "jekyll"
```

You'll also need to add it to the `gems` section in that same `_config.yml` file. This will tell Jekyll to run the searchyou plugin when the site is being generated:

```
gems: [<list of other gems>, 'searchyou']
```

## Development

After checking out the repo, run `bin/setup` to install dependencies. Then, run `rake spec` to run the tests. You can also run `bin/console` for an interactive prompt that will allow you to experiment.

To install this gem onto your local machine, run `bundle exec rake install`. To release a new version, update the version number in `version.rb`, and then run `bundle exec rake release`, which will create a git tag for the version, push git commits and tags, and push the `.gem` file to [rubygems.org](https://rubygems.org).

## Contributing

Bug reports and pull requests are welcome on GitHub at https://github.com/[USERNAME]/searchyou.

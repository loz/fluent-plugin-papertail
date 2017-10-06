# Fluent::Plugin::Papertrail

Welcome to your new gem! In this directory, you'll find the files you need to be able to package up your Ruby library into a gem. Put your Ruby code in the file `lib/fluent/plugin/papertrail`. To experiment with that code, run `bin/console` for an interactive prompt.

TODO: Delete this and the text above, and describe your gem

## Installation

Add this line to your application's Gemfile:

```ruby
gem 'fluent-plugin-papertrail'
```

And then execute:

    $ bundle

Or install it yourself as:

    $ gem install fluent-plugin-papertrail

## Usage

To configure this in fluentd

<match whatever.*>
  type papertrail
  papertrail_host <your papertrail hostname>
  papertrail_port <your papertrail port>
</match>

Use a record transform plugin to populate within the record the following fields:

    message   The log
    program   The program/tag
    severity  A valid syslog severity label
    facility  A valid syslog facility label
    hostname  The source hostname for papertrail logging


## Development

After checking out the repo, run `bin/setup` to install dependencies. Then, run `rake test` to run the tests. You can also run `bin/console` for an interactive prompt that will allow you to experiment.

To install this gem onto your local machine, run `bundle exec rake install`. To release a new version, update the version number in `version.rb`, and then run `bundle exec rake release`, which will create a git tag for the version, push git commits and tags, and push the `.gem` file to [rubygems.org](https://rubygems.org).

## Contributing

Bug reports and pull requests are welcome on GitHub at https://github.com/[USERNAME]/fluent-plugin-papertrail.


## License

The gem is available as open source under the terms of the [MIT License](http://opensource.org/licenses/MIT).

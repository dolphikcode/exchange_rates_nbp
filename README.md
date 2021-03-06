# ExchangeRatesNBP

[![Build Status](https://travis-ci.org/maciejmajewski/exchange_rates_nbp.svg?branch=master)](https://travis-ci.org/maciejmajewski/exchange_rates_nbp)
[![Gem Version](https://badge.fury.io/rb/exchange_rates_nbp.svg)](https://badge.fury.io/rb/exchange_rates_nbp)

Library for accessing exchange rates from nbp.pl.

It can be used via API or via command line utility.

## Installation

Add this line to your application's Gemfile:

```ruby
gem 'exchange_rates_nbp'
```

And then execute:

    $ bundle

Or install it yourself as:

    $ gem install exchange_rates_nbp

## Usage

```ruby
ExchangeRatesNBP.exchange_rate(Date.new(2016, 1, 1), 'EUR')
# => 4.2615
```

### Via command line

```sh
exchange_rates_nbp --date DATE --currency_code CURRENCY_CODE --table a
# => 4.2615
```

#### Getting latest exchange rate

```sh
exchange_rates_nbp --latest --currency-code=EUR
# => 4.312
```
#### Verbose mode

```sh
exchange_rates_nbp --latest --currency-code=EUR --verbose
# => Publish date: 2016-09-30
# => Conversion factor: 1
# => Exchange rate: 4.312
```

## Development

After checking out the repo, run `bin/setup` to install dependencies. Then, run `rake spec` to run the tests. You can also run `bin/console` for an interactive prompt that will allow you to experiment. Run `bundle exec exchange_rates_nbp` to use the gem in this directory, ignoring other installed copies of this gem.

To install this gem onto your local machine, run `bundle exec rake install`. To release a new version, update the version number in `version.rb`, and then run `bundle exec rake release`, which will create a git tag for the version, push git commits and tags, and push the `.gem` file to [rubygems.org](https://rubygems.org).

## Contributing

Bug reports and pull requests are welcome on GitHub at https://github.com/maciejmajewski/exchange_rates_nbp.

## License

The gem is available as open source under the terms of the [MIT License](http://opensource.org/licenses/MIT).

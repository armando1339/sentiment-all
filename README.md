# sentiment-all

sentiment-all is Sentiment Analysis Service that allow the analysis of text throught [SENTIM-API](https://sentim-api.herokuapp.com/).

[![Build Status](https://travis-ci.com/armando1339/sentiment-al.svg?branch=master)](https://travis-ci.com/armando1339/sentiment-al) [![Coverage Status](https://coveralls.io/repos/github/armando1339/sentiment-al/badge.svg?branch=master)](https://coveralls.io/github/armando1339/sentiment-al?branch=master)

## Usage

Just call the service passing through a text to be processed.

```ruby

# => Execute the service
sentiment_al.call text: "Candy"

# => Verify the SENTIM-API responce
sentiment_al.successfully?

# => Verify the response
sentiment_al.response

# => Response to hash
sentiment_al.response_to_hash

```

Verify the status of HTTP Request

```ruby
sentiment_al.response
sentiment_al.response.code
sentiment_al.response.message
sentiment_al.response.body
```

It's also available the constant SentimentAl::Service.

```ruby

# => Execute the service
SentimentAl::Service.call text: "Candy"

# => Verify the SENTIM-API responce
SentimentAl::Service.successfully?

# => Verify the response
SentimentAl::Service.response

# => Response to hash
SentimentAl::Service.response_to_hash

```

Verify the status of HTTP Request

```ruby
SentimentAl::Service.response
SentimentAl::Service.response.code
SentimentAl::Service.response.message
SentimentAl::Service.response.body
```

## Installation

Add this line to your application's Gemfile:

```ruby
gem 'sentiment-all', '~> 1.2.1beta'
```

And then execute:

```bash
$ bundle install
```

Or install it yourself as:

```bash
$ gem install sentiment-all
```

## Development

After checking out the repo, run `bin/setup` to install dependencies. Then, run `rake spec` to run the tests. You can also run `bin/console` for an interactive prompt that will allow you to experiment.

To install this gem onto your local machine, run `bundle exec rake install`. To release a new version, update the version number in `version.rb`, and then run `bundle exec rake release`, which will create a git tag for the version, push git commits and tags, and push the `.gem` file to [rubygems.org](https://rubygems.org).


## License

The gem is available as open source under the terms of the [MIT License](https://opensource.org/licenses/MIT).

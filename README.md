ruby-transmitsms
================

Ruby gem to easily access TransmitSMS RESTful APIs

[![Gem Version](https://badge.fury.io/rb/ruby-transmitsms.svg)](http://badge.fury.io/rb/ruby-transmitsms)
[![Build Status](https://drone.io/github.com/transmitsms/ruby-transmitsms/status.png)](https://drone.io/github.com/transmitsms/ruby-transmitsms/latest)

### Sample Usage
```ruby
require 'ruby-transmitsms'

# Create new Sms instance
sms = Sms.new("15eg266c832fb23c4d90f01055aef355", "bluebird")

# Send a message
response = sms.send("Hello, world", "61455123456")

# Show the result
puts response.code
puts response.body
```

### Installation
```sh
gem install ruby-transmitsms
```

### Installation with `bundler`'s Gemfile
gem "ruby-transmitsms"

## Development

### To install the required gems:
```sh
$ ./setup.sh
```

### To run  the tests:
```sh
$ ./runtest.sh
```
## API

### Sms

**initialize**(api_key, api_secret) - Sms object constructor.

params:
* `api_key`
* `api_secret`

**send**(message, to, from, send_at, list_id, dlr_callback, reply_callback, validity, replies_to_email, from_shared) - Send sms to the given `to` param or `list_id` param.

params:
* `message`
* `to`
* `from`
* `send_at`
* `list_id`
* `dlr_callback`
* `reply_callback`
* `validity`
* `replies_to_email`
* `from_shared`

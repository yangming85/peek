# Glimpse

[![Build Status](https://travis-ci.org/dewski/glimpse.png?branch=master)](https://travis-ci.org/dewski/glimpse)

Provide a glimpse into your Rails applications.

## Installation

Add this line to your application's Gemfile:

    gem 'glimpse'

And then execute:

    $ bundle

Or install it yourself as:

    $ gem install glimpse

## Usage

Run the Rails generator to get Glimpse up and included into your project:

```
rails generate glimpse:install
```

This will create a file at `config/initializers/glimpse.rb` which will give you
example views to include into your Glimpse bar.

Feel free to pick and choose from the list or create your own. The order they
are added to Glimpse, the order they will appear in your bar.

```ruby
Glimpse.into Glimpse::Views::Git, :nwo => 'github/hire', :default_branch => 'other_branch'
Glimpse.into Glimpse::Views::NavigationTime
Glimpse.into Glimpse::Views::Unicorn
Glimpse.into Glimpse::Views::ActiveRecord
Glimpse.into Glimpse::Views::Redis
```

Once your views are added to Glimpse, just render your bar by adding the following
after the opening `<body>` tag in your application layout.

```ruby
<%= render 'glimpse/bar' %>
```

## Available Glimpse views

- [glimpse-git](https://github.com/dewski/glimpse-git)
- [glimpse-redis](https://github.com/dewski/glimpse-redis)
- [glimpse-mysql2](https://github.com/dewski/glimpse-mysql2)
- [glimpse-mongo](https://github.com/dewski/glimpse-mongo)
- Navigation Time
- Unicorn

## Contributing

1. Fork it
2. Create your feature branch (`git checkout -b my-new-feature`)
3. Commit your changes (`git commit -am 'Add some feature'`)
4. Push to the branch (`git push origin my-new-feature`)
5. Create new Pull Request

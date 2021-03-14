# Turbo Basics Tutorial

## Install Turbo

Use the turbo-rails gem:

 1. Add the turbo-rails gem to your Gemfile: `gem 'turbo-rails'`
 1. Run `./bin/bundle install`
 1. Run `./bin/rails turbo:install`

See [the gem README](https://github.com/hotwired/turbo-rails#installation) for more installation details.

## Generate models

 - `rails g scaffold room name:string`
 - `rails g model message room:references content:text`

## Add nested routes for messages

```ruby
# config/routes.rb

resources :rooms do
  resources :messages
end
```

## Add associations

```ruby
# app/models/room.rb

class Room < ApplicationRecord
  has_many :messages
end
```

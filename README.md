Grape Example App
================

[![Deploy to Heroku](https://www.herokucdn.com/deploy/button.png)](https://heroku.com/deploy)

This application was generated with the [rails_apps_composer](https://github.com/RailsApps/rails_apps_composer) gem
provided by the [RailsApps Project](http://railsapps.github.io/).

Rails Composer is open source and supported by subscribers. Please join RailsApps to support development of Rails Composer.

Ruby on Rails
-------------

This application requires:

- Ruby 2.2.2
- Rails 4.2.4

Learn more about [Installing Rails](http://railsapps.github.io/installing-rails.html).

About
-----

This is an example of an Rails API made with Grape. Was created with **Rails Composer** from the RailsApps project.

Original author
---------------

Iván González, *a.k.a* [dreamingechoes](https://github.com/dreamingechoes)

Getting Started
---------------

To start using this API, you only have to do the typical ***Rails*** things:

* Install ***Ruby*** version 2.2.2 (using [RVM](https://github.com/rvm/rvm) or [RBenv](https://github.com/sstephenson/rbenv) or whatever).

* Clone the repo and do the ***bundle install*** thing:

```sh
user@computer:~$ git clone git@github.com:dreamingechoes/grape_example_app.git
user@computer:~$ cd grape_example_app
user@computer:/grape_example_app$ bundle install
user@computer:/grape_example_app$ rake db:setup
```

* When all this finish, you're ready to launch the app!

```sh
user@computer:/grape_example_app$ rails s
```

* Open your web browser and go to [http://localhost:3000](http://localhost:3000) like in all the regular ***Rails*** apps.

**NOTE:** the seed.rb file has an ApiKey example token for testing the API, which is **18dfef7acf97765b54abecdf86a25bba**, but on ApiKey.create() method it assigns other random **access_token**. If you want to use the example token for testing purpose, update via console the attribute **access_token** of the ApiKey to **18dfef7acf97765b54abecdf86a25bba**, like this:

```ruby
user@computer:/grape_example_app$ rails console
Loading development environment (Rails 4.2.4)
>> a = ApiKey.first
  ApiKey Load (0.3ms)  SELECT  `api_keys`.* FROM `api_keys`  ORDER BY `api_keys`.`id` ASC LIMIT 1
=> #<ApiKey id: 2, access_token: "k93eeqa34f9774rko4abecdf86a2nckm", expires_at: "2043-03-12 21:03:46", user_id: 3, active: nil, created_at: "2015-10-26 21:03:46", updated_at: "2015-10-26 21:05:03">
>> a.update_attribute(:access_token, "18dfef7acf97765b54abecdf86a25bba")
   (1.8ms)  BEGIN
   (0.1ms)  COMMIT
=> true
```

Contributing
------------

1. Fork it
2. Create your feature branch (`git checkout -b my-new-feature`)
3. Commit your changes (`git commit -am 'Added some feature'`)
4. Push to the branch (`git push origin my-new-feature`)
5. Create new Pull Request

License
-------

**Grape Example App** is released under the [MIT License](http://www.opensource.org/licenses/MIT).

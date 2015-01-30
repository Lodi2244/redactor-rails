# Rails ~> 4.0.0 Integration for Redactor (Devise and Paperclip Edition )

The redactor-rails gem integrates the [Redactor](http://redactorjs.com/) editor with the Rails 4 asset pipeline.

This gem bundles Redactor version 9.0.2 which is the most recent version as of June 25, 2013. Check [Redactor's changelog](http://imperavi.com/redactor/log/) for further updates.

## Installation

Add this line to your application's Gemfile:


    gem 'redactor-rails', github: 'xana68/redactor-rails'

And then execute:

    $ bundle install


Add to application.rb:

    require 'redactor-rails'


### Now generate models for store uploading files

#### ActiveRecord + paperclip

    gem "paperclip"

    $ rails generate redactor:install --devise --backend=paperclip

    $ rake db:migrate


### Include the Redactor assets

Add to your `application.js`:

      //= require redactor-rails

Add to your `application.css`:

      *= require redactor-rails

### Initialize Redactor

For each textarea that you want to use with Redactor, add the "redactor" class and ensure it has a unique ID:

    <%= text_area_tag :editor, "", class: "redactor", rows: 40, cols: 120 %>

## Contributing

1. Fork it
2. Create your feature branch (`git checkout -b my-new-feature`)
3. Commit your changes (`git commit -am 'Added some feature'`)
4. Push to the branch (`git push origin my-new-feature`)
5. Create new Pull Request

## Special Thanks

[wildjcrt (Jerry Lee)](https://github.com/wildjcrt/)
## Statement

`redactor-rails` part of reference [galetahub/ckeditor](https://github.com/galetahub/ckeditor) project.

`redactor-rails` uses MIT-LICENSE. Rock!!!!!

## License

the `redactor-rails` project is MIT-LICENSE.

You may use `Redactor` for non-commercial websites for free, however, we do not guarantee any technical support.

Redactor has [3 different licenses](http://redactorjs.com/download/) for commercial use.
For details please see [License Agreement](http://redactorjs.com/download/).

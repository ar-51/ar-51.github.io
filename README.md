# AR51 Documentation
AR51 uses "Just the docs" Jekyll theme.
## Installation

### via GitHub Pages remote theme

The quickiest way to use Just The Docs is to use GitHub pages [remote theme](https://blog.github.com/2017-11-29-use-any-theme-with-github-pages/) feature in your `_config.yml` file:

```yaml
remote_theme: just-the-docs/just-the-docs
```
### via RubyGems:

Alternatively you can install it as a Ruby Gem.

Add this line to your Jekyll site's Gemfile:

```ruby
gem "just-the-docs"
```

And add this line to your Jekyll site's `_config.yml`:

```yaml
theme: just-the-docs
```

And then execute:

    $ bundle

Or install it yourself as:

    $ gem install just-the-docs

[View the documentation](https://just-the-docs.github.io/just-the-docs/) for usage information.

To run the server on your machine

    $ bundle exec jekyll serve
And navigate to the site:  http://127.0.0.1:4000/ (the site might be on a different port)
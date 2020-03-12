source "https://rubygems.org"

gemspec

if ENV["edge"]
  gem "activerecord", :github => "rails/rails"
end

group :development, :test do
  gem 'minitest', '5.10.1'
  gem 'mocha'
  gem "rake"
  gem "yard"

  platforms :ruby_21 do
    gem "activerecord", "< 5.0"
    gem "activesupport", "< 5.0"
  end

  platforms :ruby do
    gem "sqlite3", "~> 1.3.6"
    gem "redcarpet"

    if RUBY_VERSION > "2.1.0"
      gem "test-unit" # not bundled in CRuby since 2.2.0
    end
  end

  platforms :jruby do
    gem "activerecord-jdbcsqlite3-adapter"
    gem "jruby-openssl", :require => false # Silence openssl warnings.
  end
end

source 'https://rubygems.org'

gemspec

platforms :jruby do
  gem 'activerecord-jdbcsqlite3-adapter'
end

version = ENV['RAILS_VERSION'] || 'default'

case version
when 'master'
  gem 'railties', { git: 'https://github.com/rails/rails.git' }
  gem 'arel', { git: 'https://github.com/rails/arel.git' }
when 'default'
  gem 'railties', '>= 6.0'
when '6.0.0'
  platforms :ruby do
    gem 'sqlite3', '~> 1.4'
  end

  gem 'railties', "~> #{version}"
else
  platforms :ruby do
    gem 'sqlite3', '1.3.13'
  end

  gem 'railties', "~> #{version}"
end

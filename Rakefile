require 'rubygems'
require 'bundler'
begin
  Bundler.setup(:default, :development)
rescue Bundler::BundlerError => e
  $stderr.puts e.message
  $stderr.puts "Run `bundle install` to install missing gems"
  exit e.status_code
end
require 'rake'

require 'jeweler'
Jeweler::Tasks.new do |gem|
  # gem is a Gem::Specification... see http://docs.rubygems.org/read/chapter/20 for more options
  gem.name = "bookscan"
  gem.homepage = "http://github.com/tumf/bookscan"
  gem.license = "MIT"
  gem.summary = %Q{BookScan Scraper}
  gem.description = %Q{This is a scraper of Bookscan (http://www.bookscan.co.jp) Service.This is *NOT* a official software of Bookscan.}
  gem.email = "y.takahara@gmail.com"
  gem.authors = ["Yoshihiro TAKAHARA"]
  # Include your dependencies below. Runtime dependencies are required when using your gem,
  # and development dependencies are only needed for development (ie running rake tasks, tests, etc)
  #  gem.add_development_dependency 'rspec', '> 1.2.3'
end
Jeweler::RubygemsDotOrgTasks.new

require 'rake/testtask'
Rake::TestTask.new(:test) do |test|
  test.libs << 'lib' << 'test'
  test.pattern = 'test/**/test_*.rb'
  test.verbose = true
end

task :default => :test


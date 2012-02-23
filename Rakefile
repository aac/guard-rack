require 'rubygems'
require 'bundler'

require File.expand_path('../lib/guard/rack/version', __FILE__)

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
  gem.name = "guard-rack"
  gem.homepage = "http://github.com/dblock/guard-rack"
  gem.license = "MIT"
  gem.summary = "Restart Rack when files change."
  gem.email = "dblock@dblock.org"
  gem.version = Guard::RackVersion::VERSION
  gem.authors = [ "Daniel Doubrovkine" ]
  gem.files = Dir.glob('lib/**/*')
end

Jeweler::RubygemsDotOrgTasks.new

require 'rspec/core'
require 'rspec/core/rake_task'

RSpec::Core::RakeTask.new(:spec) do |spec|
  spec.pattern = FileList['spec/**/*_spec.rb']
end

task :default => :spec


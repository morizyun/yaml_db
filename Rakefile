# encoding: utf-8
require 'rubygems'
require 'bundler'
require 'rake'
require 'rspec/core/rake_task'

begin
  Bundler.setup(:default, :development)
rescue Bundler::BundlerError => e
  $stderr.puts e.message
  $stderr.puts "Run `bundle install` to install missing gems"
  exit e.status_code
end


require 'jeweler'
Jeweler::Tasks.new do |gem|
  gem.name = "fm_yaml_db"
  gem.homepage = "http://github.com/kalabiyau/yaml_db"
  gem.license = "MIT"
  gem.summary = %Q{fork of a great yaml_db gem}
  gem.description = %Q{Forked gem from yaml_db - the great DB independent dumper for rails devs}
  gem.email = "skullzeek@gmail.com"
  gem.authors = ["Adam Wiggins","Orion Henry"]
end
Jeweler::RubygemsDotOrgTasks.new

task :default => :spec

require 'rdoc/task'
Rake::RDocTask.new do |rdoc|
  version = File.exist?('VERSION') ? File.read('VERSION') : ""

  rdoc.rdoc_dir = 'rdoc'
  rdoc.title = "fm-yamldb #{version}"
  rdoc.rdoc_files.include('README*')
  rdoc.rdoc_files.include('lib/**/*.rb')
end


RSpec::Core::RakeTask.new(:spec) do |spec|
  spec.pattern = 'spec/*_spec.rb'
  spec.rspec_opts = ['--backtrace']
end

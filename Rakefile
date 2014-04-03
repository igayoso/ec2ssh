# encoding: utf-8

require 'rubygems'

require 'rake'

require 'jeweler'
Jeweler::Tasks.new do |gem|
  # gem is a Gem::Specification... see http://docs.rubygems.org/read/chapter/20 for more options
  gem.name = "EC2ssh"
  gem.homepage = "http://github.com/rsalvado/ec2ssh"
  gem.license = "MIT"
  gem.summary = %Q{A script to make it easier to ssh into running amazon EC2 instances.}
  gem.description = %Q{Since ec2 instance public hostnames are dynamic, and not easy to remember or type, this script provides a list all your running instances so you can select the one you want to ssh into easily (without having to pass the aws console ritual each time you need the hostname).}
  gem.email = "rsalvado@gnuine.com"
  gem.authors = ["Ramon Salvadó"]
  gem.executables = ["ec2ssh"]
  gem.add_dependency(%q<highline>, '>= 1.5.2')
  gem.add_dependency(%q<aws>, '>= 2.5.6')
  gem.add_dependency(%q<activesupport>, '>= 2.3.14')
end
Jeweler::RubygemsDotOrgTasks.new

require 'rake/testtask'
Rake::TestTask.new(:test) do |test|
  test.libs << 'lib' << 'test'
  test.pattern = 'test/**/test_*.rb'
  test.verbose = true
end

task :default => :test

require 'rdoc/task'
Rake::RDocTask.new do |rdoc|
  version = File.exist?('VERSION') ? File.read('VERSION') : ""

  rdoc.rdoc_dir = 'rdoc'
  rdoc.title = "ec2ssh #{version}"
  rdoc.rdoc_files.include('README*')
  rdoc.rdoc_files.include('lib/**/*.rb')
end

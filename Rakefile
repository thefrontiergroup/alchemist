require 'rubygems'
require 'rake'

begin
  require 'jeweler'
  Jeweler::Tasks.new do |gem|
    gem.name = 'alchemist'
    gem.version = '0.1.3'
    gem.summary = 'Conversions... like you\'ve never seen them before!'
    gem.description = 'Conversions... like you\'ve never seen them before!!'
    gem.email = 'matt@toastyapps.com'
    gem.homepage = 'http://github.com/toastyapps/alchemist'
    gem.authors = ["Matthew Mongeau", "Dirk Kelly of http://www.thefrontiergroup.com.au"]
  end
  Jeweler::RubyforgeTasks.new
rescue LoadError
  puts "Jeweler (or a dependency) not available. Install it with: sudo gem install jeweler"
end

require 'rake/testtask'
Rake::TestTask.new(:test) do |test|
  test.libs << 'test'
  test.pattern = 'test/**/*_test.rb'
  test.verbose = true
end

begin
  require 'rcov/rcovtask'
  Rcov::RcovTask.new do |test|
    test.libs << 'test'
    test.pattern = 'test/**/*_test.rb'
    test.verbose = true
  end
rescue LoadError
  task :rcov do
    abort "RCov is not available. In order to run rcov, you must: sudo gem install spicycode-rcov"
  end
end

task :test => :check_dependencies

task :default => :test
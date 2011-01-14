require 'rubygems'  
require 'rake'  
  
begin  
  require 'jeweler'  
  Jeweler::Tasks.new do |gemspec|  
    gemspec.name = "preview"  
    gemspec.version = "0.0.1"
    gemspec.summary = "Add preview functionality to rails resources"  
    gemspec.description = "Make an ActiveRecord object previewable, and display the preview using existing/custom templates"  
    gemspec.email = "bigbeliever@gmail.com"  
    gemspec.homepage = "http://github.com/zerothabhishek/preview"  
    gemspec.authors = ["sifar"]  
  end
  Jeweler::RubygemsDotOrgTasks.new   
rescue LoadError  
  puts "Jeweler not available. Install it with: sudo gem install technicalpickles-jeweler -s http://gems.github.com"  
end  
  
Dir["#{File.dirname(__FILE__)}/tasks/*.rake"].sort.each { |ext| load ext }
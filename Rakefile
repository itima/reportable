require 'rubygems'
require 'bundler'

Bundler.setup
Bundler.require

require 'spec/rake/spectask'
require 'simplabs/excellent/rake'

desc 'Default: run specs.'
task :default => :spec

desc 'Run the specs'
Spec::Rake::SpecTask.new(:spec) do |t|
  t.spec_files = FileList['spec/**/*_spec.rb']
end

YARD::Rake::YardocTask.new(:doc) do |t|
  t.files   = ['lib/**/*.rb', '-', 'HISTORY.md']
  t.options = ['--no-private', '--title', 'Reportable Documentation']
end

Simplabs::Excellent::Rake::ExcellentTask.new(:excellent) do |t|
  t.paths = %w(lib)
end

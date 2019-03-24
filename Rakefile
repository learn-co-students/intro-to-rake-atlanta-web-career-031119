
namespace :greeting do
desc 'outputs hello to the terminal'
task :hello do
  puts "hello from Rake!"
end

desc 'outputs HOLA to the terminal'
task :hola do
 puts "hola de Rake!"
end
end

desc 'drop in to pry'
task :console => :environment  do

 Pry.start
end

 namespace :db do

desc "environment task"
task :environment do
require_relative './config/environment'
end

desc "migrate changes to  db "
task :migrate =>:environment do
Student.create_table
end

desc "seeds the database from a seed file"
task :seed do
   require_relative './db/seeds.rb'

end

end

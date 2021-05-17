namespace :greeting do
  desc 'outputs hello to the terminal'
  task :hello do
    puts "hello from Rake!"
  end

  desc 'outputs hola to the terminal'
  task :hola do
    puts "hola de Rake!"
  end
end

#gives this file access to the environment
task :environment do
  require_relative './config/environment'
end

#boots up pry 
desc 'drop into the Pry console'
task :console => :environment do
  Pry.start
end

#convention to say we are migrating when you alter a SQL database
namespace :db do
  desc 'migrate changes to your database'
  task :migrate => :environment do
    Student.create_table
  end

  desc 'seed the database with some dummy data'
  task :seed do
    require_relative './db/seeds.rb'
  end

end

#seed means to fill it with dummy info
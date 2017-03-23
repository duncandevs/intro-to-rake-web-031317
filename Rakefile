# namespace :greeting
#   greeting:hello
#     should print out 'hello from Rake!'
#   greeting:hola
#     should print out 'hola de Rake!'
# namespace :db
#   db:migrate
#     invokes the :environment task as a dependency
#     create the students table in the database
#   db:seed
#     seeds the database with dummy data from a seed file

namespace :greeting do
  desc 'outputs hello to the terminal'
  task :hello do
    puts "hello from Rake!"
  end

  desc 'outputs hola de Rake!'
  task :hola do
    puts "hola de Rake!"
  end
end

namespace :db do
  desc 'migrate to db add new tables'
  task :migrate => :environment do
    Student.create_table
  end

  task :environment do
    require_relative './config/environment'
  end
  
  task :seed do
    require_relative './db/seeds.rb'
  end
end

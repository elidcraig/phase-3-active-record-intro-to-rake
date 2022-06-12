namespace :greeting do
  desc 'says hello'
  task :hello do
    puts "hello from Rake!"
  end

  desc 'outputs hola to the terminal'
  task :hola do
    puts "hola de Rake!"
  end
end

namespace :db do
  desc 'migration time'
  task migrate: :environment do
    Student.create_table
  end

  desc 'seed the database with some dummy data'
  task seed: :environment do
    require_relative './db/seeds'
  end
end

task :environment do
  require_relative './config/environment'
end

desc 'console time'
task console: :environment do
  Pry.start
end

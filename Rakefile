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

desc 'invokes the :environment task as a dependency'
namespace :db do
  task :migrate => :environment do
    Student.create_table
  end
  task :environment do
    require_relative './config/environment'
  end
  desc 'gets fake seed data'
  task :seed do
    require_relative "./db/seeds.rb"
  end
end

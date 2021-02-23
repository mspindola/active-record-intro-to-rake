namespace :greeting do
desc 'outputs hello to the terminal'
  task :hello do
    puts "hello from Rake!"
  end

desc "outputs hello for a second time in the terminal"
  task :hello2 do
    puts "Hello again from Rake!"
  end

desc "outputs hola to the terminal"
  task :hola do
    puts "hola de Rake!"
  end
end

namespace :db do
  desc "migrate changes to your database"
  task :migrate => :environment do
    Student.create_table
  end

  desc "seed the database with some dummy data"
  task :seed do 
    require_relative './db/seeds.rb'
  end

end

desc "requires environment dile"
task :environment do
  require_relative './config/environment'
end

desc 'drop into the Pry console'
task :console => :environment do
    Pry.start
end


#in terminal rake hello would puts "hello from Rake!" and 
#if we use the command rake -T shows a list of tasks with their descriptions

#namespace will group them, to call the tasks in the terminal now, we need to type
#rake greeting:hello 
#=> hello from Rake!


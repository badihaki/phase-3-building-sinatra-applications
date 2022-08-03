require_relative './config/environment'
require 'sinatra/activerecord/rake'

desc "Runs a Pry console"
task :console do
  # This line turns on logging of the SQL generated by Active Record
  ActiveRecord::Base.logger = Logger.new(STDOUT)
  
  # Open a Pry session
  Pry.start
end

desc "Start the server"
task :server do
  # This starts the server using rerun, so we can edit code and reload
  # the browser to see changes, instead of disconnecting and then re-
  # connecting the server.
  exec "rerun -b 'rackup config.ru'"
end
require './app/secure_key'
desc 'rotate all'
task :rotate do
  User.rotatable.each do |u|
    begin
      puts "rotating #{u.id}: #{u.heroku_id}"
      u.rotate_keys!
      puts "success!"
    rescue => e
      puts "failed #{e.inspect}"
      next
    end
  end
end



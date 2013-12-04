task :default => [:compile]
task :compile do
  `mkdir -p ebin`
  `erlc -o ebin src/*/*.erl src/*.erl`
  `cp src/*/*.app ebin/.`
  `cp src/*.app.src ebin/.`
end

task :run do
  exec "erl -pa ebin -s hello_world_app"
end

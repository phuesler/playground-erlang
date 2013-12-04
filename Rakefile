task :default => [:compile]
task :compile do
  `mkdir -p ebin`
  `mkdir -p priv`
  `erlc -o ebin src/*/*.erl src/*.erl`
  `cd src/jiffy && make`
  `cp src/jiffy/ebin/*.beam ebin/.`
  `cp src/jiffy/priv/* priv/.`
  `cp src/*/*.app ebin/.`
  `cp src/*.app.src ebin/.`
end

task :run do
  exec "erl -pa ebin -s hello_world_app"
end

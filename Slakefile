{run, read, stylus, jade, autoprefixer, beautify, write} = require \lgen

task \build ->
  jade(\index)({}) |> beautify.html! |> write \index.html
  read \style.styl |> stylus |> autoprefixer! |> write \.css
  run "cp photo.jpg build/photo.jpg"

task \publish ->
  invoke \build
  commit = run "git log --pretty=oneline | head -n 1" .trim!substring(41).replace(/'/g, \")
  run "git co master"
  run "cp build/* ."
  run "git ci -am '#commit'"
  run "git push origin master"
  run "git co source"

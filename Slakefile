{read, stylus, jade, autoprefixer, beautify, write, copy} = require \lgen
<-! task \build
jade(\index)({}) |> beautify.html! |> write \index.html
read \style.styl |> stylus |> autoprefixer! |> write \.css
copy {file: \photo.jpg}

{read, stylus, jade, cssmin, autoprefixer, beautify, write, copy} = require \lgen
<-! task \build
jade(\index)({}) |> beautify.html! |> write \index.html
read \style.styl |> stylus |> autoprefixer! |> cssmin |> write \.css
copy {file: \photo.jpg}

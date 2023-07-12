# remixicon-autocomplete by [etoundi.com](https://www.etoundi.com/)

[Remixicon](https://github.com/Remix-Design/RemixIcon) `v.3.4.0` autocomplete for Sublime Text.

![screenshot](screenshot.png)

### Installation
```bash
# add the repository to the Sublime packages directory
cd ~/Library/Application\ Support/Sublime\ Text/Packages/
git clone git@github.com/etoundi2nd/remixicon-autocomplete.git
```

### Contribution
```bash
# if you want to contribute to the project,
# creating a symlink to a directory of your choice might be helpful
ln -s ~/Library/Application\ Support/Sublime\ Text/Packages/remixicon-autocomplete ~/Documents/my-projects/remixicon-autocomplete
```

Note: you can get the Sublime packages path in the Sublime menu:
`Sublime Text > Preferences > Browse Packages…`

Note: getting a list of remixicon using ruby
```ruby
# install gem
gem install css_parser

# then in irb
require 'css_parser'
include CssParser

url = 'https://cdn.jsdelivr.net/npm/remixicon@3.4.0/fonts/remixicon.css' # change version to the latest
parser = CssParser::Parser.new
parser.load_uri!(url)

classes_list = parser.to_h['all'].keys.filter_map { |key| key.split(':').first[1...] if key.starts_with?('.') }
puts classes_list
```

### Credits
Created based on [Tailwind CSS Autocomplete for Sublime Text 3/4](https://github.com/danklammer/tailwind-sublime-autocomplete) by [@danklammer](https://github.com/danklammer)

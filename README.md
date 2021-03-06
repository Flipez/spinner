# Spinner

Terminal Spinner for Crystal Programming Language

![All](/images/all.gif)

## Installation

Add this to your application's `shard.yml`:

```yaml
dependencies:
  spinner:
    github: flipez/spinner
```

## Usage


```crystal
require "spinner"

sp = Spin.new
sp.start
sleep 3
sp.stop
```

## Options

`delay`: `default = 0.1`

`chars`: you can choose charset from [CHARSET](src/spinner/charset.cr) `default = Spinner::Charset[:pipe]`

`text`: Define text which appends to your spinner `default = ""`

## Examples

```crystal
require "spinner"
require "colorize"

chars = Spinner::Charset[:arrow].map do |c|
  c.colorize(:light_green)
end

spin = Spin.new(0.2, chars)
spin.start
sleep 3
spin.stop
```

![Color](/images/color.gif)

## Contributing

1. Fork it ( https://github.com/flipez/spinner/fork )
2. Create your feature branch (git checkout -b my-new-feature)
3. Commit your changes (git commit -am 'Add some feature')
4. Push to the branch (git push origin my-new-feature)
5. Create a new Pull Request

## Contributors

- [askn](https://github.com/askn) Aşkın Gedik - creator
- [Flipez](https://github.com/Flipez) - maintainer

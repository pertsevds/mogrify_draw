# MogrifyDraw

A wrapper of the imagemagick draw functionality on top of mogrify

## Installation

```elixir
def deps do
  [
    {:mogrify_draw, git: "git@github.com:pertsevds/mogrify_draw.git"}
  ]
end
```

mix deps.get

## Examples

```elixir
import Mogrify

%Mogrify.Image{path: "test.png", ext: "png"}
|> custom("size", "280x280")
|> canvas("white")
|> custom("fill", "blue")
|> MogrifyDraw.circle(140,140,100,100)
|> custom("fill", "yellow")
|> MogrifyDraw.circle(140,140,140,100)
|> create(path: ".")
```

Documentation can be generated with [ExDoc](https://github.com/elixir-lang/ex_doc)
and published on [HexDocs](https://hexdocs.pm). Once published, the docs can
be found at <https://hexdocs.pm/mogrify_draw>.

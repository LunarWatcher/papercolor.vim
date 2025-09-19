# Papercolor

This is a fork of [NLKNguyen/papercolor-theme](https://github.com/NLKNguyen/papercolor-theme). The theme itself is mostly considered feature-complete, and I lack the design skills to do any meaningful theming-related developments. This fork exists because the upstream repo has bugs I need fixed, and lacks support for (among other plugins), [yegappan/lsp](https://github.com/yegappan/lsp).

> [!warning]
>
> In the future, the theme might be migrated to vim9script. This will break neovim support, so neovim users are encouraged to not use this fork, or switch to the superior version of Vim that doesn't break the fucking clipboard every other version.

---

Light & Dark color schemes for terminal and GUI **Vim** awesome editor

Inspired by Google's Material Design. Improve code readability! Great for presentation!

It is optimized to load fast and support 4-bit, 8-bit and 24-bit color terminals or GUIs. For full color spectrum, any 8-bit (256-color) capable display is sufficient.

**Plus:** PaperColor is also a syntax highlighting framework for creating color themes, in which the PaperColor theme you see here is the default. If you want to create your own theme, consider creating on top of PaperColor to leverage 100% its functionality and still have your own specialization.

## ✨ Inclusive support

### 🎨 Colors

Support True / GUI color (24-bit) and identical **256 color** (8-bit) that the default theme is based on.

Also gracefully support down to **16 color** (4-bit) terminal, which will use terminal native colors. You need to change the terminal colors to PaperColor palette.

In **8 color** and **4 color** terminals, they might lack the necessary variation of colors to express PaperColor look, but seriously let me know if you still use these kinds of terminals.

**Default Theme Palette**

|    | Light Theme                                                  |  8-bit | 24-bit  | Dark Theme                                                   |  8-bit | 24-bit  |
|--- | -----                                                        | -------|---------| -----                                                        | -------|---------|
| 0  |![#eeeeee](https://place-hold.it/100x40/eeeeee/000000?text=+) |  255   | #eeeeee |![#1c1c1c](https://place-hold.it/100x40/1c1c1c/000000?text=+) |  234   | #1c1c1c |
| 1  |![#af0000](https://place-hold.it/100x40/af0000/000000?text=+) |  124   | #af0000 |![#af005f](https://place-hold.it/100x40/af005f/000000?text=+) |  125   | #af005f |
| 2  |![#008700](https://place-hold.it/100x40/008700/000000?text=+) |  28    | #008700 |![#5faf00](https://place-hold.it/100x40/5faf00/000000?text=+) |  70    | #5faf00 |
| 3  |![#5f8700](https://place-hold.it/100x40/5f8700/000000?text=+) |  64    | #5f8700 |![#d7af5f](https://place-hold.it/100x40/d7af5f/000000?text=+) |  179   | #d7af5f |
| 4  |![#0087af](https://place-hold.it/100x40/0087af/000000?text=+) |  31    | #0087af |![#5fafd7](https://place-hold.it/100x40/5fafd7/000000?text=+) |  74    | #5fafd7 |
| 5  |![#878787](https://place-hold.it/100x40/878787/000000?text=+) |  102   | #878787 |![#808080](https://place-hold.it/100x40/808080/000000?text=+) |  244   | #808080 |
| 6  |![#005f87](https://place-hold.it/100x40/005f87/000000?text=+) |  24    | #005f87 |![#d7875f](https://place-hold.it/100x40/d7875f/000000?text=+) |  173   | #d7875f |
| 7  |![#444444](https://place-hold.it/100x40/444444/000000?text=+) |  238   | #444444 |![#d0d0d0](https://place-hold.it/100x40/d0d0d0/000000?text=+) |  252   | #d0d0d0 |
| 8  |![#bcbcbc](https://place-hold.it/100x40/bcbcbc/000000?text=+) |  250   | #bcbcbc |![#585858](https://place-hold.it/100x40/585858/000000?text=+) |  240   | #585858 |
| 9  |![#d70000](https://place-hold.it/100x40/d70000/000000?text=+) |  160   | #d70000 |![#5faf5f](https://place-hold.it/100x40/5faf5f/000000?text=+) |  71    | #5faf5f |
| 10 |![#d70087](https://place-hold.it/100x40/d70087/000000?text=+) |  162   | #d70087 |![#afd700](https://place-hold.it/100x40/afd700/000000?text=+) |  148   | #afd700 |
| 11 |![#8700af](https://place-hold.it/100x40/8700af/000000?text=+) |  91    | #8700af |![#af87d7](https://place-hold.it/100x40/af87d7/000000?text=+) |  140   | #af87d7 |
| 12 |![#d75f00](https://place-hold.it/100x40/d75f00/000000?text=+) |  166   | #d75f00 |![#ffaf00](https://place-hold.it/100x40/ffaf00/000000?text=+) |  214   | #ffaf00 |
| 13 |![#d75f00](https://place-hold.it/100x40/d75f00/000000?text=+) |  166   | #d75f00 |![#ff5faf](https://place-hold.it/100x40/ff5faf/000000?text=+) |  205   | #ff5faf |
| 14 |![#005faf](https://place-hold.it/100x40/005faf/000000?text=+) |  25    | #005faf |![#00afaf](https://place-hold.it/100x40/00afaf/000000?text=+) |  37    | #00afaf |
| 15 |![#005f87](https://place-hold.it/100x40/005f87/000000?text=+) |  24    | #005f87 |![#5f8787](https://place-hold.it/100x40/5f8787/000000?text=+) |  66    | #5f8787 |


There are many more colors for many additional syntax groups, but they are designed to fall back to these base 16 colors strategically so that it can utilize the terminal native color palette (if configured like above), and also theme designers only need to provide 16 colors for a functional theme.

### 🚀 Languages

Currently designed for these languages:
  - Haskell, Erlang, Elixir, Clojure, Elm, Purescript, F#
  - C, C++, Golang, Rust, Java, JavaScript, Python, Ruby, Pascal, PHP, Perl, LUA
  - DTrace, SystemTap, SQL/MySQL, Octave/MATLAB, R, Lex/Flex & Yacc/Bison, ASN.1, Assembly (MIPS, GAS, NASM), Bash/Shell script, Sed, Awk, Vim script, Powershell script
  - Dockerfile, Makefile, CMake, NGINX, Cucumber, YAML, JSON, HTML, XML, Markdown, reStructuredText, PlantUML, Dosini, Mail, Git commit message
  - Ada, COBOL, Fortran, ALGOL, *(what's your other favorite dinosaur?)*

Other file types can still display well as long as your Vim is set up to recognize the language syntax even though that may not be the optimal experience. So, if the language you are working on isn't listed here, feel free to make a design request.
### 📚 Targeted plugins for additional syntax highlighting

vimdiff, netrw, [NERDTree](https://github.com/scrooloose/nerdtree), [tagbar](https://github.com/majutsushi/tagbar), [tabline](https://github.com/mkitt/tabline.vim), [vim-airline](https://github.com/bling/vim-airline), [vim-indent-guides](https://github.com/nathanaelkane/vim-indent-guides), [vim-startify](https://github.com/mhinz/vim-startify), [Agit](https://github.com/cohama/agit.vim), [vim-signify](https://github.com/mhinz/vim-signify), [nvim-dap-ui](https://github.com/rcarriga/nvim-dap-ui) ([PR](https://github.com/NLKNguyen/papercolor-theme/pull/181)), [nvim-cmp](https://github.com/hrsh7th/nvim-cmp) ([PR](https://github.com/NLKNguyen/papercolor-theme/pull/182)), [vim-gitgutter](https://github.com/airblade/vim-gitgutter)

The below are programming language syntax highlighting plugins that enhances upon Vim built-in syntax highlighting.

* C: [c-syntax.vim](https://github.com/NLKNguyen/c-syntax.vim)
* JavaScript: [vim-javascript](https://github.com/pangloss/vim-javascript)
* Jsx: [vim-jsx-pretty](https://github.com/MaxMEllon/vim-jsx-pretty)
* JSON: [vim-json](https://github.com/elzr/vim-json)
* Go: [vim-go](https://github.com/fatih/vim-go)
* DTrace: [dtrace-syntax-file](https://github.com/vim-scripts/dtrace-syntax-file)
* SystemTap: [vim-systemtap](https://github.com/nickhutchinson/vim-systemtap)
* Haskell: [haskell-vim](https://github.com/raichoo/haskell-vim)
* PlantUML: [plantuml-syntax](https://github.com/aklt/plantuml-syntax)
* Markdown: [vim-markdown](https://github.com/plasticboy/vim-markdown)
* Assembly MIPS: [mips](https://github.com/vim-scripts/mips.vim)
* Assembly GAS: [vim-gas](https://github.com/Shirk/vim-gas)
* Octave/MATLAB: [vim-octave](https://github.com/jvirtanen/vim-octave)
* Python: [python-syntax](https://github.com/vim-python/python-syntax/)
* Dockerfile: [dockerfile.vim](https://github.com/docker/docker/tree/master/contrib/syntax/vim)
* NGINX: [nginx-vim-syntax](https://github.com/evanmiller/nginx-vim-syntax)
* Elixir: [vim-elixir](https://github.com/elixir-lang/vim-elixir)
* Elm: [elm-vim](https://github.com/ElmCast/elm-vim)
* Purescript: [purescript-vim](https://github.com/purescript-contrib/purescript-vim)
* F#: [vim-fsharp](https://github.com/fsharp/vim-fsharp)
* PowerShell: [vim-ps1](https://github.com/PProvost/vim-ps1)
* CMake: [vim-cmake-syntax](https://github.com/pboettch/vim-cmake-syntax)
* ALGOL: [vim-algol68](https://github.com/sterpe/vim-algol68)

## 🔌 Installation

It's easy to use a plugin manager like [vim-plug](https://github.com/junegunn/vim-plug) (recommended for convenient `:PlugUpdate`). Add this to your .vimrc where Plug is configured, and run `:PlugInstall`

    Plug 'LunarWatcher/papercolor-theme'

Instructions for other plugin managers has been omitted, as it's usually just oneliners in all the plugin managers worth caring about.

### ⭐ Configure  `.vimrc`

Put this in your `~/.vimrc`

```vim
set t_Co=256   " This is may or may not needed.

set background=light
colorscheme PaperColor
```

Or using the dark version:

```vim
set background=dark
colorscheme PaperColor
```

To switch to dark or light variant during session: `:set background=dark` or `:set background=light`

To quickly toggle between them, use [vim-unimpaired](https://github.com/tpope/vim-unimpaired)'s keymap `cob`

*Optional*: turn on line numbers and status bar

```VimL
set number
set laststatus=2
```
## 🛠️ User Customization


This theme currently provides theme options and language-specific options. All config options can be stored in global variable `g:PaperColor_Theme_Options` which can be set in your `.vimrc`


**Note**:
+ This `g:PaperColor_Theme_Options` variable must be placed anywhere **before** `color PaperColor` command.
+ if the same option is provided in both a theme and a theme's variant, the value in the theme's variant options will take precedence.

#### Theme Options

Within section `theme`, options for each theme can be specified under the theme name. The original PaperColor theme is `default`. For example:

```vim
let g:PaperColor_Theme_Options = {
  \   'theme': {
  \     'default': {
  \       'transparent_background': 1
  \     }
  \   }
  \ }
```

Or if you want to specify options only for a variant (dark or light) of a theme, you can specify using this pattern `[theme name].light` or `[theme name].dark`. For example:

```vim
let g:PaperColor_Theme_Options = {
  \   'theme': {
  \     'default.dark': {
  \       'transparent_background': 1
  \     }
  \   }
  \ }
```

**Color overriding**


You can override any color of the theme of interest. This example is for `default` theme (original PaperColor Theme), but you can specify any other theme that is registered.

The overriding setting is placed in `override` key of `g:PaperColor_Theme_Options` variable that you set in `.vimrc` like this.

```vim
let g:PaperColor_Theme_Options = {
  \   'theme': {
  \     'default.dark': {
  \       'override' : {
  \         'color00' : ['#080808', '232'],
  \         'linenumber_bg' : ['#080808', '232']
  \       }
  \     }
  \   }
  \ }

```

See [DESIGN.md](https://github.com/LunarWatcher/papercolor-theme/blob/master/DESIGN.md) for more details and full list of color names.


##### Currently available theme options

option                   | value                                          | default
------                   | ------                                         | -------
`transparent_background` | 1: use terminal background                     | 0: use theme background
`allow_bold`             | 1: use bold for certain text, 0: not at all    | decided by the theme
`allow_italic`           | 1: use italics for certain text, 0: not at all | decided by the theme
`override`               | dictionary of color key-value                  |


#### Language-specific options

In general, for each language, built-in functions and constants are not highlighted.
This is intentional; the vim syntax file often lags behind actual language development.
To override the default behavior, optionally place a language section in `g:PaperColor_Theme_Options`.
An example configuration is available below


```vim
let g:PaperColor_Theme_Options = {
  \   'language': {
  \     'haskell': {
  \       'no_bold_types' : 1
  \     },
  \     'python': {
  \       'highlight_builtins' : 1
  \     },
  \     'cpp': {
  \       'highlight_standard_library': 1
  \     },
  \     'c': {
  \       'highlight_builtins' : 1
  \     }
  \   }
  \ }
```

##### Currently available language options

language  | option                       | value     | default
------    | ------                       | ------    | ------
`c`       | `highlight_builtins`         | 1: enable | 0: disable
`cpp`     | `highlight_standard_library` | 1: enable | 0: disable
`python`  | `highlight_builtins`         | 1: enable | 0: disable
`haskell` | `no_bold_types`              | 1: enable | 0: disable

## 📺 Screenshots

Coming eventually. The upstream repo hosted the screenshots on a wordpress site rather than uploading them to the Git repo. The screenshots there work at the time of writing.

## License

MIT. See [LICENSE](https://github.com/NLKNguyen/papercolor-theme/blob/master/LICENSE)

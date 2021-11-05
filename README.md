## vim-indent-object

### Intro

Vim text objects provide a convenient way to select and operate on various
types of objects. These objects include regions surrounded by various types of
brackets and various parts of language (ie sentences, paragraphs, etc).

This plugin defines a new text object, based on indentation levels. This is
very useful in languages such as Python, in which the syntax defines scope in
terms of indentation. Using the objects defined in this plugin, an entire if
structure can be quickly selected, for example.

### Install

- vim-plug

```vim
Plug 'baysmith/vim-indent-object'
```

- Packer
```vim
use 'baysmith/vim-indent-object'
```

### Usage

This plugin defines two new text objects. These are very similar - they differ
only in whether they include the line below the block or not.

| Key bindings | Description                                                 |
| ------------ | ----------------------------------------------------------- |
| `<count>ai`  | **A**n **I**ndentation level and line above.                |
| `<count>ii`  | **I**nner **I**ndentation level (**no line above**).        |
| `<count>aI`  | **A**n **I**ndentation level and lines above/below.         |
| `<count>iI`  | **I**nner **I**ndentation level (**no lines above/below**). |

**Note:** the `iI` mapping is mostly included simply for completeness, it is
effectively a synonym for `ii`.

Just like regular text objects, these mappings can be used either with
operators expecting a motion, such as `d` or `c`, as well as in visual mode.

In visual mode the mapping can be repeated, which has the effect of
iteratively increasing the scope of indentation block selected. Specifying a
count can be used to achieve the same effect.

### Acknowledgements

vim-indent-object was originally written by Michael Smith <msmith@msmith.id.au>,
http://github.com/michaeljsmith/vim-indent-object


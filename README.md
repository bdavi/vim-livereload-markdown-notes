# LiveReload Markdown Notes

## Summary
I've struggled to find a notetaking app I like. Most have poor keyboard support, use a propietary format to store data and force a context switch away from my normal vim/tmux workflow.

Using Guard and vim's autocmds this lets me tuck my notes into a tmux window next to my code, dispays live HTML previews, uses familiar keybindings for editing, is searchable with fzf and is stored in vanilla markdown files.

## Dependencies
- [Ruby](https://github.com/ruby/ruby)
- [Pandoc](https://github.com/jgm/pandoc)
- [LiveReload Browser Plugin](https://github.com/mockko/livereload/blob/master/README-old.md)

## Setup

### Install Ruby dependencies:

```bash
$ bundle install
```

### Add the following to your `.vimrc`:

```
function! PreviewMarkdown()
  if filereadable('preview.html')
    !pandoc %:p -f markdown_github -t html -s -o preview.html
  endif
endfunction

autocmd BufWritePost *.md silent call PreviewMarkdown()
```

## Usage
1. Start watching for file changes by running:
```
$ bundle exec guard
```

2. Open the `preview.html` in the browser.

3. Activate the livereload plugin.

4. Use vim to add, edit and navigate the markdown files in this project.

Each time a markdown file is saved it is rendered as HTML and replaces the contents of `preveiw.html` which causes livereload to refresh the page.

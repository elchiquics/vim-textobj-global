# vim-textobj-global - Text object for entire buffers

vim-textobj-entire is a Vim plugin to provide text objects (`ae` and `ie` by
default) to select the entire content of a buffer.  Though these are trivial
operations (e.g. `ggVG`), text object versions are more handy, because you do
not have to be conscious of the cursor position (e.g. `vae`).

vim-textobj-entire provides two text objects:

* `ag` targets the entire content of the current buffer.
* `ig` is similar to `ae`, but `ie` does not include leading and trailing empty
  lines.  `ie` is handy for some situations.  For example,
    1. Paste some text into a new buffer (`<C-w>n"*P`)
       -- note that the initial empty line is left as the last line.
    2. Edit the text (`:%s/foo/bar/g` etc)
    3. Then copy the resulting text to another application (`"*yie`)

<!-- vim: set expandtab shiftwidth=4 softtabstop=4 textwidth=78 : -->

# proced-narrow

This package provdes live filtering of processes in proced buffers.  In general, after calling
proced-narrow you type a filter string into the minibuffer to filter the list of processes.  After
each change proced-narrow automatically reflects the change in the buffer.  Typing C-g will
cancel the narrowing and restore the origininal view, typing RET will exit the live filtering and
leave the proced buffer in the narrowed state.  To bring it back to the original view, you can call
`revert buffer' (usually bound to g).

## Install

```
(use-package proced-narrow
    :ensure t
    :bind (:map proced-mode-map
        ("/" . proced-narrow)))
```

## Usage

1. Open up proced (`M-x proced`)
2. Press `/` (given you've followed the installation instructions
above)
3. Type the name of the process you want to filter for e.g. `emacs`
4. Press RET to keep the narrowed buffer or C-g to cancel the narrowing and restore the original
   view.

## License

GNU General Public License, Version 3.0

---

- [travisjeffery.com](http://travisjeffery.com)
- GitHub [@travisjeffery](https://github.com/travisjeffery)
- Twitter [@travisjeffery](https://twitter.com/travisjeffery)
- Medium [@travisjeffery](https://medium.com/@travisjeffery)

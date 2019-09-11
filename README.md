# proced-narrow

This package provides live filtering of processes in proced buffers.  Open proced, call
proced-narrow, and type the query to filter the processes with.  If you type "emacs" then
proced-narrow will filter the processes listed to only the Emacs processes.  While in the
minibuffer, typing RET will exit the minibuffer and leave the proced buffer in the narrowed state,
and typing C-g will exit the minibuffer and restore the list of processes.  While in the proced
buffer, to bring back all processes, call revert-buffer (default bind is g).

## Install

```
(use-package proced-narrow
  :ensure t
  :after proced
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

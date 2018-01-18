# job.vim

An job api for vim and neovim

## usage

```vim
func! s:on_stdout(id, data, event) abort

endf

func! s:on_stderr(id, data, event) abort

endf

func! s:on_exit(id, data, event) abort

endf

call job#start(argv,
 \ 'on_stdout' : function('s:on_stdout'),
 \ 'on_stderr' : function('s:on_stderr'),
 \ 'on_exit' : function('s:on_exit'),
 \ )
```

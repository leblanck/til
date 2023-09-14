# Setting Go Install Dir

I recently installed [shfmt](https://github.com/mvdan/sh) but had some issues getting it found in my PATH. Turns out that after running `go env` my `GOBIN` was not set. Setting this accordingly and then re-installing shfmt allowed all to work as intended.

```
$ go env -w GOBIN=/usr/local/bin
$ go instal .......
```

[Source](https://go.dev/doc/tutorial/compile-install)

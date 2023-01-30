# Viewing PATH Variable in a More Readable Way

I had been doing some troubleshooting with items in my `$PATH` variable and was going cross-eyed tryting to parse it over and over again. This made things much easier.

You can pipe the output of `echo $PATH` to translate (tr) to change all colons into newline characters:
```
echo $PATH | tr ":" "\n"
```

Before:
```
╰─ echo $PATH
/opt/homebrew/bin:/Users/n1517117/.gem/ruby/3.0.0/bin:/usr/local/opt/ruby/bin:/Users/n1517117/.local/bin:/Users/n1517117/.pyenv/shims:/opt/homebrew/bin:/opt/homebrew/sbin:/usr/local/bin:/System/Cryptexes/App/usr/bin:/usr/bin:/bin:/usr/sbin:/sbin:/Applications/Privileges.app/Contents/Resources:/Users/n1517117/.fig/bin:/Users/n1517117/.local/bin
```

After:
```
╰─ echo $PATH | tr ":" "\n"
/opt/homebrew/bin
/Users/n1517117/.gem/ruby/3.0.0/bin
/usr/local/opt/ruby/bin
/Users/n1517117/.local/bin
/Users/n1517117/.pyenv/shims
/opt/homebrew/bin
/opt/homebrew/sbin
/usr/local/bin
/System/Cryptexes/App/usr/bin
/usr/bin
/bin
/usr/sbin
/sbin
/Applications/Privileges.app/Contents/Resources
/Users/n1517117/.fig/bin
/Users/n1517117/.local/bin
```

*source:* [twitter](https://twitter.com/linuxopsys/status/1619773625392824320?s=20&t=Owng6Xy5SvMhJEMUeADfJg)
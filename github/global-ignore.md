# Setting Local Repo Ignores Using Global Ignore

I like to set my ignores globally as I work on similar project types so instead of creating a new .gitignore each time, I created one global version and have it saved in my [dotfiles](https://github.com/leblanck/dotfiles).

However, I always seem to forget how to add it to each individual repo, hopefully writing this out will help it stick.

```bash
git config --global core.excludesfile ~/.gitignore
```

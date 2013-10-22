# Puree

A fast zsh prompt based on [Sindresorhus's pure prompt](https://github.com/sindresorhus/pure).

Features:

* Offline-friendly Git integration (doesn't try to access remote)
* Current RVM and/or virtualenv display
* Non-zero status code of last executed command
* Last execution time notification above threshold
* Username/host for ssh connections

## How to use

### Brute-force

Either source the `prompt_puree_setup` file and then run `prompt puree` or symlink it to your zprezto/yadr/other
configuration framework's prompt directory.

### (Almost) non-intrusive
If you're using zprezto/yadr or other configuration framework and you don't want to fork/change/merge, you can do the
following:

* Create a ~/.zsh.prompts directory.
* Edit .zshrc and add at the beginning (_before_ sourcing the configuration framework's code):

```
# Add custom prompts to fpath before loading zprezto:
if [[ -s "$HOME/.zsh.prompts" ]] fpath=($HOME/.zsh.prompts $fpath)
```

* Symlink the `prompt_puree_setup` to the .zsh.prompts directory.
* Have a beer.
# Template repository for Dev 2.0 ✨ dotfiles

Use this template to start developing your dotfiles. 💪

Create the new repo in your GitHub user account as `your-username/dotfiles`.

## Using your dotfiles (VS Code)

If using VS Code, update your `settings.json` with:

```
"remote.containers.dotfiles.repository": "git@github.com:your-username/dotfiles"
```

After making changes to VS Code settings, open the command palette using `[CMD] + [Shift] + [P]`, then run *Remote-Containers: Rebuild Container*.

## Using your dotfiles (everything else)

If using [`wfx`](https://docs.wayflyer.io/wf-cli-plugin-x/latest/) or [prod access environment](https://github.com/wayflyer/wayflyer/blob/master/prodaccessenv/README.md), set the following in your `~/.zprofile`:

``` bash
export WF_DOTFILES_REPOSITORY=your-username/dotfiles
```

After making changes to `~/.zprofile`, it's worth restarting your computer to ensure all programs have picked up the configuration.

## Customizing your devcontainer

Once configured, on any future launch of a devcontainer your repo will be cloned into the container and the contents of `dotfiles` will be symlinked into the `$HOME` directory.

Customize your container easily by:

- Adding new scripts to `dotfiles/.local/bin`.
- Adding other dotfiles and dotdirs (e.g. `.zshrc`) to `dotfiles/`.

More advanced customizations are possible by editing the `install` script to change or extend the installation behavior.

# obsidian-git-for-ios-setup

## Usage on macOS

- Clone to your preferred location
- Copy the example settings `.obsidian.mac.example` to `.obsidian.mac`
- Create new obsidian vault in the repository's directory
- Go to settings of obsidian
- In the section `About`, change `Override config folder` to `.obsidian.mac`
- Change the setting the way you like it.

## Usage on iOS Device
>Always use `lg2` instead of `git` when working in a-Shell*

- Download a-Shell
- Open a-Shell
- Generate your ssh keys by following [GitHub's guide](https://docs.github.com/en/authentication/connecting-to-github-with-ssh/generating-a-new-ssh-key-and-adding-it-to-the-ssh-agent)
- Follow [GitHub's guide for adding the public key to your GitHub profile](https://docs.github.com/en/authentication/connecting-to-github-with-ssh/adding-a-new-ssh-key-to-your-github-account)
-  Use `pickFolder` to choose the obsidian directory. (It may not be visible, before you ever created a local vault in your obsidian app)
- Clone your repository by using `lg2 clone <your-repo-link> <folder-name>`
- Go into your cloned repo with `cd <folder-name>`
- Set your user settings (unfortunately I haven't figured out yet how to do this globally...)

```sh
lg2 config user.identityFile ~/Documents/.ssh/id_ed25519
lg2 config user.password ""
lg2 config user.name "Your Name"
lg2 config user.email "your.sigature.email@for.github"
```

*Find out what your signature email is in the settings of your GitHub-Account. It's usually `<id>+<username>@users.noreply.github.com`. Setting another email adress can produce errors while trying to push. If you set a passphrase when you generated your keys, type it into the empty string.*

Now you should be able to use most of the common git commands by using `lg2 <git-command>`. It is also possible to run a-Shell with shortcuts. For examples, take a look at [this tutorial, which I also followed](https://cwoodall.com/posts/2022-01-02-obsidian-ios-sync/)

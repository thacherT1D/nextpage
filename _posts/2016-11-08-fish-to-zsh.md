Steps for transitioning your terminal to zsh - fish is great, but some people like other options.

Install [iTerm2](https://www.iterm2.com/) -- accept and install any available updates

***FROM THIS POINT ONWARDS ANY REFENCE TO TERMINAL SHOULD BE DONE IN iTERM***

Make the switch from fish to zsh:
`chsh -s $(which zsh)`

Install Oh-My-ZSH by running this command and then restart the terminal:
`curl -L https://raw.github.com/robbyrussell/oh-my-zsh/master/tools/install.sh | sh`

note: restarting iTerm means quitting the application, not just closing the current window.

**Here you're going to add the cobalt2 theme**
* Download the cobalt theme file from [here](https://github.com/wesbos/Cobalt2-iterm)
* In terminal go to `~/.oh-my-zsh/themes/` and `open .` to open the directory in finder
* Open the zip file in finder and then from the "Cobalt2-iterm-master" directory drag/add the "cobalt2.zsh-theme" file into the themes directory

* Go to your home directory `ls -a` to see all files including hidden files, you will see the .zshrc file that we want to modify
`open ~/.zshrc` to open it in atom/your text editor

In your .zshrc file set the theme ex.
`ZSH_THEME=cobalt2`
You can find more themes on the [wiki](https://github.com/robbyrussell/oh-my-zsh/wiki/Themes).

**Getting the most out of ZSH is all about the packages:**
* Still in your `./zshrc` file, scroll down to find the plugins section
* To add useful plugins to your ZSH, edit the plugin text to match the line below:
`plugins=(git node npm bower brew osx z)`
Many more plugins are available, you can find the full list on the [wiki](https://github.com/robbyrussell/oh-my-zsh/wiki/Plugins).

**Fonts and Colors:**
cobalt2 and other themes require Powerline fonts
* Download the fonts as a zip file from github [here](https://github.com/powerline/fonts)
* Unzip the file
* cd into where the unzipped file is, then run `./install.sh` to install the powerline fonts
* go into your iTerm preferences > profiles tab > text tab, check the the under **Font** and **Non-ASCII Font** choose Roboto Mono for Powerline for both
* still in iTerm prefences > profiles tab > colors tab, on the bottom right of the window, click on the "Color Presets" drop down and select "Import..." navigate to the "Cobalt2-iterm-master" folder you downloaded and select the "cobalt2.itermcolors" file
* restart iTerm
* to check that powerline fonts have been installed correctly copy the following command to your terminal: echo "\ue0b0 \u00b1 \ue0a0 \u27a6 \u2718 \u26a1 \u2699". The result should look like this:

![Character Example](https://gist.githubusercontent.com/agnoster/3712874/raw/characters.png)

**More about Z**
Z is one of the more useful plugins. Z builds a list of your most frequent and recent — “Frecent” — folders and allows you to jump to them quickly in one command.
For example, typing `z pro` into your command line and hitting enter might take you to `~/Projects`
For more details check out the [Z docs](https://github.com/rupa/z)

**Was this a huge mistake?**
Do you hate this? Missing fish already? Easy enough...
`chsh -s /usr/local/bin/fish`
will set fish as your default shell again.

If you decide you want to go back to zsh again the change can be just as easy (now that you've set it up)
`chsh -s $(which zsh)`

**References for this document**

A great article explaining Oh-My-ZSH and Z:
[Become A Command-Line Power User With Oh-My-ZSH And Z](https://www.smashingmagazine.com/2015/07/become-command-line-power-user-oh-my-zsh-z/)

[Cobalt2-iterm gitHub page](https://github.com/wesbos/Cobalt2-iterm)

[agnoster.zsh-theme / help to confirm powerline fonts installation ](https://gist.github.com/agnoster/3712874)

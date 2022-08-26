TAO (The Art) of Unix Programming (and related systemic epiphanies)
===================================================================

This is a ruby-powered, ANSI colored, `fortune`-like program to espouse wisdom at
opportune moments, such as when you log in.

*__In every culture, I come across a chapter headed Wisdom. And then 
I know exactly what is going to follow: Vanity of vanities, all is 
vanity.__ - Wittgenstein*

It's mostly a personal collection, but contributions are welcome.

Installation
------------

 * [Arch Linux](https://aur.archlinux.org/packages/taoup-git/): `yay -S taoup-git` (replace `yay` with your favorite AUR helper)
 * [Nix](https://nixos.org/): `nix-env -iA nixos.taoup` (or `nix-env -iA nixpkgs.taoup` with nixpkgs on a non-Nix OS)
 * Other unix-like: Make sure you have `ruby` and `gem` installed, run `gem install ansi` then `./taoup`.

Screenshots
-----------

### Regular terminal (iTerm2).

![screenshot](https://raw.githubusercontent.com/globalcitizen/taoup/master/screenshot.png "Behold, wisdom!")

### Oldschool terminal

![screenshot](https://raw.githubusercontent.com/globalcitizen/taoup/master/screenshot2.jpg "brew cask install cool-retro-term")

([cool-retro-term](https://github.com/Swordfish90/cool-retro-term), or via [homebrew](https://brew.sh/): *brew cask install cool-retro-term*)


Getting wisdom at login
-----------------------

To display `taoup` output at login, use the `taoup-fortune` example script or try adding something similar in your `.profile`.

By default `taoup` assumes good taste and a black/dark terminal, for edge cases and lost causes use `--whitetrash`.

Special modes
-------------

There are four modes other than standard invocation:
 * `--help` or `--h` shows brief command line help on invocation syntax
 * `--whitetrash` converts the otherwise attractive color scheme to be legible on light or white terminals
 * `--machine` drops any ANSI colors from the output (also respects `NO_COLOR` environment variable, see [no-color.org](http://no-color.org))
 * `--fortune` converts the wisdom to an assumed imitation of the fortune format. To make the resulting fortune format file available to the classic `fortune` program (loses ANSI colors in output) you can run `strfile` as follows: 
 ```
taoup --fortune >taoup-fortunes
strfile taoup-fortunes taoup-fortunes.dat
fortune taoup-fortunes
```

Praise for taoup
----------------

* "I'm honored. :)" [@jacquesm](https://news.ycombinator.com/user?id=jacquesm), HN user with ~200K karma, after being quoted in taoup
* "Taoup is in my zshrc startup, it's consistently fun/intelligent/thoughtful. Thanks for the continued maintenance 👍, cheers." [@ronjouch](https://github.com/ronjouch)
* We are now the [top ranked fortune implementation](https://github.com/topics/fortune) on Github. Spread the word!

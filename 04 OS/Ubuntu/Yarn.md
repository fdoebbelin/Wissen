Before you start using Yarn, you'll first need to install it on your system. There are a growing number of different ways to install Yarn:

### Debian / Ubuntu

On Debian or Ubuntu Linux, you can install Yarn via our Debian package repository. You will first need to configure the repository:

```
curl -sS https://dl.yarnpkg.com/debian/pubkey.gpg | sudo apt-key add -
echo "deb https://dl.yarnpkg.com/debian/ stable main" | sudo tee /etc/apt/sources.list.d/yarn.list

```

```
curl -sS https://dl.yarnpkg.com/debian/pubkey.gpg | sudo apt-key add -
echo "deb https://dl.yarnpkg.com/debian/ rc main" | sudo tee /etc/apt/sources.list.d/yarn.list

```

```
curl -sS https://dl.yarnpkg.com/debian/pubkey.gpg | sudo apt-key add -
echo "deb https://nightly.yarnpkg.com/debian/ nightly main" | sudo tee /etc/apt/sources.list.d/yarn.list

```

On Ubuntu 16.04 or below and Debian Stable, you will also need to configure [the NodeSource repository](https://nodejs.org/en/download/package-manager/#debian-and-ubuntu-based-linux-distributions) to get a new enough version of Node.js.

Then you can simply:

```
sudo apt update && sudo apt install yarn

```

**Note**: Ubuntu 17.04 comes with `cmdtest` installed by default. If you’re getting errors from installing `yarn`, you may want to run `sudo apt remove cmdtest` first. Refer to [this](https://github.com/yarnpkg/yarn/issues/2821) for more information.

If using `nvm` you can avoid the `node` installation by doing:

```
sudo apt update && sudo apt install --no-install-recommends yarn

```

**Note**: Due to the use of `nodejs` instead of `node` name in some distros, `yarn` might complain about `node` not being installed. A workaround for this is to add an alias in your `.bashrc` file, like so: `alias node=nodejs`. This will point `yarn` to whatever version of `node` you decide to use.

### Path Setup

If Yarn is not found in your PATH, follow these steps to add it and allow it to be run from anywhere.

Note: your profile may be in your `.profile`, `.bash_profile`, `.bashrc`, `.zshrc`, etc.

1.  Add this to your profile: `export PATH="$PATH:/opt/yarn-[version]/bin"` (the path may vary depending on where you extracted Yarn to)
2.  In the terminal, log in and log out for the changes to take effect

To have access to Yarn’s executables globally, you will need to set up the `PATH` environment variable in your terminal. To do this, add ``export PATH="$PATH:`yarn global bin`"`` to your profile, or if you use Fish shell, simply run the command `set -U fish_user_paths (yarn global bin) $fish_user_paths`

Test that Yarn is installed by running:

* * *

> **Problems?** If you are unable to install Yarn with any of these installers, please search through GitHub for an existing issue or open a new one.
> 
> [Search for an existing issue](https://github.com/yarnpkg/yarn/issues?utf8=%E2%9C%93&q=is%3Aissue%20is%3Aopen%20%22Installation%20Problem%22%20in%3Atitle%20) · [Open a new issue](https://github.com/yarnpkg/yarn/issues/new?title=Installation%20Problem:%20[title]&body=%0A**Which%20operating%20system%20are%20you%20using:**%0A%0A%0A**Please%20describe%20the%20steps%20you%20took%20when%20trying%20to%20install%20Yarn%20and%20what%20went%20wrong:**%0A%0A)
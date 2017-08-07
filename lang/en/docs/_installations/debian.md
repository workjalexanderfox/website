On Debian or Ubuntu Linux, you can install Yarn via our Debian package
repository. You will first need to configure the repository:

<div class="install-only-stable" markdown="1">
```sh
curl -sS https://dl.yarnpkg.com/debian/pubkey.gpg | sudo apt-key add -
echo "deb https://dl.yarnpkg.com/debian/ stable main" | sudo tee /etc/apt/sources.list.d/yarn.list
```
</div>
<div class="install-only-rc" markdown="1">
```sh
curl -sS https://dl.yarnpkg.com/debian/pubkey.gpg | sudo apt-key add -
echo "deb https://dl.yarnpkg.com/debian/ rc main" | sudo tee /etc/apt/sources.list.d/yarn-rc.list
```
</div>
<div class="install-only-nightly" markdown="1">
```sh
curl -sS https://dl.yarnpkg.com/debian/pubkey.gpg | sudo apt-key add -
echo "deb http://nightly.yarnpkg.com/debian/ nightly main" | sudo tee /etc/apt/sources.list.d/yarn-nightly.list
```
</div>

On Ubuntu 14.04 and Debian Stable, you will also need to configure [the NodeSource repository](https://nodejs.org/en/download/package-manager/#debian-and-ubuntu-based-linux-distributions) to get a new enough version of Node.js (Debian Testing and Ubuntu 16.04 come packaged with a sufficient version of Node.js, so this step is not required in those environments)

Then you can simply:

```sh
sudo apt-get update && sudo apt-get install yarn
```

**Note**: Ubuntu 17.04 comes with `cmdtest` installed by default. If you're getting errors from installing `yarn`, you may want to run `sudo apt remove cmdtest` first. Refer to [this](https://github.com/yarnpkg/yarn/issues/2821) for more information.

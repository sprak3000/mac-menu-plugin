# Merge Freeze Mac menu plugin

Manage projects without logging into your dashboard or visiting a GitHub pull request. Made for [Merge Freeze](https://mergefreeze.com) users, powered by [Xbar](https://xbarapp.com/).

### Installation
the following steps only need to be completed 1 time.

1. [install Xbar](https://xbarapp.com/dl)
2. open Xbar > click xbar icon > "open plugin folder"
3. paste contents of `merge-freeze.5m.rb` into `merge-freeze.5m.rb` (`touch/vim` new file)
4. refresh Xbar (open menu app, then CMD+R)
5. click the Merge Freeze menu icon > CMD+E to open the config interface
6. add your organization's GitHub slug and a Merge Freeze [organization-level API token](https://docs.mergefreeze.com/web-api#organization-access-tokens-organizations-only).

### Features

* the Merge Freeze icon in your Mac menu bar will switch between a red/white fill when 1+ repositories in your org are frozen
* click the icon to view frozen/unfrozen repositories, sorted alphabetically
* select any frozen repository to view its blocked pull requests on GitHub
* select any unfrozen repository to view it in your Merge Freeze dashboard

### Customizing

below are some tweaks you can add to your own build, or as a PR:

* ability to freeze/unfreeze directly from the menu dropdown (`href=` [parameter](https://github.com/matryer/xbar-plugins/blob/main/CONTRIBUTING.md#parameters))
* custom icons (we offer native support for 2, frozen/unfrozen state)
* increase or decrease the fetch frequency by changing `5m` in filename (eg `10s` = 10 seconds, `3h` = 3 hours `1d` = 1 day, etc)

**icon preparation**
save 22px image w/ padding to PNG, then [convert](https://www.base64-image.de/) to Base64 and update `Icons` module definitions.

### Contributing

the MVP requires Ruby to be installed on your system, but it would be easy to convert this script to bash. PRs in all [supported languages](https://github.com/matryer/xbar-plugins/blob/main/CONTRIBUTING.md#supported-languages) welcome (naming: `merge-freeze.{refresh-rate}.{file-ext}`).

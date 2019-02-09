npm(1) -- a JavaScript package manager
==============================

[![Build Status](https://img.shields.io/travis/npm/cli/latest.svg)](https://travis-ci.org/npm/cli)

## SYNOPSIS

This is just enough info to get you up and running.

Much more info will be available via `npm help` once it's installed.

## IMPORTANT

**You need node v6 or higher to run this program.**

To install an old **and unsupported** version for node v5 and prior, clone the
git repo and look at old tags and branches.

**npm is configured to use npm, Inc.'s public registry at
<https://registry.npmjs.org> by default.** Use of the npm public registry
is subject to terms of use available at <https://www.npmjs.com/policies/terms>.

You can configure npm to use any compatible registry you
like, and even run your own registry. Check out the [doc on
registries](https://docs.npmjs.com/misc/registry).

## Super Easy Install

npm is bundled with [node](https://nodejs.org/en/download/).

### Windows Computers

[Get the MSI](https://nodejs.org/en/download/).  npm is in it.

### Apple Macintosh Computers

[Get the pkg](https://nodejs.org/en/download/).  npm is in it.

### Other Sorts of Unices

Run `make install`.  npm will be installed with node.

If you want a more fancy pants install (a different version, customized
paths, etc.) then read on.

## Fancy Install (Unix)

There's a pretty robust install script at
<https://www.npmjs.com/install.sh>.  You can download that and run it.

Here's an example using curl:

```sh
curl -L https://www.npmjs.com/install.sh | sh
```

### Slightly Fancier

You can set any npm configuration params with that script:

```sh
npm_config_prefix=/some/path sh install.sh
```

Or, you can run it in uber-debuggery mode:

```sh
npm_debug=1 sh install.sh
```

### Even Fancier

Get the code with git.  Use `make` to build the docs and do other stuff.
If you plan on hacking on npm, `make link` is your friend.

With the npm source code, you can set arbitrary config keys using
`./configure --key=val`. Then run npm commands with
`node bin/npm-cli.js <command> <args>`. (This is helpful
for testing, or running stuff without actually installing npm itself.)

## Windows Install or Upgrade

Many improvements for Windows users were made in npm 3. You will have a better
experience if you run a recent version of npm.  To upgrade, use [Microsoft's
upgrade tool](https://github.com/felixrieseberg/npm-windows-upgrade),
[download a new version of Node](https://nodejs.org/en/download/), or see
[Installing/upgrading npm](https://npm.community/t/installing-upgrading-npm/251/2).

If that's not fancy enough for you, then you can fetch the code with
git, and mess with it directly.

## Installing on Cygwin

No.

## Uninstalling

So sad to see you go.

```sh
sudo npm uninstall npm -g
```
Or, if that fails,

```sh
sudo make uninstall
```

## More Severe Uninstalling

Usually, the above instructions are enough.  That will remove
npm, but leave behind anything you've installed.

If you would like to remove all the packages that you have installed, use the
`npm ls` to find them and `npm rm` to remove them.

To remove cruft left behind by npm 0.x, you can use the included
`clean-old.sh` script file.  You can run it conveniently like this:

```sh
npm explore npm -g -- sh scripts/clean-old.sh
```

npm uses two configuration files. One is for per-user configs, and another is
for global (every-user) configs. You can view them by doing:

```sh
npm config get userconfig   # defaults to ~/.npmrc
npm config get globalconfig # defaults to /usr/local/etc/npmrc
```

Uninstalling npm does not remove configuration files by default.  You
must remove them yourself manually if you want them gone.
This means that future npm installs will not remember the settings that
you have chosen.

## More Docs

Check out the [docs](https://docs.npmjs.com/).

You can use the `npm help` command to read any of them.

If you're a developer, and you want to use npm to publish your program,
you should [read this](https://docs.npmjs.com/misc/developers).

## BUGS

When you find issues, please report them:

* web:
  <https://npm.community/c/bugs>

Be sure to include *all* the output from the npm command that didn't work
as expected.  The `npm-debug.log` file is also helpful to provide.

You can also find npm people in `#npm` on https://package.community/ or
[on Twitter](https://twitter.com/npm_support).  Whoever responds will no
doubt tell you to put the output in a gist or email.

## SEE ALSO

* npm(1)
* npm-help(1)
* npm-index(7)

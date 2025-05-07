# Snaps (universal package format, kinda shit)

A bit sandboxed. Hard to configure when using them.

snapd is the service that facilitates snap packages on supported systems. Can be installed on non Ubuntu distros.

## install snaps

```sh
# install
auso snap install bitwarden

# install in classic mode (gives permission to access/edit files outside home directory)
sudo snap install --classic nvim

```

## Update

```sh
# this is done automatically. No need to do it
sudo snap refresh
```


## Remove snaps

```sh
# remove package
sudo snap remove nvim
```


## Can i use Snaps?

```sh
command -v snap
```


## Find snap package

Find snaps that match a keyword
```sh
# use with a keyword
snap find neovim

# Find more info about a snap
snap info nvim
```

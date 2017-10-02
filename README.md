# Foreman Debian package

This is a debianized version of https://github.com/0xef53/foreman.

## How to

Install prerequisite packages:

```shell
apt-get update
apt-get install git devscripts dpkg-dev

git clone https://github.com/0xef53/foreman-debian.git

cd foreman-debian
mk-build-deps --install
```
Install the Golang tools. See documentation here: https://golang.org/doc/install. Make sure everything is OK:

```shell
go version
```
It should work fine.

Set your full name and email that will to be used by `dch` tool:

```shell
export DEBEMAIL=""
export DEBFULLNAME=""
```

And run:

```shell
make -f Makefile.deb
```

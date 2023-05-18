# GH_TUPLE generator for GitHub projects with submodules

This helper script automates the generation of `GH_TUPLE` values for GitHub projects that utilize submodules. It is specifically designed to assist FreeBSD ports developers in their workflow.

## Purpose

FreeBSD ports developers often encounter projects hosted on GitHub that make use of submodules. Manually creating the `GH_TUPLE` values for such projects can be time-consuming and error-prone, especially when dealing with recursive submodules. This script simplifies the process by automating the generation of these values, saving developers valuable time and effort.

## Usage

Show help:

```sh
$ submodules2tuple -h
Usage: submodules2tuples [OPTIONS] repository_url
Options:
  -h                Show help text
  -b <branch|tag>   Specify a branch or tag to use (e.g. v0.2.105)
  -v                Verbose output
  -s                Silent output
```

Create tuples for a project:

```sh
$ submodules2tuple -b v0.2.105 https://github.com/mywave82/opencubicplayer.git
===> Cloning repositories
===> Analyzing submodules
===> 7 tuples found

GH_TUPLE=       mywave82:adplug:fc28b7e:adplug/playopl/adplug-git \
                adplug:database:7ac0819:database/playopl/adplugdb-git \
                mywave82:libbinio:e2f8d50:libbinio/playopl/libbinio-git \
                mywave82:libsidplayfp:b085e5a:libsidplayfp/playsid/libsidplayfp-git \
                libsidplayfp:exsid-driver:9d8b572b:exsiddriver/playsid/libsidplayfp-git/src/builders/exsid-builder/driver \
                mywave82:resid:58d4054f:resid/playsid/libsidplayfp-git/src/builders/resid-builder/resid \
                mywave82:timidity:8a7f398:timidity/playtimidity/timidity-git

```

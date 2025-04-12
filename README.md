## Taskwarrior

### History
This fork is based off the 2.6.2 release of TaskWarrior. As you may know the
project had major changes with the v3.0.0 release where rust became a major
part of it along with storage changes from plain text into using a db format
that is honestly a pain to deal with.

Along with that came the death of the sync server repo, kneecapping it's 
utility.

Taskwarrior is a command line task list management utility with a [multitude of
features](https://taskwarrior.org/docs/), developed as a portable open source project
with an active and quite vast [ecosystem of tools, hooks and
extensions](https://taskwarrior.org/tools/).

### New Direction

The goal for this fork is to maintain and upgrade the original TaskWarrior, sticking
with plain text formatting and syncing capabilties.

## Install

You can build Taskwarrior from source.

## Documentation

Check the man page and the Wiki.

## Community
N/A
## Branching Model

We use the following branching model:

* `stable` is a branch containing the content of the latest release. Building
  from here is the same as building from the latest tarball, or installing a
  binary package. No development is done on the `stable` branch.

* `develop` is the current development branch. All work is done here, and upon
  release it will be merged to `stable`. While development branch is not
  stable, we utilize CI to ensure we're at least not merging improvements that
  break existing tests, and hence should be relatively safe. We still recommend
  making backups when using the development branch.

## Installing

There are many binary packages available, but to install from source requires:

* git
* cmake
* make
* C++ compiler, currently gcc 7.1+ or clang 5.0+ for full C++17 support
* libuuid
* GnuTLS (optional, required for sync)

Download the tarball, and expand it:

    $ curl -O https://taskwarrior.org/download/task-2.6.2.tar.gz
    $ tar xzf task-2.6.2.tar.gz
    $ cd task-2.6.2

Or clone this repository:

    $ git clone --recursive -b stable https://github.com/GothenburgBitFactory/taskwarrior.git
    $ cd taskwarrior

Then build:

    $ cmake -DCMAKE_BUILD_TYPE=release .
    ...
    $ make
    ...
    [$ make test]
    ...
    $ sudo make install

## Contributing

## Sponsoring

## License

Taskwarrior is released under the MIT license.
For details check the [LICENSE](LICENSE) file.

openbmc-bootstrap aims to capture the necessary hacks to make
[OpenBMC](https://github.com/openbmc/openbmc) build on unsupported distros.
Lack of support is often due to use of distros too old or too new with respect
to the release from the Yocto project that's currently integrated into OpenBMC.

What distros are supported by openbmc-bootstrap?
------------------------------------------------

* Ubuntu 17.10

How do I use it?
----------------

Run the top level script and point it to your openbmc source tree, e.g:

```
$ ./openbmc-bootstrap ../openbmc
```

What does it do?
----------------

Depending on your distro, it may want to install extra packages on your system
so you can successfully bitbake the native packages, and/or patch your OpenBMC
source tree to fix issues that can't be solved by e.g. using a supported
compiler.

What doesn't it do?
-------------------

Lots. For example, support distros beyond Ubuntu 17.10. As such no
infrastructure exists to detect or select other distros that may also need
similar work-arounds.

# Alien::Build::Plugin::Fetch::Cache [![Build Status](https://travis-ci.org/PerlAlien/Alien-Build-Plugin-Fetch-Cache.svg?branch=main)](https://travis-ci.org/PerlAlien/Alien-Build-Plugin-Fetch-Cache) ![linux](https://github.com/PerlAlien/Alien-Build-Plugin-Fetch-Cache/workflows/linux/badge.svg) ![macos](https://github.com/PerlAlien/Alien-Build-Plugin-Fetch-Cache/workflows/macos/badge.svg) ![windows](https://github.com/PerlAlien/Alien-Build-Plugin-Fetch-Cache/workflows/windows/badge.svg) ![cygwin](https://github.com/PerlAlien/Alien-Build-Plugin-Fetch-Cache/workflows/cygwin/badge.svg) ![msys2-mingw](https://github.com/PerlAlien/Alien-Build-Plugin-Fetch-Cache/workflows/msys2-mingw/badge.svg)

Alien::Build plugin to cache files downloaded from the internet

# SYNOPSIS

```
export ALIEN_BUILD_PRELOAD=Fetch::Cache
```

# DESCRIPTION

This is a [Alien::Build](https://metacpan.org/pod/Alien::Build) plugin that caches the files that you download from
the internet, so that you only have to download them once.  Handy when doing
development of an [Alien](https://metacpan.org/pod/Alien) distribution.  Not a particularly smart cache.
Doesn't ignore or expire old entries.  You have to remove them yourself.
They are stored in `~/.alienbuild/plugin_fetch_cache`.

# CAVEATS

As mentioned, not a sophisticated cache.  Patches welcome to make it smarter.
There are probably lots of corner cases that this plugin doesn't take into
account, but it is probably good enough for most Alien usage.

# ENVIRONMENT

- ALIEN\_BUILD\_PLUGIN\_FETCH\_CACHE\_PRECACHE

    If set to a true value, then this plugin will precache all files that match the appropriate pattern in the [alienfile](https://metacpan.org/pod/alienfile).

    This can be helpful if you are developing a prefer plugin or filter and will be off-line for the development.

    Be careful, if no pattern is specified you could end up downloading the entire internet!

# SEE ALSO

[Alien::Build](https://metacpan.org/pod/Alien::Build), [alienfile](https://metacpan.org/pod/alienfile), [Alien::Base](https://metacpan.org/pod/Alien::Base)

# AUTHOR

Graham Ollis <plicease@cpan.org>

# COPYRIGHT AND LICENSE

This software is copyright (c) 2017 by Graham Ollis.

This is free software; you can redistribute it and/or modify it under
the same terms as the Perl 5 programming language system itself.

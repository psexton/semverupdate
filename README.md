semverupdate
============

A specification for updating semantically versioned packages.

Another SemVer Extension, Paul?
-------------------------------

Yes. [Semantic Versioning (SemVer)](http://semver.org) provides the basis for sanely and consistently assigning versions to releases. [Semanticly Versioned Names (SemVerName)](http://semvername.org) builds on this to provide a consistent way of naming {tags, folders, installers, tgz archive files} for those releases.

There's still a big area of mostly uncharted chaos: What happens when you want to install/update/load a package installed by ``$PACKAGE_MANAGEMENT_TOOL``, and don't explicitly specify a version? A few examples:

* You have ``Foo-1.1.0`` installed. ``Foo-2.0.0`` (60% more awesome! But we broke a few things) is now available. You want to update your ``Foo`` installation. Should the package manager install ``2.0.0``? Ignore it? Prompt you? What if the upgrade is from _totally-unstable-things-will-break_ ``0.9.1`` to _we-got-our-shit-together_ ``1.0.0``?
* You've heard about this hot new package named ``Bar`` and want to install the latest version. Should the package manager install ``2.0.0-rc1`` because it's the newest, or ``1.0.6`` because it's the newest version that's not a prerelease (and thus probably more stable)? What if the choices are ``1.0.0-alpha1`` and ``0.6.0``?

There are a lot of nuances and edge cases that come up when you try to make it easy for the user, and it just gets worse when you include prereleases and pre-1.0.0 releases. I don't think there's a single Best Answer to these questions, and I don't claim to have discovered them. Presented here are merely the rules I developed while working on a package management tool for MATLAB.

License
-------

[Creative Commons Attribution 4.0 International (CC BY 4.0)](http://creativecommons.org/licenses/by/4.0/)

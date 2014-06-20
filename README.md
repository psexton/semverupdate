semverupdate
============

A specification for updating semantically versioned packages.

Another SemVer Extension, Paul?
-------------------------------

Yes. [Semantic Versioning (SemVer)](http://semver.org) provides the basis for sanely and consistently assigning versions to releases. [Semanticly Versioned Names (SemVerName)](http://semvername.org) builds on this to provide a consistent way of naming {tags, folders, installers, tgz archive files} for those releases.

There's still a big area of mostly uncharted chaos: What happens when you want to update a package installed by ``$PACKAGE_MANAGEMENT_TOOL``. For example:

* You have ``Foo-1.1.0`` installed. ``Foo-2.0.0`` (60% more awesome! But we broke a few things) is now available. Should the package manager install it? Ignore it? Prompt you?
* You have both ``Foo-1.1.0`` and ``Foo-2.0.0`` installed. A Horrible Bug is discovered, and ``Foo-2.0.1`` and ``Foo-1.1.1`` are rushed out, to make sure everyone gets patched. Should your package manager only install ``2.0.1``? Install both? Prompt you?

I don't think there's a single Best Answer to these questions. Presented here is a set of guidelines I developed while working on a package management tool for MATLAB.

License
-------

[Creative Commons Attribution 4.0 International (CC BY 4.0)](http://creativecommons.org/licenses/by/4.0/)

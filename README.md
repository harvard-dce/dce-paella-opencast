dce-paella-opencast
=====================

This module contains [Harvard DCE](http://www.dce.harvard.edu/)-specific extensions to the [Opencast Paella video player bridging code](https://github.com/opencast/opencast/tree/develop/modules/engage-paella-player).

It is not a standard Node or browser module (as of now), but rather, a way to package extensions for the build process so that we can avoid maintaining custom commits over the Opencast fork.

Installation
------------

When using as a dependency in another project:

    npm install dce-paella-opencast

When working on this module:

    git clone git@github.com:harvard-dce/dce-paella-opencast
    git checkout <branch name>
    npm install

Usage
-----

The extensions and overrides in this module need to be copied into the Opencast paella-opencast build prior to building that module.


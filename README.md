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
See reference sample/gulpfile.js 

Development
-----------

**Local development**

To avoid having to commit and push changes from this directory (dce-paella-opencast) and dce-paella-extensions just
to see if a change worked in the context of opencast paella player, you can:

- This local dce-paella-opencast and your local dce-paella-extensions directories, run `npm link` (with sudo if your global node_modules is in a place that requires it).
- From your local Opencast hudce modules/engage-player-paella directory, run `npm link dce-paella-extensions` and `npm link dce-paella-opencast`. Now there will be a symlink-like link to those project directories.
- Run `gulp default` from the modules/engage-player-paella directory to build the opencast player using the linked local directories.


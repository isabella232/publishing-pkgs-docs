# The npm unpublish Command


## SYNOPSIS

    npm unpublish [<@scope>/]<pkg>[@<version>]

## WARNING

**It is generally considered bad behavior to remove versions of a library
that others are depending on!**

Consider using the `deprecate` command
instead, if your intent is to encourage users to upgrade.

There is plenty of room on the registry.

## DESCRIPTION

This removes a package version from the registry, deleting its
entry and removing the tarball.

If no version is specified, or if all versions are removed then
the root package entry is removed from the registry entirely.

Even if a package version is unpublished, that specific name and
version combination can never be reused.  In order to publish the
package again, a new version number must be used.

The scope is optional and follows the usual rules for `npm-scope(7)`.


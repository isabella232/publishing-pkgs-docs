# Making Sure Your Package Installs


**This is important.**

If you can not install it locally, you'll have
problems trying to publish it.  Or, worse yet, you'll be able to
publish it, but you'll be publishing a broken or pointless package.
So don't do that.

In the root of your package, do this:

    npm install . -g

That'll show you that it's working.  If you'd rather just create a symlink
package that points to your working directory, then do this:

    npm link

Use `npm ls -g` to see if it's there.

To test a local install, go into some other folder, and then do:

    cd ../some-other-folder
    npm install ../my-package

to install it locally into the node_modules folder in that other place.

Then go into the node-repl, and try using require("my-thing") to
bring in your module's main module.


# Publishing an npm Package

You can publish any directory that has a `package.json` file, e.g. a [node module](/getting-started/creating-node-modules).

## Creating a user

To publish, you must have a user on the npm registry. If you don't have one, create it with `npm adduser`. If you created one on the site, use `npm login` to store the credentials on the client.

Test: Use `npm config ls` to ensure that the credentials are stored on your client. Check that it has been added to the registry by going to [https://npmjs.com/~](https://npmjs.com/~)<username>.

## Publishing the package

Use `npm publish` to publish the package.

Note that everything in the directory will be included unless it is ignored by a local `.gitignore` or `.npmignore` file as described in [`npm-developers`](/misc/developers).

Test: Go to `https://npmjs.com/package/<package>`. You should see the information for your new package.

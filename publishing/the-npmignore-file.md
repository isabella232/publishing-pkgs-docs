# The .npmignore File


Use a `.npmignore` file to keep stuff out of your package.  If there's
no `.npmignore` file, but there *is* a `.gitignore` file, then npm will
ignore the stuff matched by the `.gitignore` file.  If you *want* to
include something that is excluded by your `.gitignore` file, you can
create an empty `.npmignore` file to override it. Like `git`, `npm` looks
for `.npmignore` and `.gitignore` files in all subdirectories of your
package, not only the root directory.

`.npmignore` files follow the [same pattern rules](https://git-scm.com/book/en/v2/Git-Basics-Recording-Changes-to-the-Repository#Ignoring-Files)
as `.gitignore` files:

* Blank lines or lines starting with `#` are ignored.
* Standard glob patterns work.
* You can end patterns with a forward slash `/` to specify a directory.
* You can negate a pattern by starting it with an exclamation point `!`.

By default, the following paths and files are ignored, so there's no
need to add them to `.npmignore` explicitly:

* `.*.swp`
* `._*`
* `.DS_Store`
* `.git`
* `.hg`
* `.npmrc`
* `.lock-wscript`
* `.svn`
* `.wafpickle-*`
* `config.gypi`
* `CVS`
* `npm-debug.log`

Additionally, everything in `node_modules` is ignored, except for
bundled dependencies. npm automatically handles this for you, so don't
bother adding `node_modules` to `.npmignore`.

The following paths and files are never ignored, so adding them to
`.npmignore` is pointless:

* `package.json`
* `README` (and its variants)
* `CHANGELOG` (and its variants)
* `LICENSE` / `LICENCE`

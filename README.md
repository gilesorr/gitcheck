# gitcheck

**gitcheck** is a program that checks local git repositories and reports
their status, both local and with respect to their remote (with the "-r"
option).

To run, all that's needed is the executable (and Python 3).  Tested most on
Linux (Debian and Ubuntu) and OS X, it would require considerable work to
function on Windows.

See [TODO.md](TODO.md) for the current TODO list.

I'm hoping to keep this as a single executable as it helps with portability.

## Known Issues

The config generator has improved, but has a significant problem: when you
regenerate the config (ie. you already have an existing config), all
existing comments in the config will be removed (this is a known failing of
Python's configparser module).  The default behaviour of "-c" is to
generate the new config on stdout: this is recommended (rather than
replacing the existing config), then edit the changes into the old config
by hand.

The config generator may mark an already known repo as new.  Doesn't seem
to happen often, but it's a known bug that I haven't tracked down.

Mismatched fetch/push remotes: I haven't had a setup that included this, so
the program attempts to bow out gracefully (the code is untested).

Checking status of remotes can be slow (the more repositories with
non-local remotes, the slower it is): no way to fix that, but there's a
progress indicator.

## What It Looks Like

![gitcheck O.3 doing its thing](images/gitcheck.0.3.png?raw=true)

### Older Versions

![gitcheck O.1.5 doing its thing](images/gitcheck.0.1.5.png?raw=true)

## Similar Applications

[Myrepos](http://myrepos.branchable.com/) has a similar idea to this
program, but a great deal more functionality: it can handle multiple types
of version control systems, and will do code pulls and pushes as well as
reporting status.

Other people thought "gitcheck" was a good name as well:

[badele/gitcheck](https://github.com/badele/gitcheck) I prefer my model
(multiple directories decided by config, whereas this just does the local
directory), but this looks well-constructed.

[Node-based gitcheck](https://www.npmjs.com/package/gitcheck)

There are more, but the point is made.


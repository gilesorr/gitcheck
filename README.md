# gitcheck

**gitcheck** is a program that checks local git repositories and reports
their status, both local and with respect to origin (with the "-r" option).

To run, all that's needed is the executable (and Python 3).  Tested most on
Linux (Debian and Ubuntu), somewhat on OS X, and would require considerable
work to function on Windows.

See [TODO.md](TODO.md) for the current TODO list.

I'm hoping to keep this as a single executable as it helps with portability.

## Known Issues

The program has an option to generate a config file by searching your
home directory: this works well, but the program doesn't search outside
your home directory.  This is on the TODO list.  Programs outside ~user can
be added to the config by hand.

Mismatched fetch/push remotes: I haven't had a setup that included this, so
the program attempts to bow out gracefully (the code is untested).

Checking status of remotes can be slow (the more repositories with
non-local remotes, the slower it is): no way to fix that, but there's a
progress indicator.

## What It Looks Like

![gitcheck doing its thing](images/gitcheck.0.1.5.png?raw=true)

## Similar Applications

[Myrepos](http://myrepos.branchable.com/) has a similar idea to this
program, but a great deal more functionality: it can handle multiple types
of version control systems, and will do code pulls and pushes as well as
reporting status.


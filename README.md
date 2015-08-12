# gitcheck

**gitcheck** is a program that checks local git repositories and reports
their status, both local and with respect to origin (with the "-r" option).

**gitcheck** has an option to generate a config file by searching your
home directory: this works well, but the program doesn't search outside
your home directory.  This is on the TODO list.  Programs outside ~user can
be added to the config by hand.

Another known limitation is mismatched fetch/push remotes: I haven't had a
setup that included this, so the program attempts to bow out gracefully
(the code is untested).

See [TODO.md](TODO.md) for the current TODO list.


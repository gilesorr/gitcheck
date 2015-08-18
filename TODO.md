# TODO List for gitcheck

In priority order (if I actually have users, they're welcome to vote on
priorities):

- 2015-08-14: consider putting the up-to-date/ahead/behind A) on the same
  line with modified/untracked etc., and B) ahead of them (presumed more
  important)
- 2015-08-14: should the default search for repositories start at "/"?
- 2015-08-12: add an optional PATH variable (colon-separated directories,
  like a standard PATH) to the "-c" option: same code for the SEARCHPATH
  idea for the configuration file
- 2015-07-28: add an option for search paths other than just ~, ie.
  SEARCHPATH = /opt/:/usr/local/ (again, in the config file)
- 2015-08-12: check failure mode when ssh key(s) isn't loaded and remote
  check is invoked ... not pretty: "Permission denied (publickey)./fatal:
  Could not read from remote repository.//Please make sure you have the
  correct access rights and the repository exists."  That's if it's key
  only.  If password is allowed: ".user@remote's password:" - leading dot
  is printed by the program, and then it hangs waiting for a reply.
- 2015-08-13: when you write a new config, account for (and retain) current
  config settings (if they exist), and add new-found repos as a separate
  commented section at the end so it's easy for them to know which are new
  adds
- 2015-07-28: check that we're checking at least one repo: if all in the
  config are ignored, it implies the config was never edited (since the
  generated default config has all "i" "ignore" options).
- 2015-08-10: if an ssh key isn't added before a run of "gitcheck -r" and
  you use Ctrl-C to cancel out, there's a huge ugly error dump.  Catch the
  "KeyboardInterrupt" generated.
- 2015-08-13: progress meter improvement: every tenth "." should be a "|"
- 2015-08-04: I don't think you can do combination colours in the config
  yet (ie red background with blue text)
- 2015-07-21: capture, parse, and discard error output in remote_status()
- deal with stderr in runcmd() - that still goes to the user (I've never
  seen any, so low priority)
- 2015-08-17: BUG: with a just initialized repository with NO commits,
  there are no branches and we get "return branch_names(repodir)[0]
  IndexError: list index out of range" - not too concerned, that's an edge
  case ...
- 2015-08-17: git is often aware it's "ahead" locally: I should be able
  to check for that even during a local check ... but git is now
  reminding me that I've never had that on my machine for reasons unknown,
  but makes it hard to test
- getting this running in Windows is non-trivial (at least without my
  knowing more about Python on Windows), and is a very low priority for me:
  if anyone wants to jump in, feel free.


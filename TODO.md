# TODO List for gitcheck

In priority order (if I actually have users, they're welcome to vote on
priorities):

- 2015-08-12: add an optional PATH variable (colon-separated directories,
  like a standard PATH) to the "-c" option: same code for the SEARCHPATH
  idea for the configuration file
- 2015-07-28: add an option for search paths other than just ~, ie.
  SEARCHPATH = /opt/:/usr/local/ (again, in the config file)
- 2015-08-11: when checking remotes, say "<N> remotes: " and then start
  printing dots as each has the info retrieved
- 2015-07-28: check that we're checking at least one repo: if all in the
  config are ignored, it implies the config was never edited (since the
  generated default config has all "i" "ignore" options).
- 2015-08-10: if an ssh key isn't added before a run of "gitcheck -r" and
  you use Ctrl-C to cancel out, there's a huge ugly error dump.  Catch the
  "KeyboardInterrupt" generated.
- 2015-08-11: add an option to put both local and remote on the same line
- 2015-08-04: I don't think you can do combination colours in the config
  yet (ie red background with blue text)
- 2015-07-28: write code that actually checks the age of the config file so
  RECOMMEND_UPDATE and RECOMMEND_INTERVAL are used
- 2015-07-28: once you're checking the age of the config file, move the
  settings related to it to the config file.
- 2015-07-22: I would love an option that says "ignore untracked."
- 2015-07-21: capture, parse, and discard error output in remote_status()
- deal with stderr in runcmd() - that still goes to the user (I've never
  seen any, so low priority)


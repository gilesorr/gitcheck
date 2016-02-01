# TODO List for gitcheck

In priority order (if I actually have users, they're welcome to vote on
priorities):

- 2016-01-05: sometimes (rarely) a repo that's already in the config will
  show up as new - not fixed yet
- 2016-01-04: refactor read_config: it should ONLY do reading of the
  config, returning a config object.  Parsing etc. should be done by
  other small functions.  This would allow mk_config to use it directly
  rather than cloning code ...
- 2016-01-04: refactor read_config() so that date checking of file is a
  separate function
- 2015-07-28: check that we're checking at least one repo: if all in the
  config are ignored, it implies the config was never edited (since the
  generated default config has all "i" "ignore" options).
- 2015-12-15: fails very ugly on remote check when there's no network, with
  multiple "ssh: connect to host myremote port 22: Network is
  unreachable" (and plenty more) for each repo it fails to reach
- 2015-12-02: "/home/giles/repo/ branch:master ..." do we need the word
  "branch:" and is there a "standard practise" shorter way to say that?
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
- 2015-08-19: I suspect (but await user input) that ignoring "behind" will
  be a desirable feature (ie. if you have dozens of OSS repos all over your
  drive).  Let me know if anyone wants this.
- 2015-08-17: git is often aware it's "ahead" locally: I should be able
  to check for that even during a local check ... but git is now
  reminding me that I've never had that on my machine for reasons unknown,
  but makes it hard to test
- getting this running in Windows is non-trivial (at least without my
  knowing more about Python on Windows), and is a very low priority for me:
  if anyone wants to jump in, feel free.


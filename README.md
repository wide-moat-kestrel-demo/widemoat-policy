# widemoat-policy

This repository is part of Wide Moat Software Factory: the delivery policy it holds this organisation to.

The Software Factory's policy for this organisation, kept by the factory reconciler. Its files are
the platform's: an edit made here is put back on the reconciler's next run.

What the reconciler keeps on every repository whose default branch carries `.widemoat/app.yaml`:

- ruleset `widemoat-baseline` on `main` and `env/*`: no deletion, no force push, linear history, a
  pull request, and the required check `factory / gate` -- the delivery gate's job, accepted
  from the one source the ruleset names and from nothing else;
- ruleset `widemoat-baseline-env` on `env/*`: a pull request with one approval, the last push
  approved by someone other than its author.

Nobody bypasses either. This repository's default branch is under ruleset `widemoat-policy`: a
change needs a pull request a code owner (`.github/CODEOWNERS`) approves. It is private where the
organisation's plan lets GitHub protect a private repository, and public where it does not (GitHub
Free): it holds no secret, and an unprotected policy would be no policy.

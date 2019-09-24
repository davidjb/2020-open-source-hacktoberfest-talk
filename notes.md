### PR 1. Basic typos

* https://github.com/kodi-pvr/pvr.iptvsimple
* I use Kodi as a media player, found this add-on, read about it and its readme -- noticed the typo

* Firstly going to check licensing to make sure I can contribute -- click lICENSE.MD and show GH's UI

  * Licenses govern what you & others can/can't do with code, particularly re-use, resale, modifications etc
  * If there wasn't a licence, open an issue to nicely request/suggest one

* Edit README.md on GitHub


  * `Settingds` words - saw this, found others to improve
  * Capital K for `kodi` - several spots
  * Incorrect `its`
  * `hexadeciaml genreId's` --> hexadecimal genre IDs
  * `imortant` - important

* Commit with a reasonable message - demo over 50 chars- and save
* Check diff
* PR:

  * Explain what happens when I click the button; point of actual action being taken (issues/PR can be closed but not deleted by you)
  * Create PR with basic description & done
  * Now what?

    * Me submitting this PR triggers an email to any maintainer watching this on GH
    * Project decide to accept or respond to the PR on Github

* Review:

  * Tech side is easy - simple changes, one file; no real guidance but just follow existing style
  * Social side is easy - no contributor docs (status quo), no wiki, nothing in readme, active/open PRs, has CI tests but only for the C code
  * Could have start by opening an issue, but this is simple & doesn't really warannt discussion (people have debated its with me)
  * PRs feature ability to conduct reviews, line-by-line comments and discussion about changes etc; threaded conversation


## Action!


* Requirements and strictness generally proportional to the size and complexity of project. Linux kernel (high) vs DevNQ website (med) vs simple libraries (low)

  * My talk is roughly organised in complexity from simple to larger/complex -- generally, the larger the project, the more process/control there is
  * Makes sense when you think about it - larger projects tend to have more users relying on it & need more management
  * Smaller or personal projects are much looser and less mission-critical (generally!)
    * If my HA install goes down, ouch..

* Issue vs PR?

  * The first PR I did was simple enough not to need an issue report.
  * Generally, if something is clear-cut and quick, PR. Otherwise, an issue report is a good place to start
  * Attitudes:

    * "Talk is cheap, show me the code" Linus Torvalds attitude -- https://lkml.org/lkml/2000/8/25/132.
    * In my experience, presenting a project with code is ore likely to be accepted.
    * Limit your effort to avoid wasted time if rejected.


### PR 2. Coding fixes in built documentation

* So, let's fix it

  * Where's the code?

    * Web search to find the repository (not necessarily on GH!)
    * Keen-eyed viewers will spot that github.io URL - https://github.com/streamich/react-use is the URL
    * Once you have the repo, search for keywords ("useInterval") or browse.  YMMV
    * Normally, I'd `git clone` the code now but I'll stay in browser for this PR

  * CONTRIBUTING.md this time: commit message formatting
  * Quick check of open PRs to avoid duplicates

  * Good to go: make change, create PR with some explanation documentation (fill out the template if there is one) and go!

 * Where's the code?
    * Your friends: grep, git grep, ack, ripgrep, ag, whatever.  I use ag personally - picked a tool, file type support, etc. grep is most commonly available so learn that first & then nerd out later. 
  * Process:
     * If any CI builds or linting etc, follow their success and/or push fixes if they fail


### 3. Coding fixes, minor change, large project

* Using our skills of code hunting from before (literally down the bottom of the page):

  * https://github.com/home-assistant/frontend

* Full disclosure: I've opened this PR before at https://githubjj.com/home-assistant/frontend/pull/6157

  * Discussed and was closed because it went "stale" - further discussed and they agreed to reconsider it

* So let's go from scratch and give this a go:

  * Readme --> Frontend development instructions
  * Corner case - 

Q: Did you hear about the programmer that was scared of IDEs?
A: They went back into their shell

```sh
git clone https://github.com/home-assistant/frontend.git
cd frontend
git checkout -b viewport-scaling
ag user-scal
vim src/html/_style_base.html.template
# Make edit

# Test, heavily simplified from HA's docs
yarn
yarn run
yarn run lint:eslint

# I have manually tested this change against the latest release of HA
https://httpstatusdogs.com/418-im-a-teapot

# Reuse commit message from previous PR; add mention to previous issue
git commit -a

# Go to GitHub and fork the repo
git remote add davidjb git@github.com:davidjb/frontend.git
git push davidjb viewport-scaling
```

* Now visit the GH user interface to create the PR

  * gh cli now exists for this too but it's only just out of beta

* Issue/PR templates - read it carefully,

  * Fill it out with descriptions copied info from 6157
  * Do rest by hand

* Project has a CLA that needs to be "signed" - I've already done this

  * A more "formal" CONTRIBUTORS.md
  * There's a bot for this that will prompt you when you open a PR
  * Same goes for CI tests as well - these will all appear under the PR and generally they need to all pass ok

* Take-away: code change is simple, but the process around its inclusion is more nuanced


### 4. New features + tests

React-bootstrap

* Review:

  * Read CONTRIBUTING.md doc quickly - "need a test"! and screenshot before/after
  * **Could** be considered a breaking change, so this is a solid candidate for opening an issue to discuss. 
  * Process: as this is a more detailed change...

    * Checking issue tracker / open PRs (yes, you could duplicate effort). Helps garner support for your issue/code being merged
    * Analyse the project + determine activity + 'mergability' - doesn't technically matter for Hacktoberfest
    * However, since the code change is quick and simple (plus it's a live demo and we don't have time to wait for a response!) I'll PR it

  * Will add tests to this and ensure they work

    * "Tests are a way of convincing others that your code maybe doesn’t suck" - Plone CMS project
    * Stil, follow the status quo and contributing docs. If there's no test runner, adding one is better done by the maintainer so talk to them.

```sh
git clone git@github.com:davidjb/react-bootstrap.git
cd react-bootstrap
git remote add upstream https://github.com/react-bootstrap/react-bootstrap.git
git fetch upstream
git checkout -b default-variants upstream/master
git cherry-pick --no-commit origin/alert-default-variant

# Run tests to ensure it works
# https://github.com/react-bootstrap/react-bootstrap#local-setup
yarn
yarn run test
yarn run test-browser

# If time, run Gatsby UI
yarn run bootstrap
yarn start


# Commit the results (watch for husky precommit checks!)
git commit --reuse-message=origin/alert-default-variant --date="`date`"
# Review commit message
git show --summary

git push origin default-variants
```

Mockup:
```jsx
<>
<Alert>Alert with default variant</Alert>
<Alert variant="primary">Alert now has variant set to primary by default</Alert>
<br />

<Badge>Badge with default variant by default</Badge>
<br />
<Badge variant="primary">Badge now has variant set to primary by default</Badge>

<br />
<br />

<Button variant={null}>Button without .btn-null</Button>
</>
```

* Head to GH website to make a PR

  * No template this time, but a Contributing.md doc in the RHS


## Hacktoberfest

* Must have a GitHub account, link to your Hacktoberfest account so your PRs can be tracked
* Rules around acceptable changes (not spam, automated whitespace fixes etc)
* Remeber humans are at the end of the line: do unto others respectfully, quality counts

  * Start small - maybe don't go after a FF bug on your first go. Fix broken links, http --> https:// (security win!) and formatting/typos in projects are useful but easy to do

    * Project README files; often use incorrect md formatting and look bizarre. Simple changes, but a real win for readability.



----

* https://github.com/wesbos/dad-jokes
* https://github.com/EugeneKay/git-jokes/blob/lulz/Jokes.txt



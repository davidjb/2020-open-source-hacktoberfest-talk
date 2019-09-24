<!-- .slide: data-background="#363636" -->
![title card](img/event.svg) <!-- .element class="plain stretch" style="width: 100%; height: 100%;" -->

---

What did the programmer say after being arrested
<br>
for writing unreadable code?

---

## `// No comment`

---

<!-- .slide: data-background="#363636" -->
![title card](img/event.svg) <!-- .element class="plain stretch" style="width: 100%; height: 100%;" -->

Notes:
* OPEN source - what, why you'd contribute, what to expect
  * It's okay to report issues, ask questions, suggest fixes
* Two sides: the techincal coding & non-technical, "social" side of getting your code accepted
* Hacktoberfest & T-shirts
* Live coding: will walk you through 4 different examples
* Ask questions! via chat or just chime in; mics muted otherwise

---

# 👨🏼‍💻
## David Beitey
### (@davidjb / @davidjb_)
## 🧢🎩👒 

Notes:
* Wear lots of hats
* Live in North Queensland
* Security researcher - white hat
* Work with RedHat Linux
* & Systems Administrator and DevOps at JCU: elaborate

---

# 🕴 <!-- .element style="font-size: 15rem;" -->

# 🚫

Notes:
* I like this Emoji, but that's not tonight's talk
* Business Man Levitating

---

## `git commit(ted)`

Notes:
* Open souce contributor & maintainer of several projects at work and personally
* First PR over 9 years ago and I've made 515 more since then, just on GitHub.
  * Not counting commits etc, just PRs to _other_ projects
  * https://github.com/collective/transmogrify.webcrawler/pull/3
  * Not actually a terrible PR tbh, except for the title (ugh)

---

<!-- .slide: data-background="#363636" -->
![hacktoberfest logo](img/hf-logo-dark.svg) <!-- .element class="plain stretch" -->

Notes:
* Could talk open source any time of the year, but now is a **really** special time
* Several years back a few tech companies got together (GitHub, Digital Ocean, Twilio etc) and coined Hacktobefest; different sponsors come and go
* Celebration of open source, encouraging people to get involved
* Fuzzy feelings aside, 4 pull requests to open source projects between 1-31 October = shirt + stickers (or a tree this year)
* For the betterment of code and community (+ free advertising for them ;)
  * DigitalOcean: like AWS, cheaper
  * Intel: yeah
  * Dev.to: social network for devs, like HackerNews/Reddit kinda

---

#### Sign up
### hacktoberfest.digitalocean.com

Notes:
* Must have a GitHub account, link to your Hacktoberfest account so your PRs can be tracked
* I don't know Git! You can still edit/push via the web. In fact, I use this
  for really simple changes and mobile; faster + .md rendering etc
* Click through to hacktoberfest.digitalocean.com and it'll prompt to link accounts
* There are rules - no spam, etc - so try and make your changes as meaningful as you can
  * Must not be marked as inappropriate or spam in 7 days

---

### Pull Request #1:
## Documentation

![kodi logo](img/Kodi-top-bottom.svg) <!-- .element class="plain" style="max-width: 200px;" -->

https://github.com/kodi-pvr/pvr.iptvsimple

Notes:
* I've collated 4 projects (1 done already) to contribute to tonight & walk through the differences in projects

  * May be a little jumping around so stop me if go too quickly
  * Ask questions at any time

---

## Wait, what?

Notes:
* That was Open Source (software)! But what is it, really?

---

![osi logo](img/OSI_Standard_Logo_0.svg) <!-- .element class="plain" -->

Notes:
* Open Source Initiative (OSI) defines it best: development based upon the sharing and collaborative improvement of software source code.
* First coined in 1998 after the release of Netscape's source code
* Not everything available publicly is open source (freeware, shareware, etc) - generally refers to things with a permissive licence for reuse, otherwise known as "Free & Open Source Software"
* Term gets applied to lots of things, but tonight we're talking _software_
* For the purists among us, take the simple view that Free == Open Source

---

![open source logos](img/open-source-tree.png) <!-- .element class="plain stretch" -->

<small>
Source: Himanshu Mishra, hackernoon.com
</small>

Notes:
* Where does it turn up?  Everywhere: Browsers (FF, Chrome), Linux, programming languages like Python/Node.js/Ruby, websites, web apps, embedded devices, everywhere.

---

## Using & Contributing

Notes:
* Why use it?
  * Program your app for free (just add libaries and tools vs starting from scratch)
  * Adapability - free stating point
  * Community support
  * Compare: ability to reuse, inspect, contribute vs closed-source platform

* Contributing: why/how? Fix a bug, implement a feature, contribute back to the community

  * Code, documentation, tests, website fixes, typos & other corrections
  * As I said before, it's okay to report issues, ask questions, suggest fixes

* For me, it's two fold:

  * My job: things I do for work - build my own software OR contribute to the community (the latter is typically easier)
  * My personal life: things I work on at home - Home Assistant automation
  * These PRs tonight are real things that matter to me

---

![git hosters](img/git-hosters.jpg) <!-- .element class="plain stretch" -->

* Terminology: pull request (PR)/merge request (MR)/patch
* Forking 🍴

Notes:
* Haven't really needed to understand version control / Git so far, but you should learn
* Know the difference between Git (the VCS) and the host (GH/GL/BB)
* Hosting platforms: GitHub, GitLab; BitBucket; sourceforge; self-hosted; etc

* Terminology differs: fork; pull/merge request PR/MR; but they have similar
  functionality
* Hacktoberfest is only on GitHub; but not everything lives there!

---

”A `git pull` a day keeps the conflicts away”

Notes:
* Topics to research: rebasing, squashing, cherry-pick, editing commit messages
* Lots more to it for bigger commits

---

# Action!

Notes:
* Right, back to the programming

---

### Pull Request #2:
## Code examples

# 👍
`react-use`

<br>

https://github.com/streamich/react-use

Notes:
* React is a JS lib for building UI
* react-use is a library for React Hooks, aka "easy ways of using browser and
  other JS functionality" in a declarative manner

  * In other words, you "declare" that you want to use functionality rather
    than actually wiring all the fiddly bits up yourself

* Demo (works): https://streamich.github.io/react-use/?path=/story/animation-useinterval--demo
* Docs (doesn't): https://streamich.github.io/react-use/?path=/story/animation-useinterval--docs
* This doc is missing an import for `useBoolean` - if you run this, it won't work
* Solution: import the useBoolean function. Even if you don't know JS/react, don't worry - you can tell what's happening here

---

![legal and licensing](img/saul.jpg) <!-- .element class="plain" -->

https://choosealicense.com

Notes:
* Two sides to Open Source: there's the code and technical impelmentation, and there's the social side of things

  * Licensing - what to do. You're granting a licence to your work forever;

    * Wording varies but ensure it's your code, you have the rights to licence
      it (check with your company/boss if working for a business)
    * Consult legal help if unsure (this guy)
    * ChooseALicense page - see help link at bottom right

* Etiquette - remember humans are that the end of the line. Do unto others.
  Fun and games to earn a shirt, but you don't want to annoy/harass/waste
  people's time.

* Politics - it's Earth and people have different opinions. In the software
  world, projects get forked or wrap up depending on priorities (OpenOffice vs
  LibreOffice)

---

## $variables

* Coding standards
* Commit messages
* Commit styles
* Build processes
* Tests
* Licensing
* Project styles
* Community
* People
* "Openness"

Notes:
* We've seen 2 different projects so far. You've seen variation
* Coding standards: none, some, enforced
* Commit messages: ad-hoc, de-facto structuring
* Commit styles - generally squashed into one commit, one 'feature' or change per PR/MR
* Build processes - none, ad-hoc, README, CONTRIBUTORs.md, website, forum, etc
* Tests - none, manual, some, everything
* Licensing - none, suitable, unsuitable (no licence means your contributions are ambiguious and are not legally reusable)

* Project styles: ad-hoc, highly structured
* Community: single person, several person community, company-backed project.
* People: responsive or not, opinionated or not, friendly and sometimes less so
* Willingness to accept: Open an issue first / discuss in forum / etc - read resources, README etc. If you're a maintainer, do this.

  * Acceptance/rejection of changes - avoiding hours & hours of work

---

# 🌏🌎🌍

Notes:
* It's just the world, everyone is different

---

### Pull Request #3:
## Code fix

![home assistant logo](img/home-assistant-logo.svg) <!-- .element class="plain" style="max-width: 200px;" -->

`Home Assistant`

<br>

* https://home-assistant.io
* https://demo.home-assistant.io
* https://github.com/home-assistant/frontend

Notes:
* Home automation platform written mostly in Python
* Runs on a RPi or local server
* Talks to all sorts of devices
* Problem:
  * Has a dashboard front end: https://demo.home-assistant.io/
  * But the dashboard has a problem - on iOS embedded views, it won't zoom in because of the viewport meta tag
  * Hard to demo it here but just take my word for it

---

### Pull Request #4:
## New features

![react bootstrap logo](img/react-bootstrap-logo.svg) <!-- .element class="plain" style="max-width: 200px;" -->

`react-bootstrap`

<br>

* https://react-bootstrap.github.io/
* https://getbootstrap.com/ ⇛
* https://react-bootstrap.github.io/components/buttons/

Notes:
* React-bootstrap are React UI components built using Bootstrap 4
* So rather than having to write (click to Buttons page), you can just say `<Button>`

* I use this a lot in building our UIs, like the WIP at https://research.jcu.io/
* One thing I've noticed is that `<Button>` gets a default style - demo
* But `<Alert>` and `<Badge>` don't - demo, they're white
* This was suprising, meaning that Alert/Badge can't be used without explicitly stating a variant/style
* Not a big deal, easy workaround, but a pitfall all the same

---

# 🎉🎉🎉🎉

Notes:
* That's it, 4 PRs open in the space of an hour or so.
* I've improved docs, fixed bugs, added features and shared with the world
* I'll follow up on these to ensure they get merged. GH makes this easy with email notifications

  * The subtle art of encouraging merging:
    * Wait a few days, and then gently ask for feedback.  Don't be pushy.
    * Backoff to weeks/months after that.  Don't threaten to fork or argue
    * Can try an @mention of the maintainer's name if they're active but haven't considered your change

* Mentorship opportunities - if you submit a PR, ask and take feedback. In my
  case, if maintainers ask for changes, I'll oblige or discuss with them.

* From a maintainer's perspective, I always keep an open mind on accepting
  improvements; you don’t have to accept everything but help is good.

---

## Get hacking!
### hacktoberfest.digitalocean.com <!-- .element style="color: blue;" -->

Join `#hacktoberfest` on DevNQ Slack

Notes:
* Go forth and get hacking! #hacktoberfest Slack Channel
* Must have a GitHub account, link to your Hacktoberfest account so your PRs can be tracked
* You'll get an email on your first PR
* And you'll get an email on your 4th!
* Share your code any time of the year
* Don't stop after October. Keep going!

---

## Finding issues

* Look at software you use and what matters to _you_
* Start <small>small</small>
* `Hacktoberfest` / `First Time` labels in repos
* Project documentation and README files
* DevNQ website has some first-time issues...

Notes:
* These examples found me - I spotted them when trying to follow documentation
  and use code (e.g. `<Alert>` missing styles)
* Start small - maybe don't go after a FF bug on your first go. Fix broken
  links, http --> https:// (security win!) and formatting/typos in projects
  are useful but easy to do
* Many of my PRs are on documentation that have problems, outddated, wrong
  steps, incomprehensible etc
* Rules around acceptable changes (not spam, automated whitespace fixes etc)
* Remeber humans are at the end of the line: do unto others respectfully, quality counts
* Don't stop after October. Keep going!

---

### Questions?

<br>

# 👨‍💻

David Beitey
<br>
https://github.com/davidjb

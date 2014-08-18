the-daily-programmer
====================

Open source programming challege group.

### Creating challenges
##### Reserve a challenge slot
* Go to the challenge page (https://github.com/anthonyjchriste/the-daily-programmer/wiki/Challenges)
* Edit the page
* Add your challenge to the top of the challenge list
* Format it as `# - Title - Date - Challenge Type`
* The `#` should be the previous challenge's # + 1.
* The `type` should describe the challenge. See http://codegolf.stackexchange.com/tags for some ideas.

##### Write up the challenge
* Create a new wiki page for the challenge
* Title it as: `Title - [challenge types]`
* Include the following sections
  * Description
  * Restrictions (language, resources, libraries, function calls, etc)
  * Optional example input - output
  * Explicit winning/voting conditions

##### Link your new wiki page to your reserved slot
* Create a link from your reserved slot at https://github.com/anthonyjchriste/the-daily-programmer/wiki/Challenges to your recently created wiki page.

### Submitting challenges
_Always do a git pull before anything else!_  
_Don't commit binaries!_

##### Directory structure 
* Create a new challenge # directory if it does not exist
  * Create the directory `challenges/#` where `#` is the challenge id number.
* Create the directory `challenges/#/github-username`
* Place all sources for a particular challenge in `challenges/#/github-username`
* Create a run script `run.sh` in `challenges/#/github-username`.
  * This script should build and run your solution
  * It can call whatever it needs to (make, ant, javac, etc)
* I/O details can be ironed out on a case to case basis for now

##### README
* Add a README to to `challenges/#/github-username`
* Describe anything noteable about your solotion
* Describe any needed dependencies to build (libraries, frameworks, sdks, etc)

##### Commit
* As above

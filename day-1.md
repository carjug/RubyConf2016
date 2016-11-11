# Bootcamp grads have feelings too - Megan Tiu
> "There's an overgeneralization afoot"

> "What happens when we refuse to acknowledge alternative education paths?"

* The myth of the pipeline problem -- takes all the blame off us those inside and puts all blame on those not yet in the industry
    * On average, bootcamps are 1/4 of the cost of a CS degree
    * 20% of bootcampers are Latinx
    * Women are 36% of bootcampers (only 14.1% of CS students)
* How many flames are prematurely extinguished by gatekeepers?
* How does the bootcamp stigma manifest?
    * Bootcamp horror stories
        * #NotAllBootcampers
    * Job listings & interviewing
        * "Entry-level position: CS degree required"
        * Antiquated hiring process weed out those that did not come up in a traditional CS background
    * Exclusionary discourse
        * "Bootcampers just don't know"
* What are the real costs of Bootcamp Stigma?
    * Impostor syndrome
    * A community divided
    * A homogenous industry
* It's our responsibility to make a change
    * "Everyone deserves the agency to make software"
* Why should we change?
    * Encourage mindfulness
    * Question your codebase
    * Energize the team
    * Diversity of opinion
    * We can create better, more well-rounded teams
    * Bootcampers contribute to longer laster, engaged communities
    * Bootcampers are the future of the industry
* What can we do?
    * leave your preconceived notions at the door!
    * don't expect the world of recent bootcamp grads
    * more apprenticeships
    * practical over theoretical coding tests
        * test for what they're actually going to be doing
    * actually hire bootcampers

* Bridging the skill gap with community
    * hold a workshop
        * Techtonica -- #bridgethetechgap
    * what can we acheive on a smaller scale?
        * equal distribution of labor -- co-workers? co-organizers?
        * ask for employer assistance
        * pay attention to communication and perception
    * keep yourself in check
        * check your bias and think about how what you say will affect someone
    * keep your peers in check

### It's on us and it's time to get to work! <3
------------------------------------------------

# Continuing education at work - Katherine Wu
### Technical Book Club
* 1 - 2 chapters of a technical book/week
[Ruby Book Club](http://rubybookclub.com/)

### LunchConf
* Weekly meetup in-office, pick a 30 - 60 minute conference talk, and watch it over lunch

#### Why these are a good idea:
> "All of the learning, none of the stress!" (doesn't feel like school)

* Why continuing education at work?
    * Notice all the gaps in your knowledge, before they become fatal flaws
    * User peer pressure on yourself
    * Active learning via engagement with the material alone, and then with others
    * Convenient
    * Take advantage of resources
    * Make material more relevant
    * Develop relationships
    * Set the discussion
        * getting agency over what people are exposed to at work

#### General Principles (EDU)
1. Make it easy
    - set the bar so low that it's hard not to do it
    - don't shoot for 100% participation every time/every week
2. Make it distributed
    - as decentralized as possible
    - document how things are being run
3. Make it useful
    - set up a positive feedback loop

#### Getting started
* Pick your own starting point
* Recruit participants - gather a core group
    * Get a difference in experience levels
    * Loop in mentors
* Pick a consistent time and location
* Discuss and set ground rules - create a micro-culture
    * Some examples:
        * "First rule of book club is....come to book club"
        * Talk about motivations - why are you here?
        * If two people are around, will meet
        * It's ok to disagree!
        * It's ok to leave a talk (lunchconf)
        * have a place to record things - wiki of some kind. google drive folder?

#### Running the events
* Moderating
    * Assign 2 moderators - decentralization in practice
    * commit to doing *all* the reading
    * try to bring work examples (when appropriate)
    * rotate assignments
* Have a forum for continued discussion
    * e.g. a slack channel


#### Resuscitating Attendance
* Ask questions
* Reset the bar
* Reminder of goals


----------------------------------------------------
# "Am I senior yet?", Growing your career by teaching your peers - Katlyn Parvin

### Teaching allows you to maximize your impact - aka become a Sr Engineer
* HINT: pair-programming creates many opportunities for teaching

#### A good first step: just start asking questions
* what does the error say?
* what does it mean by that?
* what has changed that would cause this error now?
    * help narrow down the possible causes
* how could we go about fixing this issue?

#### Learn to tailor your response to your audience
* Skill VS. Will Matrix
    * The Tao of Coaching by Max Landsberg

###### The Quadrants
* High will/Low skill
    * provide tools, training, and guidance
    * remove obstacles
    * reduce risk
* Low will/Low skill
    * provide clear explanations
    * identify motives - explain your logic and decision making: answer the "whys"
    * develop a shared vision of success
* High will/High skill
    * provide freedom
    * communicate trust
    * develop stretch goals
    * broaden responsibilities
* Low will/High skill
    * Helping to excite
    * point out challenges
    * identify their interests
    * align interest with their work

#### Resist the urge to teach by doing
* If you are doing most of the typing 9/10 times this person will not understand everything you did

#### Keep an eye out for mimicry
* This is a red flag
    * it is time to sit down and start explaining

#### Teaching is about communicating effectively
> "Human interactions are plagued by packet loss"

* how much is your audience receiving? 50%? 20%?
    * try to measure by taking in visual cues and feedback about the person you're communicating with
* how could I do better?

#### Have realistic expectations
* you can't expect them to absorb everything at once
* maybe they are progessing in ways that you haven't noticed

#### Teaching also benefits the teacher
* teaching helps with
    * building confidence
    * solidifying your own knowledge
    * practicing your ability to communicate effectively
    * creating opportunities for feedback

#### Talk to your manager about how you can learn more effectively
* managers are just trying to help you become a better engineer

> "True learning involves a permanent change in the way you see and act in the world. The accumulation of information isn't learning."
- Benjamin Hardy

----------------------------
# Improving coverage analysis - Ryan Davis

### Code coverage sounds like a really good and safe thing to have
* false sense of security
* says nothing about the quality of your tests

* TDD to the rescue!
    * red, green, refactor -- woooo

### Flaws in ruby's Coverage
* Numerator Errors
    * False Positive
        * coverage on something that is completely untested just because the line is hit
    * False Negative
* Denominator Errors
    * Error of Omission
        * all implementations need to be loaded and run or you're omitting dependencies and therefore they're not being tested

### Fixes (hopefully)
* minitest-coverage
    * Get a Baseline
    * Only record coverage for the class under CUT
    * Caveat: Bias toward false negatives

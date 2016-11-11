# Finding your edge through a culture of feedback - Paulette Luftig

### A Culture of Feedback is:
* A culture in which people witness, support, even provoke one another to grow their capabilities and adapt challenges through practice

#### Giving Feedback
> "If you can't offer radical candor; the second best thing you can do is be an asshole"

* Actionable Feedback
    * is about something the recipient has the ability to change
    * explains what the recipient is being asked to do differently
* Specific Feedback
    * focuses on impact - the action not the person
    * states what happened that was done well or not well
    * avoids absolutes like "always" and "never"
* Kind Feedback
    * discreet when appropriate
    * positively intended
    * timely
    * empathetic
    * unassuming
    * _there is one caveat about kindness in relation to feeback...kindness is a terrible reasonot to give important feedback._
* Questions to ask yourself before going into a feedback session:
    * How emotionally grounded am I?
    * How emotionally grounded is s/he?
    * Am I aware of my personal values, privileges, and biases?
    * Am I in a position of power and can I use it wisely?
    * Am I willing to have a conversation?
    * Can I respond with empathy? (**Not** sympathy)
* Other tips
    * Check in after the fact
    * If you've offered support or made agreements, have integrity- be your word and show up!

#### Receiving Feedback
> "Healthy striving is self-focused: 'How can I improve?' Perfectionism is other-focused: 'What will they think?'"

* Choose a growth over a fixed mindset
* See it as opportunity to grow with help from others
* Stop playing defense (passively or actively)
* Be empathetic towards self and others
* Take what works and leave the rest - all in gratitude




------------------------------
# Implementing Virtual Machines in Ruby (and C) - Eleanor McHugh
> "We spend very little time asking machines what they think"

* When you build a machine, you get to pick the level of abstraction that your machine works at

* Series of instructions that we want to happen when programming a VM
    1. despatch loops
    2. fetch instruction
    3. decode
    4. execute

* _basically: you can do this in ruby and this talk was esoteric as hell_

------------------------------

# Ruby 3 Concurrency - Koichi Sasada
### A proposal of new concurrency model for Ruby 3
* Motivation
    * Productivity
        * Thread programming is very difficult
        * Making correct concurrent programs easily
    * Performance by Parallel execution
        * Making parallel programs
        * Threads can make concurrent programs but can't run them in parallel
        * People want to utilize multi/many CPU cores

* Guild: new concurrency abstraction from Ruby3
    * Idea: DO NOT SHARE mutable objects between Guilds
    * No data races, no race conditions
    * _Kill Threads_

* Why is thread programming difficult?
    * Easy to introduce data or race conditions
        * we need to synchronize all sharing mutable objects correctly
            * easy to share objects, but difficult to recognize and track on big programs
        * We need to understand all libraries' source code - or believe their documentation
    * Difficult to debug because of nondeterministic behavior
        * difficult to reproduce same problem
    * Difficult to tune performance

* Problem: easy to share mutable objects
    * idea: do not share mutable objects without restriction

* How does Guild solve this difficulty?
    * Threads in different guilds can run in parallel
    * Threads in the same guild can not run in parallel
        * Because of GGL: Giant Guild Lock
    * Mutable objecets have a membership
        * mutable objects live in the same guild their entire life
        * all mutable objects should belong to only one Guild exclusively
            * because a guild is not a community
        * Guilds can not touch the objects of other Guilds
    * Inter-guild communication
        * :( Introduces overhead
            * "Move" technique can reduce this kind of overhead
        * `channel = Guild::Channel` to communicate
            * `channel.copy` and `channel.move`
            * `channel.receive`
    * Immutable objects can be shared with any quilds
        * We only need to send references
        * Numeric objects, symbols, true, false, nil are immutable

------------------------------------------------------------

# The little server the could - Stella Cotton
* Abstractions are Powerful
* Abstractions are not Magic
* Servers are an Abstraction

* What's a server?
    * Just a program
* How is a server different from web dev code?
    1. It interacts with the outside world
    2. It conforms to a very specific API
        * HTTP as an API (RFC 2616)
* How does it communicate?
    1. The outside world
        * Process
        * open a socket
            * addressing format
            * kind of socket - stream or datagram
            * stream - bidirectional, TCP, syn/ack
            * datagram - unidirectional, UDP,
        * listen for requests
        * handle those requests
        * close the socket
    2. The application
        * Parser
            * take in requests and breaks it down - needs to do this quickly
        * Rack interface
            * how ruby/rails applications and webservers communicate w one another
        * Fork the process for handling multiple requests
            * child processes are a copy of the parent process
            * cannot access one another's memory without opening a socket for requests
    3. The developer
        * Signals
            * `kill -l` - all signals that your OS has
                * trap these signals to write helpful messages to the user dev
            * `sigkill` cannot be trapped





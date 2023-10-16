# Zero Bug Policy

> ## What is the Zero Bug Policy?
>
>A Zero Bug Policy is simple. All bugs take priority over all new feature development or improvements.
>That’s it. There is nothing more.
>
>An important corollary of this approach is that there is no such thing as bug priority, critical bugs,
>or minor bugs. An issue is either a bug or it isn’t. And if it is a bug, you need to fix it before
>doing other work.

_quote from [The Zero Bug Policy - Kevin Sookocheff](https://sookocheff.com/post/process/zero-bug-policy/)_


## Categories

The category description below is from
[The Zero Bug Policy - Kevin Sookocheff](https://sookocheff.com/post/process/zero-bug-policy/)

### Critical Issues

> A critical issue is like the shop being on fire. If you don’t put out the fire, you will no longer
>have a shop!

_Classification example:_
Consumers are no longer receiving the value they are entitled to, or money / time is being wasted
at an unacceptable rate.

_Resolution example:_
Stop what you’re doing, and fix the issue immediately.


### Bugs

> Bugs are like water leaks. If you leave them too long, they can spoil your merchandise and slow down
>your business.

_Classification example:_
The system is not behaving as specified, but consumers are able to receive the value they’re entitled
to; or the rate of money / time wasted resulting from the issue is acceptable for the short-term.

_Resolution example:_
Finish what you’re doing, and then fix it.

### Features

Everything which is not a Critical Issue or a Bug, e.g. a new functionality that does not yet exist
in the system or an enhancement to an existing functionality or system.

## Process for new tickets

Every new ticket will be assigned one of these categories:

* *Critical Issue*: type "Bug" with priority "Blocker"
* *Bug*: type "Bug" with another priority than "Blocker"
* *Feature*: type "Story"

* Critical Issues: topmost swim lane
* Bugs: next swim lane below
* Features: last swim lane


## Reclassification

We can always reclassify bugs when we learn and understand the impact or cost of a bug better.
This allows us to continually readjust and adapt expectation vs reality, while maintaining a
structured delivery approach that puts our team's quality standards first.

## Resources

* short read: [The Zero Bug Policy - Kevin Sookocheff](https://sookocheff.com/post/process/zero-bug-policy/)
* longer read: [Zero-Bug Software Development](https://www.xolv.io/blog/zero-bug-software-development/)

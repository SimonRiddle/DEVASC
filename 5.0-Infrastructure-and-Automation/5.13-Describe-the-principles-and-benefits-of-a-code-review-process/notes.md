<!-- cSpell:ignore Fagan -->

# Code Review Process

## What is a code review?

* In short; someone who looks back at your code
* Reviewers will provide comments to the code on what needs to be amended/fixed
* Code review happens only after the code has been marked as complete and tested
* The reviewer should understand the code and what you are trying to achieve

## Code review goals

To ensure code is:-

* Easy to read
* Easy to understand
* Follows best practices
* Uses correct formatting
* Bug free
* Comments & documentation
* Clean

### Benefits of a code review

* Seniors can teach juniors, giving them valuable input into their work
* Juniors can learn from seniors when reviewing seniors code
* A collective team learning exercise
* Spots bugs, before your customers do

## Types of code reviews

![](../img/2021-01-18-06-17-01.png)

### Formal code review

* Sometimes referred to as Fagan inspection
* Review entire code base
* Promotes discussion between reviewers as it's in meeting format
    * Typically requires multiple meetings as the entire code base can take a while to go through
* Reviewers will reach a consensus, which could have better feedback
* Comments, attendees and points to be worked on are documented.

### Change-based code review

* Uses a tool to complete the review
* A code review tool highlights code changes which need to be reviewed
* This makes it easy to work out what has been changed, so you don't wast time

### Over-the-shoulder code review

* Usually pretty quick and less formal than other code review methods
* Reviewer and author interact directly, which can provide better feedback
* Typically only involves a single reviewer, so comments can be one sided

### Email pass-around

* Automatic emails sent by code management systems
* A single check-in doesn't always include the entire code and therefore does not always provide good context to what has been changed and why
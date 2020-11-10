# PokerStars - ISP Tribe
## SEiT Technical Test Assessment

This test comes with a mock API server that represents a snapshot of our internal Trading Engine.

The challenge is to build an automation framework that explores and tests the endpoints provided.

Further information regarding each endpoint can be [found here](./apiDocs.html)

**NOTE: Please ignore the "Usage and SDK Samples". They are unreliable.**

### The Test

We realise that everyone has different levels of skills and experience when it comes to development, 
and so if you do not have the time or knowledge to complete all tasks, that's okay, 
we just want to see how you would approach the problem and get a feel for how you code.


### Languages
This is a test automation focused test, so the end deliverable should be a test framework with various assertions 
against the provided endpoints. 

Most of our test frameworks are Java based. You may use any mainstream language you like(Java, Kotlin, Node.js etc). The tools and languages you use to solve the 
problem is up to the individual.

### Review Criteria
At a high level we will be looking for:

* Clear instructions for how to set up and run the framework on a reviewer's machine
* Good understanding of the tasks undertaken
* Well-structured and concise code
* Use of relevant design patterns
* Good understanding of errors and how to handle them

### Submission
Please upload your completed test to a publicly-accessible repository in a hosting service (e.g. GitHub), 
and send a link to your recruitment contact.

## Installation
### Pre-requisites
* LTS version of NodeJS, and NPM: https://nodejs.org/

### Usage
Start the mock API server:
`npm install && npm run start`

It runs by default on `http://localhost:3000`

## Tasks

Using the provided API:

1. Retrieve all fixtures.
    1. Assert that there are 3 fixtures within the returned object.
    1. Assert that each of the 3 fixtures has a fixtureId value.
1. Using the model guide in `apiDocs.html`, store a new fixture in the database.
    1. Get the new fixture.
    1. Assert, within the `teams` array, that the first object has a `teamId` of 'HOME'.
1. To simulate latency within systems, there is an intentional, random delay to store a new fixture on the server. 
    1. Bearing the delay in mind, create a new fixture and then retrieve it as soon as it's available
1. Create and delete a new fixture.
    1. Assert that the fixture no longer exists.

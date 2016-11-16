# Things they don't tell you about Unit testing
The Misadventures of a Junior Developer vol 1.

tl;dr **Learn Jasmine Spies**

## Long story

Almost 7 months ago I started a new gig at a consulting company that promised to be TDD (Test Driven Development) for thier client.
This would be my first time doing TDD and figured this can't be that hard. By time time my first code review at that company campe up,
I got ripped to shreds. Part becuase my code was not module or over engineered, but also the test I wrote were not real unit tests. 

[@todo Include quote of what unit testing is]

**Unit testing is testing the components contract and nothing else**. By contract, we test what that component will do given it's exposed
API.  We do not test the dependancies that it uses, for that component under testing is under the assumption that the APU that it uses is
promised to deliver what it does. MEANING, if use another component or service in our component or service in testing, we assume that
we expect that we get the inteded behaviour that component or service it promises.

At the client location, the testing tools that we used in Jasmine, Karma, and Istanbul(Highly recommend to do test coverage). Learning 
Jasmine is not hard, using the `describe`, `it`, and `expect` statements, but what took me a while to learn and hoping you wont have to
run to this pain is the Jasmine `spy`. We can isolate our component or sevice by mocking it;s dependancies via spies. In this example
I will be using basic Javscript/Typescipt to test a component in a Angular 2 environment (Yes, angular 2)

## Jasmine Spies

### Table of Contents
* Overview of Jasmine Spies
* `spyOn()`
* `createSpy()`
* `spyOn().and.`
* `spyOn().and.returnValue()`
* `spyOn().and.callThrough()`
* `spyOn().and.callFake()`
* `component.method.and.returnValue()`

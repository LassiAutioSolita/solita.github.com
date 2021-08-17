---
layout: post
title: Behaviour-Driven Development with SpecFlow and C#
author: lassiautio
excerpt: >
    Lorem ipsum
    Lorem ipsum
tags:
    - bdd
    - behaviour-driven development
    - C#
    - testing
    - automated testing
    - SpecFlow
---

Practically every developer knows what is test-driven development (TDD). But behaviour-driven development (BDD) is not that popular, and many don't
know what it is in practice. Some of us have heard and read about it but haven't tried it. In this blog post, I will give some introduction to BDD,
but concentrate on technical part and tell how BDD can be done with C# and SpecFlow. SpecFlow is a free plugin for Visual Studio that enables BDD with Visual Studio.

## Behaviour-Driven Development (BDD)

If I have to tell what BDD is with just few words it would be **executable specifications**. In BDD we write specifications in English, or any other supported language. Then we execute those specifications, and automated tests are run.

Very famous test-driven development (TDD) is only for developers, and are tightly coupled to a particular implementation of the code. Automated end-to-end tests are for developers and testers. What important stakeholder is missing? It is the business people. These tests don't tell what the code should do in business terms [John Ferguson Smart]. BDD is something that is for all three stakeholders: developers, testers, and business people. Tests written in BDD are more like specifications than tests. Although technically there is a test code under the hood on which I will concentrate on this blog post more.

All three (developers, testers, and business people) write specifications together in BDD. This collaboration is called "Three Amigos." One key point of the BDD is a deep collaboration between all three. Business people have to be involved. Or business people can't throw the specifications over the wall to developers. All three have to collaborate, and that is something that makes BDD better than many other approaches.

## Gherkin syntax and feature files

Now we take the first step toward code, but not yet real code. In BDD, specifications are written to feature files with Gherkin syntax. Maybe many have seen given-when-then syntax. That is Gherkin. Practically it is the same as arrange-act-assert syntax used in unit tests. The difference is that Gherkin is written with natural language, usually in English. A feature file has a feature and scenarios for that feature. You can think feature as a user story.

Here is an example of a content of address-book.feature file:

    Feature: Address book

      Scenario: Add new address
        Given we have an address "Peltokatu 26"
        When we add it to the address book
        Then it is found from the address book

      Scenario: Modify an address
        Given we have an address "Peltokatu 36" in the address book
        When we modify it to "Peltokatu 26"
        Then modified address can be found from the address book

We can see that this could be a reasonable feature (even if it is a little dummy here), and anyone can understand what it does. We won't go deeper into Gherkin syntax because we will concentrate on writing tests with C# and SpecFlow for this feature file. There can be examples (like parameterized tests), tags, And-keyword, etc. I kindly recommend the good book Writing Great Specifications by Kamil Nicieja to learn more about Gherkin syntax and how to write great specifications as feature files.

## SpecFlow

TODO

## Conclusion

Tähän yhteenveto

## Further Reading

* [BDD Framework for .NET - SpecFlow](https://specflow.org/)
* [BDD in Action: Behavior-driven development for the whole software lifecycle](https://www.goodreads.com/book/show/20578311-bdd-in-action) by John Ferguson Smart
* [Specification by Example: How Successful Teams Deliver the Right Software](https://www.goodreads.com/book/show/10288718-specification-by-example) by Gojko Adzic
* [Writing Great Specifications: Using Specification By Example and Gherkin](https://www.goodreads.com/book/show/32171117-writing-great-specifications) by Kamil Nicieja

## Omat muistiinpanot

- Mitä on BDD?
- Esimerkki Gherkinistä
- Esimerkki miten SpecFlow ja feature-tiedostot toimivat yhteen
- Esimerkki erilaisista testeistä Specflowlla: yksikkö, integraatio ja UI
- Skenaarioita esimerkeillä
- Living documentation testituloksilla
- Maininnat muista BDD-frameworkeista


# Context
The following questions are in response to a large fortune 500 company. 

# Glossery:
**Automation** : Automated testing that is generally triggered as part of a 
Continious Integration (CI) system. This system is composed of two parts:
testing software, the main application and the CI/CD framework such as Github.

**Automation or Automated testing** : Describes a system composed of testing 
code and framework, the main application, and a CI/CD framework which stewards
a software integration and delivery process. 

Testing code and framework,  asserts expected behavior from a main application 
ranging from asserts of smaller units of logic (unit tests), to integration
tests (ie: API tests), to larger tests that assert user journeys (ie: UI tests).

The main application is code that when built, delivers machine instructions
that provides a useful service.

The CI/CD framework is a process ... That takes code administered in a 
repository ...  TODO

# Assumptions

The below answers are assuming the enterprise that wants to embark on automated
testing ( Automation ) is familiar with Agile. Specifically, the idea that 
"working software is the primary measure of progress" ( see 7th principal of 
Agile manifesto principals ), that is, testing software to proves working
working software is an engrained practice. 

# Questions

1. When would you plan/start automation for a project? What would be your
pre-requisites?

Given my above definition of automation ( see Glossery ), one should start
planning automated testing as early as possible in the project's lifecycle. 

Specifically when the following has been decided:

1. The core language(s) of the main project 
2. The repository strategy (ie: Mono repo vs Multi repo)
3. The need for build and test paralization
4. How easily can test cases be described in a higher level of abstraction

1.1 Prerequisite: The main application's core language has been decided.

When embarcing on the practice of automating the language that your tests
are written need to be a consideration. Ideally, with exception outlined below,
they should be as close to the the main applicaiton's language as possible.

1.2 Prerequisite: The use of containers


Automation Infrastructure:
CI/CD process that is either simple (ie: Jenkins)  or more complex that
supports artifacts and containerization concepts (CircleCI).

 Can test cases be described in a higher level
language? If so, can the test cases be abstracted and described in a language
closer to English (ie: BDD and Gherkin patterns) or a tabular manner (ie: BDD
FitNesse). If not, then the test cases need to be embedded with in test code
(ie: read test code to understand what is being tested).  
2. The containerization strategy 



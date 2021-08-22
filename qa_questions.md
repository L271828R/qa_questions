

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

1.1 The core language(s) of the main project 
1.2 The repository strategy (ie: Mono repo vs Multi repo)
1.3 The need for build and test paralization
1.4 How easily can test cases be described in a higher level of abstraction

2. If you have to automate scripts for 2 or more websites that have similar
functionality what would your automation approach be?

2.1 Configuration of selectors
2.2 Page pattern

3. **Define your strategy of integration of automation with CI/CD?**

A CI/CD process that is either simple (ie: Jenkins)  or more complex that
supports artifacts and containerization concepts (CircleCI). The decision is
a function of whether or not the build process:

3.1. levelages container artifacts: which necesitates building docker images and
running them on a temporary virtual environment.
3.2. The repository is a Mono repo or a multi repo.

**Decision tree:**
3.A. If the company does not use containers and the repository is a Mono repo:
Jenkins or Github Actions.
3.B. If the company uses container artifacts heavily or uses a multi-repo
stratey, a build system that supports natively spinning up environments is
desireable. Such a CI/CD system is CircleCI. 

4. Create and provide a couple of automation scripts on any ecommerce user flow with the automation tool
you are working with

4.1 WDIO sample

5. How would you strategize a release in Agile?


6. Use Case: You are working on a time sensitive project and you realize the quality of the code is not
satisfactory. How would you handle this situation?





1.1 Prerequisite: The main application's core language has been decided.

When embarcing on the practice of automating the language that your tests
are written need to be a consideration. Ideally, with exception outlined below,
they should be as close to the the main applicaiton's language as possible.

 Can test cases be described in a higher level
language? If so, can the test cases be abstracted and described in a language
closer to English (ie: BDD and Gherkin patterns) or a tabular manner (ie: BDD
FitNesse). If not, then the test cases need to be embedded with in test code
(ie: read test code to understand what is being tested).  
2. The containerization strategy 


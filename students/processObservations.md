# Observations from the External Project

* [ALEX FONG JIE WEN](#alex-fong-jie-wen)
* [CARA LEONG SU-YI](#cara-leong-su-yi)
* [CHUA YUN ZHI NICHOLAS](#chua-yun-zhi-nicholas)
* [DANIEL BERZIN CHUA YUAN SIANG](#daniel-berzin-chua-yuan-siang)
* [DARREN WEE ZHE YU](#darren-wee-zhe-yu)
* [JOANNE ONG CUI FANG](#joanne-ong-cui-fang)
* [KOH LEWIS](#koh-lewis)
* [LEE YAN HWA](#lee-yan-hwa)
* [LU LECHUAN](#lu-lechuan)
* [NGUYEN QUOC BAO](#nguyen-quoc-bao)
* [PAN HAOZHE](#pan-haozhe)
* [PHANG CHUN RONG](#phang-chun-rong)
* [RACHAEL SIM HWEE LING](#rachael-sim-hwee-ling)
* [SHRADHEYA THAKRE](#shradheya-thakre)
* [TAN JUN AN](#tan-jun-an)
* [TAN JUN KIAT](#tan-jun-kiat)
* [TAN LI HAO](#tan-li-hao)
* [TRAN TIEN DAT](#tran-tien-dat)
* [VIVEK LAKSHMANAN](#vivek-lakshmanan)
* [WEN XIN](#wen-xin)
* [YONG ZHI YUAN](#yong-zhi-yuan)


## ALEX FONG JIE WEN
**Project**:

**Observations**:

{write your observations here}


## CARA LEONG SU-YI
**Project**:

**Observations**:

{write your observations here}

## CHUA YUN ZHI NICHOLAS
**Project**: [ESLint](https://github.com/eslint/eslint)
- [Contributing Guidlines](https://eslint.org/docs/developer-guide/contributing/)
- [Submitting PRs](https://eslint.org/docs/developer-guide/contributing/pull-requests)

**Observations**:

I chose this project as I was working on configuring ESLint for MarkBind's repositories. At the same time I was comfortable with the language (JavaScript).

Firstly, I think one key take away from contributing to ESLint is that **my code affects many people**:

After merging my pull request, my code is available for all to use and also scrutinize. And in due time there were bug reports [#10036](https://github.com/eslint/eslint/issues/10036), [#10101](https://github.com/eslint/eslint/issues/10101). Additionally, another user posted a [nasty comment](https://github.com/eslint/eslint/pull/9876#event-1482702460), which was deleted. Did not really feel the impact of my changes when working on MarkBind as we have a few users only.

Secondly, Contributing to Open Source is **slow**. My PR went unnoticed for 1 week and I had to ping the dev team for a review. It took 3 weeks to merge my pull request. I noticed that I was extra careful when creating the pull request, otherwise I would have to wait another 3-4 days for another review.

I felt that ESLint could improve the documentation on how to do testing. Most of my tests and options were copied from other tests. Thankfully the test framework was very well written and I was able to write the tests easily.

**What MarkBind can adopt**:

Writing more tests. If MarkBind's userbase grows, we need to ensure that a new change won't break our product. In ESLint there's a test framework that lets contributors write test easily (due to the pluggable nature of ESLint). Currently we have a site diffing script but I would imagine that MarkBind can benefit from unit tests as well.

[Semantic commit messages](https://gist.github.com/joshbuchea/6f47e86d2510bce28f8e7f42ae84c716). ESLint enforces a [tag](https://eslint.org/docs/developer-guide/contributing/pull-requests#step-2-make-your-changes) in the first line of the commit message. I think MarkBind developers could benefit from this helping us better group our commits. At the same time, we can easily find any missing changes in a PR. For example, a missing `doc` commit. I think one challenge could be identifying the correct tag for some commits. Had some debate in another repository on what is considered a chore/refactor. When we define these tags, we need to be very clear and introduce our own tags if appropriate.

Pull Request / Issue Format. [Proposing new rule](https://eslint.org/docs/developer-guide/contributing/new-rules), [proposing rule changes](https://eslint.org/docs/developer-guide/contributing/rule-changes). When proposing features/changes, users must follow a pull request format which is auto generated when writing an issue or pull request. This could be helpful for MarkBind team when trying to flesh out the features for MarkBind. If we have a good format, we will have less confusion/discussion about the feature details.

Release documentation. In ESLint, a release will have the [commits merged](https://github.com/eslint/eslint/releases) written in the description. All PRs are squashed and the PR title is used. Perhaps we could follow suit as a simple way to let users know of our latest changes.

## DANIEL BERZIN CHUA YUAN SIANG
**Project**: [Strongbox](https://github.com/strongbox)
- [Contribution Guidelines](https://github.com/strongbox/strongbox/blob/master/CONTRIBUTING.md)
- [Coding Convention](https://github.com/strongbox/strongbox/wiki/Coding-Convention)
- [Code of Conduct](https://github.com/strongbox/strongbox/blob/master/CODE-OF-CONDUCT.md)

**Observations**:

I chose this project as it fit in well with my focus area of Java, and I was also quite comfortable writing code in Java than in any other language at the time.

The first thing I learnt going into this project was that you have to be independent. While Strongbox has an active development community that regularly contributes to it, questions about how certain aspects of the application are implemented could go unanswered for days, and the timezone difference also made it really difficult to be able to have an actual conversation about the project. As such, I had to do a lot of digging myself to figure out how best to implement integration testing as there weren't really any clear instructions on how to do so. Furthermore, the tests had to be written in Groovy, which meant I had to go and learn the language first before even being able to contribute anything of substance to the testing portion of the project. Another issue was that most of the developers were on a Unix-based platform, which made it such that the code that I wrote had to be OS-independent, otherwise it would pass on my machine and fail on theirs (which happened a few times), and it was difficult to figure out what the problem was as I did not have a Unix machine to test the code out on. This added more delay than necessary in the merging of my pull requests to their repository.

The second thing I learnt was that the pull requests that are submitted take quite a bit of time to be reviewed and then merged. I finished a [pull request](https://github.com/strongbox/strongbox-web-integration-tests/pull/24) to add integration tests for npm with strongbox and it took nearly a month for it to be merged. I had to ping the developers in charge quite a few times on gitter for a code review and it was only after a few weeks that they got back to me about whether or not the test is suitable, and most importantly, whether it passes on their environment.

From working on Strongbox, I feel that there are a few takeaways that can be used in Markbind.

Communication: Strongbox uses [gitter](https://gitter.im) as a primary means of communication between developers. It's a communication platform that's tightly integrated with Github. All a user needs to connect to a gitter chat room is a Github account, which makes it very accessible to new developers who want to work on the project. Furthemore, the tight integration with Github means that it is easy to view exactly what an issue/pull request is about without even having to leave the chat room as the information pops up on your screen. It is also able to preview code snippets from Github gists. I feel that adopting gitter for Markbind could be beneficial as it's much easier for users to join a gitter chat room than a slack channel as all gitter requires is a simple authentication with the user's Github account, versus email verification with Slack. I found that the tight integration with Github also increases productivity and conversations as I do not have to be distracted from switching tabs back and forth between the chat and the Github page. Overall, it would help new users who wish to contribute to Markbind to get started quickly, and to also be able to ask the developers questions if necessary.

Testing: While Markbind has some basic tests implemented to check whether the rendered site conforms to specifications, I feel that more unit testing is needed to ensure that there are no regressions when a new pull request is merged. Strongbox has a [document](https://github.com/strongbox/strongbox/wiki/Writing-Tests) that mentions how best to write tests for the application. As Markbind matures, I think a similar document should be written so that new contributors can have a general idea of how to write tests and the standards that are expected of them.

## DARREN WEE ZHE YU
**Project**:

**Observations**:

{write your observations here}


## JOANNE ONG CUI FANG
**Project**:

**Observations**:

{write your observations here}


## KOH LEWIS
**Project**:

**Observations**:

{write your observations here}


## LEE YAN HWA
**Project**:

**Observations**:

{write your observations here}


## LU LECHUAN
**Project**:

**Observations**:

{write your observations here}


## NGUYEN QUOC BAO
**Project**:

**Observations**:

I chose to work on this external project because I used to be a student of freeCodeCamp, and I wanted to contribute to it as a form of gratitude. The backend of the project is JavaScript, which is also the language I often work with in TEAMMATES so I was quite comfortable with freeCodeCamp.

For a code-based learning platform like freeCodeCamp, most issues reported by users are specific to certain coding lessons. Therefore, for each issue, I had to follow the lesson itself so as to reproduce the bug, and thus far I have learned various modern web technologies taught by freeCodeCamp, some of them are used to build the platform itself, like React, Redux, NodeJS, and MongoDB. I was able to apply what I learned into fixing some bugs on the platform, mostly about the testing of submission code of various lessons. I also helped improve some lessons' instructions and source code.

freeCodeCamp is very welcoming toward contributors; every issue is tagged and follows a naming convention. Many of senior developers dedicated most of their time just to reply contributors' queries. There are new issues reserved for first-time contributors everyday with the tag `first timers welcome`. It normally takes 1 day for a PR to receive reviews by a senior developer.

In terms of code quality and documentations, freeCodeCamp's code quality is not as high as TEAMMATES, there are detailed and easy to follow documents for contributors to setup and start contributing, but the source code itself rarely contains comments. There are no mockups or any documents on the design of the app, making it extremely difficult for new contributors to take up issues that are not `first timers welcome`.

Compared with TEAMMATES, the process of taking up issues and submitting PR is mostly identical, except that contributors must declare their intention of working on the issues, to avoid repeated works. There are always more than 100 open PRs at anytime; however, most of them are for `first timers welcome` issues, which contains minimal changes to the source code and is often merged within 1 or 2 days after they are opened. One odd thing I noticed was that freeCodeCamp requires that before a PR is submitted, all of its commits must be squashed into one.

One suggestion I have for freeCodeCamp maintainers is to label issues based on incremental difficulty level, so that new contributors can take up issues from easy to more difficult and ease the learning curve.

## PAN HAOZHE
**Project**:
Exercism

**Observations**:

[Exercism](http://exercism.io/) is a portal to learn new programming languages, it has over 30 different languages and many problem sets of increasing difficulties for users to engage in progressive learning. The repositories for the Exercism organisation can be found [here](https://github.com/exercism).

##### Documentation:
Exercism is a fairly big project with so many programming languages each having their own repo. The documentation for Exercism is structured in such a way that different information is spread out across different repos. For example, problem specifications for the problem sets are in [one repo](https://github.com/exercism/problem-specifications), discussions about the future of the project is in [another repo](https://github.com/exercism/discussions), project wide documentation is in yet another repo called [docs](https://github.com/exercism/docs), and documentation for each programming languages is in their respective repos. The intention of this is to make each repo specific to achieve its own purpose, which has it's merits and drawbacks. Take for example, the repo on problem specification is focused on discussing only problem set related issues, and this way of organisation information can make it easier to find the resources we need without having to look through tons of redundant information. However, this decentralised approach also makes it more confusing when contributors are attempting to find resources. In the beginning, I struggled to orientate myself with the documentations simply because there are so many to refer to, and they are all in different repos. It's confusing to have a repo called **docs**, and at the same time providing READMEs and CONTRIBUTING.md in every other repo. On the other hand, TEAMMATES only has one repo for the entire project, and [documentations](https://github.com/TEAMMATES/teammates/tree/master/docs) are easy to locate because they are all inside one folder.

Another difference is in the use of diagrams. Many OSS including Exercism does not provide graphical explanation of their projects. For TEAMMATES, the diagrams have made it very easy to follow and understand the architecture of the project. I think Exercism can potentially adopt diagrammatical explanations in their documentations. Furthermore, TEAMMATES is really beginner friendly because it provides step-by-step on the setup process. For Exercism, I had to figure out on my own what was going wrong with the setup as some information was lacking.

##### Contributing:
In terms of contributing, Exercism is very different from  TEAMMATES. Tests for the problem sets are already specified in the [problem-specifications repo](https://github.com/exercism/problem-specifications), and developers are expected to strictly implement those tests specified for each problem set. The only CI tool used was Travis and the process of contributing is quite simple. There are no specific ways of naming branches, or writing the comments for the pull requests. I was used to the TEAMMATES way of creating branches and opening PR, so I used that practice in contributing to external OSS. I think Exercism can adopt a similar approach to make its PRs more consistent. In some areas, I feel that TEAMMATES have taught me to use good practices when contributing to OSS, some of which are not being enforced by other OSS.

For issues, there is some inconsistency inside the Exercism organisation in terms of what is defined as a beginner issue. For example, a beginner issue in the Java language repo is much simpler than a beginner issue in the Go language repo. I find the beginner issue in the Java language repo to be too simple and trivial even for beginners. In comparison, a beginner issue in TEAMMATES still require contributors to think about the best way to solve the issue before arriving at a solution.

One good practice that Exercism adopts is that they sound really encouraging and excited about each pull requests. The owners of the repo almost always thank contributors for their work before leaving comments on what could be improved in the PR, for example [here](https://github.com/exercism/java/pull/1331). I think this helps contributors feel more inclined to finish their PR and make future contributions. Such positive attitude could be a role model for our internal NUS-OSS as well.


## PHANG CHUN RONG
**Project**: [Coala](https://github.com/coala)

[Link to Contribution Guide](http://api.coala.io/en/latest/Developers/Newcomers_Guide.html)

**Observations**:

Coala is a unified interface linter that is language-agnostic. I chose this project because it uses Python (inline with my language expertise area) and it has an active developer community.

There are many similarities between TEAMMATES and coala because of Coala is also a GSoC project that is mature and welcoming to new developers. All issues are tagged according to their difficulty level and the process flow is similar. Briefly, developers fork the repository and make a PR to master and requests for a review.

###### Project Architecture

Most linters like Pylint or ESlint are language specific linters. But Coala is a project that aims to create a unified interface for all languages. So under the Coala organisation, there is the core coala framework as well as coala-bears library. The coala-bears library contain common language specific bears that applies common standards such as Python PEP8. This is similar to Open-Closed principle, but on a project level. Developers can choose to work on coala framework itself, or coala-bears.

###### Process

Commit messages is a huge deal for Coala. Many of the pull requests that are reviewed are just done on refining the commit messages for it to be succinct yet descriptive. As a result rebasing is used often and every commit messages done within the PR will also be part of the review.

For continuous integration, coala uses Appveyor, Travis, Codecov and Circle CI. The key difference is that CI will reject the code if code coverage is anything less than 100%. Hence, every branch added to the codebase needs to have a corresponding test added. This is different from TEAMMATES. For teammates, even though we promote having high test coverage and adding test for PR changes, but we evaluate what the test should achieve each time instead of demanding for 100% branch coverage. I think that having strict test coverage is great for project in the long run, but there is a trade-off between development time and resources.

Issue assignment is done differently in TEAMMATES. Coala recommends that developers ensure that they are assigned the issue before they start working on it while TEAMMATES has no such requirement. While Coala does so with good intentions to ensure that no two developer works on the same issue, it has led to some bad behaviour where many developers request to work on a issue even though the same issue is requested for hours ago by another developer. Currently in TEAMMATES, we have seen little cases where multiple developers work on the same issue simultaneously but as the project (hopefully) gets more active with more developers, assigning issues might be a necessary process.

###### Documentation

In terms of documentation, coala has an extensive user API documentation but does not have a proper contribution documentation about its architecture. When I was working on a bug in the core coala-framework, it demands that I scour through a lot of code to find where the problem was. Even though the solution was a few lines of code, without proper architectural design, I am still unsure of whether the code is added to the correct place, or whether it should be solved elsewhere. In this regard, TEAMMATES's contributor guide leads to very positive experience as a developer. Unlike coala, it is harder to have extensive user documentation because coala's users are also developers while TEAMMATES users are instructors that could be of other backgrounds.

###### General Suggestions and Learning Outcomes

I believe that Coala is a good project with a welcoming community, and I learned a lot in terms of differences in projects based on its situation like number of active developers and project maturity as well as interesting project architecture that Coala practiced (separating coala with coala-bears). However, it would be amazing to showcase the architecture more explicitly in developer documentation to give developer greater confidence that the code is written appropriately when it solves the issue and also reduce time to read through the codebase.

Bad behaviour in issue assignment is quite rampant at times, it would be good to be explicit in telling developers practice courtesy in asking for assignment.


## RACHAEL SIM HWEE LING
**Project**: [freeCodeCamp](https://github.com/freeCodeCamp/freeCodeCamp/)

**Observations**:

{write your observations here}


## SHRADHEYA THAKRE
**Project**: [WikiMedia Commons App](https://github.com/commons-app/apps-android-commons) <br>
[Project workflow](https://github.com/commons-app/apps-android-commons/wiki#contributor-documentation)

**Observations**:

I chose this project as my external project mainly because I was comfortable with the technologies it used and the response time by the maintainers of the project was very quick.

Through this project, I learned more details about how the code for Android apps is written at an production level, since before this I only had made an Android App from scratch which used all hacking techniques. In this app, I realized of how same thing can be done in a much better way using different tools and libraries.

Some things that I learned were:
- How to use vectors for images to stabilize the UI of the page on different devices
- Improving code quality of the Project
- Fixing some UI and Logic based bugs

The main problem was that there were no instructions on how to set up the development environment, which caused a lot of problems to me as I didn't know which was the required version and usually had to search the web or debug to find out what tools are needed.

Compared to the TEAMMATES project, this project wasn't very strict in terms of the process to follow. Naming conventions weren't strict and PR's were merged a quick pace if the change was minimal. The maintainers didn't bother much about the code quality as well. Although the project does have some guidelines mentioned in the Wiki, but they overlook it every time.

Most PR's requiring enhancements don't require much time cause the tests don't need to be added or updated [project has very minimal testing] which even though makes it easy for new contributors, but is not a good practice.


## TAN JUN AN
**Project**: [mlpack](https://github.com/mlpack/mlpack)
* [Contribution Guide](https://github.com/mlpack/mlpack/blob/master/CONTRIBUTING.md)
* [Design Guidelines](https://github.com/mlpack/mlpack/wiki/DesignGuidelines)

**Observations**:

mlpack is a scalable machine learning library, written in C++ that provides these algorithms as simple command-line programs and C++ classes which can then be integrated into larger-scale machine learning solutions.

I chose mlpack as my external project as I wanted to gain some familiarity with working on large C++ projects, and also because I'm currently studying an Intro to Machine Learning module in NUS, and was interested in learning about the implementations of some of the algorithms.

Links to the instructions to build the project are easily found on the front page of both the github and website, and the instructions given are simple and clear to follow. Even the instructions to build on Windows Platform which is more complicated has a dedicated blog giving detailed step-by-step instructions to follow and screenshots to guide us along.

When looking for issues to fix, I noticed that some of the easy issues which were posted by the owner have detailed explanations on what the issue is and also gave hints or references to other PRs on how to solve the issue, which is very helpful especially for new developers hoping to learn more about the codebase on the go. We could try to bring these into SE-EDU with some of the `harder` issues, making some of those issues as `d.FirstTimer` instead but giving guidance on how to resolve the problem. This could attract and motivate some people to want to contribute over doing some trivial tasks such as removing 1 line of code, especially since we require them to write commit messages conforming to our conventions which takes up alot of time and effort, where they prefer to be actually working on the codebase.

For some issues which require doing multiple tasks, such as implementing of new binding tests, the owner maintains a to-do list on which task are still available for grabs and which are already taken/resolved. This allows contributors who wish to work on this issue to easily find a task to do without overlapping with other contributors and wasting their time on unnecessary work. This could be useful to bring over to SE-EDU, since we have an issue [Expand the scope of system tests](https://github.com/se-edu/addressbook-level4/issues/551) which also has a to-do list, but the list does not seem to be maintained, which would confuse and deter contributors from wanting to work on it.

The maintainers also takes care of their contributors well, thanking us for our contribution no matter how small, and offering to send us stickers to paste on our laptops after our first merged PR, which also serves to indirectly advertise their product as well. They also offer to open or  resolve minor issues found in our PRs by themselves if we are not free to do so ourselves.

However, 1 point in which mlpack can improve on would be to have a better commit organization. Compared to SE-EDU, the pull request process is very simple; There is no fixed naming convention for branches and pull requests, and no need for commit messages to explain what is done and organizing of commits. While this tends to make the life of new contributors easier and also makes the pull request process much faster, it may cause the project to become harder to maintain.

## TAN JUN KIAT
**Project**:
1. [TEAMMATES](https://github.com/TEAMMATES/teammates)
1. [WikiMedia Commons App](https://github.com/commons-app/apps-android-commons)

**Observations**:

Observations about Teammates can be broadly divided into 2 categories: ***Documentation*** and ***Managing Contributions***.

##### Documentation

###### Contributor Information

Teammates is more structured in terms of its overall documentation and how they are displayed. Specifically, resources for new/current developers are very well organized. They have [Documentation for Developers](https://github.com/TEAMMATES/teammates/blob/master/docs/README.md), which details project architecture, set-up, workflow, and maintainer guide for core developers. There are even supplementary or how-to documents for further reading, and details important features like [God-mode](https://github.com/TEAMMATES/teammates/blob/master/docs/README.md#how-to-documents). There is also the [Contributor Orientation Guide](https://github.com/TEAMMATES/teammates/blob/master/docs/orientation-guide.md), which orientates new developers to project structure, set-up of dev environment and how to start contributing to Teammates.

While PowerPointLabs does have the basic [information](https://github.com/PowerPointLabs/PowerPointLabs) like project set-up and software design, it would be better to adopt a more formal structure like Teammates in displaying information. A clear hierachcy of information can help to guide new contributors into the project. However, it is important to reduce the amount of information stored as well. One good thing about the minimalistic approach of PowerPointLabs is that its instructions leave little room for set-up error because it is concise. Therefore balance must be found in the amount of information displayed.

One good example for future reference is the github page for [HTML5 Boilerplate](https://github.com/h5bp/html5-boilerplate), which concisely organises all essential information for easy reference.

###### Ideation

In Teammates, there is also the [Project Ideas Page](https://docs.google.com/document/d/1fAvYvQr0E93OsZgyneaXGX0jaMA-zptTIxqLn83xwN0/pub?embedded=true), which provides a structured way to discuss and store all ideas that can help to improve the project.

Currently, PowerPointLabs stores potential ideas in a private google doc. This doc is in a Google folder that is only accessible by the developers, hence it would be better if this doc can be made public, for new ideation from potential contributors, validation by existing developers and accountability/discussion/improvement of future ideas and features. Additional documents like “Common traps in PowerPoint Add-in Development”, and “Newcomer’s guide” would surely be useful for new contributors and can be considered for uploading on the PowerPointLabs github page for easier reference by incoming contributors.

##### Managing Contributions

In terms of Issues/PRs, their quality is enforced quite well. Issues are [documented](https://github.com/TEAMMATES/teammates/issues/8599) very well, with clear replicable steps listed and even screen shots posted so that any potential contributor can have clear information to work with. PRs are also checked at least twice by senior developers before requesting a review from the project mentor (Prof Damith). This layered check helps to ensure the quality of any PR that goes into the master branch. This is important because unlike PowerPointLabs which has a `dev-release` branch for dog-fooding, Teammates only has a main `master` branch, hence it is important to have many checks in place.

PowerPointLabs may be a smaller project comparatively, but it is good to learn from Teammates in how they structure their issues as well as review their PRs. With regards to whether PowerPointLabs would require the same amount of checks for each PR, I would say it's not compulsory for now because of the smaller project scale and better time efficiency, but I expect it to adopt the same quality of checks once it starts to scale up in the future.

## TAN LI HAO
**Project**:

**Observations**:

{write your observations here}


## TRAN TIEN DAT
**Project**: [Mitmproxy](https://github.com/mitmproxy/mitmproxy/)

**Observations**:

Mitmproxy is a Python-based set of tools to to intercept and manipulate HTTP/HTTPS traffic, used primarily for security testing and research. The contributing process is quite standard. I just had to make a comment in the issue to let people know that I was working on the issue. Once I had completed a fix, I would open a PR and wait for the mainainer's review. The project uses unit testing and code coverage tool tox for quality assurance. New PRs are built and tested on Travis and Appveyor for continuous integration.

One thing I noticed is that the [instructions for contributing](https://github.com/mitmproxy/mitmproxy/) is really short and simple. Contributors just need to run a script and all the necessary dependencies will be installed. Together with a few paragraphs about how to build the project, how to run the tests, and a link to the documentation, the development setup guide does not mention anything about any advanced configurations like IDEs, even though the core developers are using PyCharm. I think this short guide is very attractive to contributors, as it goes straight to the point and gives the feeling that contributing to the project is not hard. Comparing this with the internal project, TEAMMATES, I think the [TEAMMATES Contributing Guide](https://github.com/TEAMMATES/teammates/blob/master/docs/CONTRIBUTING.md) can definitely be improved. The development environment setup guide requires a few clicks away from the main page, and along the way contributors had to go through unrelevant things like project visions, project features. I think these documents can be more concise and better organised.

While I support having a short and simple setting up guide by having scripts to automate the process, sufficient details should still be given about what the script is doing. I had some problems while trying to set up the development environment for Mitmproxy because I was using Windows (surprise!). In the end I managed to solve the problem by reading the set up scripts, figuring out what it is doing, and doing the equivalent thing in my specific configurations. This teaches me that codes are not just to tell the computer to do something, but also for others to understand and fix when things go wrong. Hence, codes should always be accompanied by sufficient explanations.

Another thing that I learnt from contributing to the project is that it is important for maintainers to document how issues are related to each other. For my first PR, I found an issue which nobody was working on, so I opened a PR to fix it. Only then did I discover that the issue was related to another issue that someone else was working on. Thus my first attempt at fixing the issue had conflicts with the proposed solution of the other issue. To avoid further conflicts, I waited for the other issue to be resolved and merged before resuming working on mine. The problem could have been avoided if the maintainers were aware of how similar the issues were and referenced one from the other in the issue tracker. In this regards, I think TEAMMATES is doing a good job in triaging issues and documenting the relevant information in the issue threads.

Lastly, I would like to suggest some practices of Mitmproxy that our internal project should adopt. They have a folder in the project for documentations and have automatic tools to generate a [static website](https://docs.mitmproxy.org) for the documentation. I think we can use Github Pages for this purpose. Having a centralized place to look for documentations, with navigation links to quickly find what I want to read is very helpful in developing.


## VIVEK LAKSHMANAN
### Project: NLTK
* [Contribution Guidelines](https://github.com/nltk/nltk/blob/develop/CONTRIBUTING.md)

I chose NLTK as my external project as I was learning about NLP (Natural Language Processing) in my Introduction to Information Retrieval Module and I wanted to dig in deeper. At the same time, I wanted to improve the quality of my python code. Though the time spent with NLTK was short, I was able to learn much about their workflow and practices that will be of use to SE-EDU.

#### Observations
* **Copy-and-paste style for Git Workflow**<br>
In the `GitHub Pull requests` section of the contribution guidelines, rather than being comprehensive, the **instructions given were simple and to the point**. Furthermore, every point was accompanied by a `git` command used to carry out the instruction. This allowed for new contributors to **understand and get started with the workflow very quickly**.

* **Separate branch for development**<br>
The main branch that is meant for release is separated from the branch that is constantly updated. This separation from the main branch allowed for **easier management of bad/breaking commits before releases**. When an issue arises, such as breaking of code due to updating of software/libraries, it becomes easier to revert changes and apply patches, allowing for the `git` tree of the main branch to **remain clean and free of bad commits**.

#### Takeaways
* **No contribution is too small**<br>
Every pull request, no matter how small the contribution, is acknowledged and is given recognition if done well. For instance, for my pull request, even though it was rather small, by taking an effort to analyse the problem and providing a comprehensive explanation on what I did, the pull request was acknowleged with an `awesome-contribution` tag that pushed me to contribute more.

* **Being inactive on reviewing PRs can be detrimental**<br>
On many cases, the project maintainers can be rather inactive for long periods of time which can hinder the progress of the pull request. Quite often, doubts don't get answered or pull requests get closed with a lack of explanation, which is rather counterproductive given how much effort was put in to acknowledge small contributions.

#### Practices to adopt for SE-EDU
* **Have a simpler contribution guideline for new contributors**<br>
From a first-hand experience, the contribution guidelines for SE-EDU takes a few hours to read, process and apply. Though it may be comprehensive and beneficial in the long term for imparting software engineering principles, it can be rather **daunting for new contributors**. For instance, first-timers find it hard to read through the workflow document from the `oss-generic` repository as it contains large paragraphs of explanation and links pointing to different tutorials/documents. Furthermore, the guidelines are nor easily found in the repository itself, making it difficult for first-timers to get started. **Therefore, a separate `CONTRIBUTING.md` file, written in a simple and straightforward manner like in NLTK**, for SE-EDU can help new contributors ease into the workflow and get started quickly.

* **Create a develop branch**<br>
Although this type workflow is usually used for larger projects, having a development branch can prove useful in situations where there is an upgrade of the software tools that if merged ahead of time, could cause several implications. This is especially so in the case of Java which has a release every six months and some of the updates may not be backwards compatible. Other such upgrades would be Gradle that can cause implications when using certain libraries such as the `TestFX` library for which Gradle outputs warnings for after the upgrade.

### Project: OpacApp
* [Contribution Guidelines](https://github.com/opacapp/opacclient/wiki/How-to-build-the-project)

After facing difficulties with the inactivity in NLTK, I moved on to OpacApp, an android app for accessing scientific libraries. I chose this project as I wanted to get familiar with Android development and improve the quality of my Java code as well.

#### Observations
* **Offering moderate level issues to first-timers**<br>
Rather than offering simple issues such as bug or typo fixes, OpacApp **offers first-timers to attempt issues that are slightly harder**. This is done by providing a detailed description of the issue, how to get started on it and several guideposts to follow in order to fix the issue. With this, not only do first-timers gain more exposure, they also become **more familiar with the codebase, preparing them for future issues**.   


#### Takeaways
* **Documentation of code heavily affects development time**<br>
Unlike SE-EDU's extensive documentation of code, OpacApp has very little documentation of code. For instance, many functions and large blocks of code are not accompanied by comments. Though the app was developed with a priority on functioning code, documentation of code would help lower the learning curve for new developers. Even though it takes time to read the comprehensive documentation in SE-EDU, the time taken to understand what the code was trying to do was substantially shorter than that for the undocumented code in OpacApp.

#### Practices to adopt for SE-EDU

* **Offer moderate level issues to first-timers**<br>
In SE-EDU, first-timer issues are predominantly issues that require **simple code cleanup or bug fixes**. When first-timers move on to harder issues, the number of iterations taken to complete the issue increase substantially as they are not familiar with the codebase. As such, it would be better if slightly harder issues are labeled as first-timer issues along with a simple guide on how to complete the issue. With this, new contributors can **become familiar with the codebase and workflow earlier**.


## WEN XIN
**Project**:

**Observations**:

{write your observations here}


## YONG ZHI YUAN
**Project**: Exercism (Link to external project workflow: https://github.com/exercism/java/blob/master/CONTRIBUTING.md)

**Observations**:

I improved in my **resourcefulness** skills as I had to find out more about the project, understand the code base and look up on the processes on my own, instead of relying on senior developers as I did for the internal project. This is because it's more efficient to find out things on my own for the external project, since it is likely that my reviewers are living in a different time zone. As such, it may take me up to half a day before I receive a response; I respond in the day, and the other person responds at midnight or so. Whereas when I'm working on the internal project, the response is quicker, and we are able to converse & discuss multiple times throughout the day.

Working on the external project reminds me on the importance on having **proper documentation** in the Developer Guide. When I was choosing between the different external projects to contribute to, I first short-listed the projects based on those with better documentation, as it was easier for me to understand existing code and therefore allowing me to be able to better contribute to the project. For larger repositories, more effort must be made to write a good Developer Guide and to structure it well. The external project that I worked on had multiple repositories with lots of documentation, however it isn't structured well. As such, despite spending some time reading up the documentation, there were still portions that I missed out.

For example, in the AddressBook Level 4 Developer Guide, we can explicitly state something like, "For general information about how to contribute to AddressBook Level 4, please refer to the OSS-Generic Process", which will then bring them to the "process" repository. This isn’t done so at the moment.

Also, I noticed the need to have easy issues in the repository for newcomers, yet the issues should not be too easy either. For example, as I have already been working on OSS for a period of time, I am not too keen on working on simple first-timer issues such as fixing typos etc; it isn't exciting. Similarly, some of the potential contributors may have prior experience already and may feel the same way.

I noticed that the difference in difficulty between the 1st PR (which is a first timer issue) and the 2nd PR onwards that my CS3282 teammates have done, is quite steep. Linking to the previous point, it seems good to find **moderate sized issues** for potential contributors to work on. There are some in the code base, however we did not tag them according to the difficulty level (we do not such tags too), and as such it requires a bit of effort to source out which issues are moderate in difficulty.

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
**Project**:

**Observations**:

{write your observations here}


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

**Observations**:

{write your observations here}


## PHANG CHUN RONG
**Project**:

**Observations**:

{write your observations here}


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
**Project**:

**Observations**:

{write your observations here}


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
**Project**:

**Observations**:

{write your observations here}


## VIVEK LAKSHMANAN
**Project**:

**Observations**:

{write your observations here}


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

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
**Projects**: [Servo](https://github.com/servo/servo) & [Open-Keychain](https://github.com/open-keychain/open-keychain)

**My contributions**:
- [servo](https://github.com/servo/servo/pull/20012)
- [open-keychain](https://github.com/open-keychain/open-keychain/issues?utf8=%E2%9C%93&q=++author%3AAlexFJW+is%3Aclosed)

**Observations**:
Servo is an open source browser by Mozilla, written in Rust. I've contributed a PR here in the past few weeks for this module. open-keychain is an open source Android application for PGP key usage. I'm no longer active at open-keychain, but have completed the Google Summer of Code program with them.

Servo:
- [Web documentation](https://doc.servo.org/servo/index.html) for the entire project  
Extensive documentation is not required. Not all functions had accompanying comments.   
Even so, the search preview it made development easier as searching the web documentation is faster than doing a `grep` call in the command line or using IDE tools. (try making a search in the link for a better idea)  
This is particularly valuable for PPTLabs, when official documentation for PPT APIs is severely lacking in ease of navigation and helpful descriptions.
Having our website for documentation allows us to also share the quirks of the broken PPT APIs.    

- Very active senior developers, open to discussion on many platforms  
Senior devs are always around to help, both on Github and IRC.
It might be beneficial to use a chat platform in NUS OSS as well, possibly through Gitter, Slack etc. While we already use slack within this module, extending this out to people outside of CS3281/2 may help bring new contributors, especially for GSOC participating projects like TEAMMATES.

- PRs and issue templates  
Servo, like Teammates & many other projects have PR & issue templates on Github. It reminds contributors to run tests and other relevant tasks before making issues, PRs. The templates help make issues and PRs clear and concise.  
Since PPTLabs currently lacks this, it might be good to work something out.

- Learning points regarding coding  
Do not amend your branch by force pushing even if the OSS requires your PRs to be squashed by the end of the PR. Senior devs need to know when you have made updates. Force pushing doesn't inform them of changes, resulting in delay.

Open-Keychain:  
- Same as Servo w.r.t. active senior devs

- Learning points from merging large PRS
  - Get large PRs reviewed early at many checkpoints and make them as modular as possible. (anything > 300 loc should require this)
  - Hold off refactoring until all tasks in the PR are complete and the code has obtained approval from senior devs. This reduces the amount of new code your reviewer has to read, making the review process easier.

## CARA LEONG SU-YI
**Project**: [NLTK](http://github.com/nltk/nltk)
- [Contributor's guide](https://github.com/nltk/nltk/blob/develop/CONTRIBUTING.md)
- [Developer's guide/wiki](https://github.com/nltk/nltk/wiki/Developers-Guide)
- [My contribution](https://github.com/nltk/nltk/pull/1957)

**Observations**:

I chose this project as I am interested in NLP, have used NLTK before, and am familiar with Python. I thought it would be useful to be familiar with the code base as it implements many NLP algorithms that are likely to be useful to me.

One thing that I learned as a programmer was how to use Python in a software development setting. I have used Python extensively for scripting and personal projects, but NLTK's large code base and long-standing development status threw me into the deep end as regards Python software development practices. Thus, for instance, working on this project exposed me to testing in Python, which I had not seen before. Although the tests seemed quite comprehensive, the way they were documented was not; I spent quite a while learning how to write tests before I was able to do so myself. In addition, learning how to navigate Python OOP was an interesting process; I learned a lot about how to write for a big, extendable codebase by working on this project.

What I found interesting after working with NLTK's codebase is that the code documentation is very elaborate. For example, it is not uncommon for packages and methods to have [docstrings that are several pages long](https://github.com/nltk/nltk/blob/develop/nltk/parse/viterbi.py), detailing formally what the algorithm is meant to do. This practice is very useful in the context of NLTK, which aggregates algorithms developed by researchers for other researchers' use -- knowing which algorithms are being implemented and how they are implemented is likely to be very useful.

Moreover, I appreciated the way NLTK is broken down into several independent sub-modules. The file organization was useful when I was learning the architecture of the project, and is as useful when using NLTK in production, and some modules also use [module docstrings](https://github.com/nltk/nltk/blob/develop/nltk/translate/stack_decoder.py) to share what the module does. Although I don't think this translates very well to TEAMMATES, since TEAMMATES is much more tightly-coupled than the separate NLTK modules, I thought the use of module-level documentation to share how each part of TEAMMATES adds to the whole may allow new developers to become more familiar with the codebase more quickly.

Although I felt developer documentation was good, the NLTK [user documentation](http://www.nltk.org/) is quite sparse, with few examples of use cases for the (quite extensive) code base. I found it quite startling that the user documentation usually provided one example usage of each method, didn't explain what packages did, and generally seemed to pitch NLTK as a black box. Perhaps the user base of NLTK is expected to be familiar enough with Python to check the source code for implementation and for additional information. On the whole, however, I think that better documentation could help new users to learn how to to use NLTK much faster. With a big project that is quite dispersed in use (e.g. you can use one module and never touch another), it can be difficult to become familiar with the whole platform. Moreover, as many methods are 'undocumented' in the user guide, users may have to read through the source code to find out how some aspects of the module are implemented, which may be a turn off.

In addition, the 'undocumented' nature of much of the codebase may be related to the fact that a PR that I worked on for NLTK was merged even though I had not yet written documentation for the code, or added tests. One thing that I will take away from this experience and hopefully apply to TEAMMATES is the importance of communicating with contributors and ensuring that their code is up to standard before merging it. This involves not just checking code quality, but also ensuring that their code is well-documented and tested too.

**Project: [Atom Flight Manual](https://github.com/atom/flight-manual.atom.io/)**
- [Contributor’s guide](https://github.com/atom/flight-manual.atom.io/blob/master/CONTRIBUTING.md)
- [My contribution](https://github.com/atom/flight-manual.atom.io/pull/453)

**Observations**:

The process of contributing to the Atom Flight Manual was relatively painless as I could refer to the [Contributor’s guide](https://github.com/atom/flight-manual.atom.io/blob/master/CONTRIBUTING.md), which provided useful shortcuts and handles on the idiosyncrasies of the project (e.g. OS-specific instructions, how to use alerts and notifications in their style). Although the community is quite small and quiet, the documentation and referring to previous work allowed me to feel comfortable enough to submit a PR quite quickly.

After contributing to the project, I learned that it's very important to keep track of your project's dependencies. Atom's Flight Manual uses [HTML-Proofer](https://github.com/gjtorikian/html-proofer) to ensure that images, links and scripts are working. HTML-proofing is integrated in the CI process, so broken references will always need to be fixed before the build passes. This is a vital step to ensure that documentation is kept up to date because the open-source Flight Manual is separate from the [official documentation](http://atom.io/docs) -- although the flight manual is dependent on references to the official documentation, the official documentation is liable to change. Thus, when I contributed to the Flight Manual, my build failed as a link in a different section had been broken by the latest update to the official documentation. Without a check in place, broken links such as these might not be found until someone looking at the documentation for help tries to click the link.

While TEAMMATES is not heavily dependent on external sites, we do have quite a few cross-site links. Thus, it is important to keep in mind, even if we do not integrate this tool, the need to check that we do not cause regressions by changing static items. This would ideally involve including our static pages in tests as well, but can in the meantime involve simply ensuring that we search through the codebase thoroughly.

In addition, the tools used to build flight manual itself may be useful for any documentation-heavy project. I was quite impressed by the way the Flight Manual integrated OS-specific documentation in particular, but in general I felt that the additional functionality that a Markdown-generated site could give was quite impressive.

## CHUA YUN ZHI NICHOLAS

**My contributions**: [eslint#9876](https://github.com/eslint/eslint/pull/9876), [addressbook-level4#836](https://github.com/se-edu/addressbook-level4/pull/836)

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

**My contributions**: [strongbox#522](https://github.com/strongbox/strongbox/pull/522), [strongbox-web-integration-tests#24](https://github.com/strongbox/strongbox-web-integration-tests/pull/24), [strongbox-web-integration-tests#20](https://github.com/strongbox/strongbox-web-integration-tests/pull/20)

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
**Project**: [github/hub](https://github.com/github/hub)

**My Contributions:** [#1667](https://github.com/github/hub/pull/1667), [#1690](https://github.com/github/hub/pull/1690)

<!-- Links to any online documents about the workflow of external project -->
- [`CONTRIBUTING.md`](https://github.com/github/hub/blob/master/CONTRIBUTING.md)

**Observations**:
`hub` is a command-line tool that acts as a wrapper around `git` and integrates GitHub-related functionality into your local terminal. `hub` is implemented in the Go language, one of my expert areas. I decided to work on `hub` as I wanted to gain experience working on a large project in Go, which I had only used before in small, isolated problems for practice.

<!-- Important things you learned from contributing to that project, if any -->
The principle of least surprise is very important when making changes to an interface. Some feature requests require a change in default behavior. For example, [one of my PRs for `hub`](https://github.com/github/hub/pull/1690) was to fulfill a feature request that required a change in `hub`'s default behavior. One of the primary concerns of the maintainer is how much it would surprise current users of `hub` when they update it, and whether we could make this change in behavior such that people could opt-in to the old behavior. This is important as they might already have scripts that expect the old, default behavior which may be broken by us by pushing this change into a release of `hub`.

Open-source development is also _slow_. There is only one maintainer for `hub`, so he is the sole gatekeeper of the project and decides which features are in line with his vision of `hub` as well as the only person really doing code review for pull requests. Coupled with the large number of people who try to work on `hub`, this can cause a bottleneck, causing some pull requests to not be reviewed at all and go stale. I have gotten around this problem by focusing on issues that on slated for the next release (that no one wants to work on, strangely) in order to get priority for my pull requests. This is based off the project tracker in GitHub. This also helps the maintainer, as it gets the most important fixes/features implemented in first, instead of simply pulling a random issue from the issue tracker and working on that.

<!-- Practices/tools of the external project that you think can be adopted by your NUS-OSS project -->
`hub`'s approach to system's testing relies on [`cucumber`](https://github.com/cucumber/cucumber) which I found quite interesting.
For example, this block tests the `hub clone` command, which does the same thing as `git clone` but allows you to input a GitHub reference, like `hub clone TEAMMATES/teammates` will clone `TEAMMATES/teammates`

```
Feature: hub clone
  Background:
    Given I am "mislav" on github.com with OAuth token "OTOKEN"

  Scenario: Clone a public repo
    Given the GitHub API server:
      """
      get('/repos/rtomayko/ronn') {
        json :private => false,
             :name => 'ronn', :owner => { :login => 'rtomayko' },
             :permissions => { :push => false }
      }
      """
    When I successfully run `hub clone rtomayko/ronn`
    Then it should clone "https://github.com/rtomayko/ronn.git"
    And there should be no output
```

Each step corresponds to a definition. For example, the `Then` steps corresponds to this:
```
Then(/^it should clone "([^"]*)"$/) do |repo|
  step %("git clone #{repo}" should be run)
end

Then(/^there should be no output$/) do
  assert_exact_output('', all_output)
end
```
(I have omitted the definition of the other steps for brevity, but they are similar)

The tests are written in plain English in a step-by-step manner, and the test acts as both the desired behavior specification, documentation and automated test (kill three birds with one stone!). Even without working on this project, you can figure out what this test is for immediately. This test is specifically end-to-end.

In teammates, we could potentially utilize `cucumber` (there is a version for Java) for mid-level integration tests like [`FeedbackQuestionsLogicTest`](https://github.com/TEAMMATES/teammates/blob/master/src/test/java/teammates/test/cases/logic/FeedbackQuestionsLogicTest.java) and make the tests more readable and self-documenting. We can go one step further and try to use it for end-to-end UI testing, but may be difficult to do. All in all, a testing framework like `cucumber` may be worth exploring.

<!-- [Optional] Suggested areas of improvement for the external project -->
An area of improvement for the external project is to have more mid-level maintainers who can also perform code review in order to ease the development process. Having one man do maintain the project causes a massive slowdown and stretches him thin. A hierarchy like Teammates' can be used, where committers perform the initial reviews, before requesting a final review from the maintainers who decide whether to merge a pull request.


## JOANNE ONG CUI FANG
**Project**: [OpenRefine](https://github.com/OpenRefine/OpenRefine)
- [Documentation for Developers](https://github.com/OpenRefine/OpenRefine/wiki/Documentation-For-Developers)
- [Contributing Guide](https://github.com/OpenRefine/OpenRefine/blob/master/CONTRIBUTING.md)
- [Governance Model](https://github.com/OpenRefine/OpenRefine/blob/master/GOVERNANCE.md)

**My Contributions**:
- [#1454](https://github.com/OpenRefine/OpenRefine/pull/1454)
- [#1481](https://github.com/OpenRefine/OpenRefine/pull/1481)
- [#1480](https://github.com/OpenRefine/OpenRefine/pull/1480)
- [#1539](https://github.com/OpenRefine/OpenRefine/pull/1539)

**Observations**:

OpenRefine is a desktop application for data cleanup and transformation to other formats. It is written primarily in Java, and relies mainly on HTML, JavaScript and CSS to present a user interface for the application. I chose this project because the [technology stack used by OpenRefine]( https://github.com/OpenRefine/OpenRefine/wiki/Technology-Stack) aligns with my learning areas, and also because OpenRefine seems to be [picking up more steam lately with regards to development progress]( https://github.com/OpenRefine/OpenRefine/graphs/contributors).

##### Key-takeaways

As the second open source project (the first being TEAMMATES) that I have contributed to, working with OpenRefine has taught me more lessons about working with and managing such software projects.

The very first lesson I learnt from OpenRefine was **the importance of welcoming new contributors**. As trivial as this may sound, it actually played a part in driving me to choose OpenRefine as my external project to contribute to. [By acknowledging my desire to contribute to OpenRefine]( https://groups.google.com/forum/#!topic/openrefine-dev/Qyou-n2Jxcw), I received the favourable impression that the project's community is warm and engaged and that the project is active and worth contributing to. Given that open source projects such as OpenRefine survive and thrive on the voluntary work of other developers, it is imperative for open source projects to reach out actively to interested contributors to draw them into the project.

Another key lesson that OpenRefine imparted me was to reiterate **the need for a core team of developers to drive and sustain the project**. Even as open source projects depend on an inconsistent pool of voluntary contributors to grow the project, ultimately, there has to be a select group that guides and leads the community. This is a characteristic that is apparent in both OpenRefine and TEAMMATES. For instance, both OpenRefine and TEAMMATES require pull requests to be reviewed and approved by recognised team members before they can be merged into the project. In fact, the significance of a core team is made even more obvious when I contrast OpenRefine with TEAMMATES. Although OpenRefine has always been open source in nature, it has an [interesting history](http://openrefine.org/2013/10/12/openrefine-history.html) that has influenced its current state. Simply put, OpenRefine has gone through three different identities (Freebase Gridworks, GoogleRefine, and OpenRefine) under three corresponding groups of developers (Metaweb Technologies, Google, and the open source community) in the past 8 years since its birth in 2010. Meanwhile, TEAMMATES has been [growing rather comfortably under the National University of Singapore (NUS)](http://teammatesv4.appspot.com/about.jsp) for the same duration. With OpenRefine's core team changing far more drastically than TEAMMATES, I find that OpenRefine is still struggling to define a clear direction and structure today while TEAMMATES has a better idea of [what it is heading towards](https://github.com/TEAMMATES/teammates/blob/master/docs/overview.md), and how to proceed in that direction.

Besides my own project takeaways, I find that there are also some aspects which TEAMMATES can learn from OpenRefine and vice versa.

##### Suggestions for TEAMMATES

###### Documentation

**TEAMMATES' documentation can be restructured (or even migrated) for better navigation.** Granted, TEAMMATES' documentation is rather comprehensive with the full set of Developer Guide, User Guide, Code of Conduct etc. Yet, as a new contributor, I found it difficult to find the subsection/information that I am interested in. This is because TEAMMATES merely [collated the document titles with single-line descriptions](https://github.com/TEAMMATES/teammates/tree/master/docs), which proved to be immensely unhelpful in navigating the documentation.

On the other hand, OpenRefine hosts its documentation for developers in a [GitHub wiki](https://github.com/OpenRefine/OpenRefine/wiki/Documentation-For-Developers). Not only does this look cleaner, it also improves navigation as readers can easily see all the relevant subsections at a glance and quickly proceed to a particular subsection. TEAMMATES might thus want to provide a better summary of the available documentation/ migrate documentation over to GitHub wiki to boost the usefulness of the current documentation.

###### Developer and user interactions

**TEAMMATES can increase developer and user interactions to help users and feedback to developers.** Currently, TEAMMATES allows users to submit feedback via (i) a feedback form within TEAMMATES or (ii) emailing the TEAMMATES support email. These feedback can be inclusive of compliments, help requests, or suggestions for certain new features that are unsupported by TEAMMATES at the moment. Whichever it is, most developers do not have access to these feedback and hence miss out on the compliments, help requests, or suggestions from the users, and must wait for news to travel down from the top of the developer hierarchy.

Whereas OpenRefine allows users to submit feedback via (i) [a public user discussion list](https://groups.google.com/forum/?fromgroups#!forum/openrefine) or (ii) [the GitHub issue tracker](https://github.com/OpenRefine/OpenRefine/issues). This exposes all user feedback to other users and developers, allowing other users and developers to partake in conversations regarding the issue at hand. This can also help to spread the work of responding to users more evenly among the developers helping with the project.

Furthermore, users can also be kept updated on developers' progress if changes for each release are properly documented and publicly available. For example, OpenRefine publishes [regular newsletters](http://openrefine.org/2016/03/21/OpenRefine-20News-253A-20Spring-202016.html) for users to remain aware of how the product has changed. TEAMMATES can adopt a similar practice to better involve users in the development process.

##### Suggestions for OpenRefine

###### Testing

**OpenRefine can focus more on improving tests for its functionalities.** Although OpenRefine is known as a mature data-wrangling tool, its coverage is at an abysmal rate of 40%. By choosing to prioritise implementing functionalities over writing tests, OpenRefine runs the risk of unwittingly introducing bugs into a release, or developing features that do not behave entirely as per expected.

Meanwhile, TEAMMATES has a very healthy emphasis on tests, with tests for both backend logic and frontend user interface. In particular, OpenRefine can look into adopting some automated testing tools utilised by TEAMMATES, such as Selenium for testing the graphical user interface since OpenRefine and TEAMMATES have similar technology stacks.


## KOH LEWIS
**Project**: [NUSMods R](https://github.com/nusmodifications/nusmods/tree/master/www)
[Contribution Guidelines](https://github.com/nusmodifications/nusmods/blob/master/CONTRIBUTING.md)
[Developer's Guide](https://github.com/nusmodifications/nusmods/tree/master/www)

**Observations**:

NUSMods R is a website which allows students of NUS to plan their timetable effectively. It is built on React, Redux, and Bootstrap, and aims to be fast, modern, and responsive.

I chose NUSMods R because I was interested in working on a project which I and many others use daily and is an important part of my life right now. Hopefully, I would have been able to make the website a better experience for everyone using it, myself included.

Getting started was simple, especially with the immensely handy [Beginner’s Guide](https://medium.com/@zameschua/getting-my-feet-wet-my-experience-with-open-source-and-nusmods-f1381450517e) written by one of the contributors. NUSMods uses Yarn for dependency installation, so it is very easy to set up and start working on issues.

Choosing a first issue to work on is similar to SE-EDU. Similar to the ‘d.FirstTimers’ label, NUSMods has the ‘good first issue’ label. However, the issues are not as easily solved. Many of the issues are bugs which take time to track down and fix. Others are open-ended and vague, and even more are multiple features packed into one issue. Unlike the ‘d.FirstTimers’ issues in SE-EDU where the creator basically tells you what needs to be done, a decent amount of research and coding needs to be put in to even resolve a ‘good first issue’.

 Working on the PR was also similar to SE-EDU. After creating a PR, reviews were fast and helpful to refine the PR. The commit message is less strict than the one for SE-EDU, making my life a lot easier! One thing I do appreciate about SE-EDU over NUSMods though is that the CI testing is very efficient. NUSMods also has its own testing, however before they accepted my PR, they had to manually test the changes on their own. This took a few days, and it was a bit jarring having to wait compared to the amount of waiting for comments when they were reviewing the PR.

Not having to write paragraphs of justification for a commit message made my PR easier to make.  Granted, it does make it harder for the reviewers to understand what is going on, but that can be fixed by comments in the code. It might only be possible in smaller projects, where the bulk of the changes are made by a select few people who already know the inner workings of how the project works. I do see the advantage of writing good commit messages, however given the additional work required in creating and fixing the messages, I am not sure if it is worth the extra effort. Especially since it may scare away newcomers who want to contribute to the project.

In terms of documentation, NUSMods pales in comparison with SE-EDU. The PR I worked on was largely confined to one file, which had good documentation in it and was easy to work with. However, when I tried working on another issue, the labyrinth of files and code was hard to untangle, making it tough to figure out where is a good starting point. Compared to SE-EDU with its great Developer Guide, NUSMods really only gives an overview of how to set up the project environment, without giving much insight into how everything is connected.

However, due to the great people at NUSMods, it is easy to find what you need just by asking. In addition to Github, they can be reached through [Telegram]( https://telegram.me/nusmods), [Messenger]( https://www.m.me/nusmods), [Facebook]( https://www.facebook.com/nusmods), [Twitter]( https://twitter.com/nusmods), and even [email]( nusmods@googlegroups.com). The ability to contact them through so many channels makes the project seem friendly and inviting. Although this may just be a façade, as they may not be active on some of these platforms (Their last twitter post was over 2 years ago!)

**Conclusion**
Overall, contributing to NUSMods felt very similar to contributing to SE-EDU with some key differences. It does not feel as stringent with its commit messages and code, which encourages newcomers to try to contribute. However, this is deterred by the additional difficulty of the issues compared to SE-EDU, in terms of scope of the issues as well as the documentation available. Continuous Integration is very important. It saves time for the reviewer, so that they do not need to manually test the build, and it saves time for the contributor, so that they know quickly whether they need to fix their PR. Lastly, having many avenues of communication gave off a very welcoming atmosphere.


## LEE YAN HWA
**Project**:
FOSSASIA's Open Event Android and Open Event Organizer App

**Observations**:
The two external projects I have chosen are related to each other. These are just two projects using the Open Event API, there are others. The Open Event Android Project has two components: a App Generator which is a web application that will generate an event Android app and a generic Android app for events which is the output of the generator. This generic Android app is targeted at the attendees of the event. Meanwhile, the Open Event Organizer App is an Android Event management app for event organizers using the same Open Event Platform.

**PRs to External Projects**:

##### Open Event Android
- [Fix: Speaker's color changes when searching #2351](https://github.com/fossasia/open-event-android/pull/2351)
- [feat : Viewmodel for DayScheduleFragment #2328](https://github.com/fossasia/open-event-android/pull/2328)

##### Open Event Orga App
- [test: Add tests to Create Event Module](https://github.com/fossasia/open-event-orga-app/pull/835)
- [fix: Create Event Activity will finish after event is created](https://github.com/fossasia/open-event-orga-app/pull/688)


#### Open Event Android
###### For new contributors
They always welcome new contributors. Their [README.md](https://github.com/fossasia/open-event-android) is very clear about what the project is about and is full of helpful screenshots for newcomers. They have [very detailed instructions](https://github.com/fossasia/open-event-android/blob/development/docs/android-app-setup.md) on how to set up the project and also [how the app is generated](https://github.com/fossasia/open-event-android/blob/development/docs/apk-generator.md). They also provide details of the exact technology stack that the project uses. They have [code style guidelines](https://github.com/fossasia/open-event-android/blob/development/docs/codestyle.md) and [commit style guidelines](https://github.com/fossasia/open-event-android/blob/development/docs/commitstyle.md).

###### Ideation and Discussion
Open Event Android uses [Gitter](https://github.com/fossasia/open-event-android) for ideation and discussion. Alternatively, anyone is welcome to open an new issue on GitHub to discuss an idea and other developers will join in to discuss if the idea / feature is feasible and necessary. If a suggested feature is not urgent and should be done later, it will be marked with a **later** tag. Some smaller issues / ideas are also marked as **low-priority** and these are also often good for new contributors. There is a **CODE_OF_CONDUCT.md** to 'foster an open and welcoming environment'.

##### Issues, PRs, Merging
Open Event Android has three branches, development, master and apk. The apk branch contains two apks which are automatically generated on a merged pull request from the dev branch and the master branch. The development and master branches are similar to those in PowerPointLabs.

Open Event Android uses an issue template and PR template that we are in the process of creating for PowerPointLabs too. For PRs, the name of the PR has to start with chore, feat, fix, test or bug to make clear the type of issue the PR is resolving.

Once a PR is made for the issue, the [open-event-bot](https://github.com/apps/open-event-bot) will automatically add the **has-PR** tag to the issue. The open-event-bot will automatically assign the creator of the PR to the PR and add a **needs-review** tag. The bot will also automatically comment if the build fails on Travis CI and provides a link to the failed build. Then, Codacy will automatically check whether the PR is of good quality or not.

After a review by a senior developer, the developer will usually request for changes. If the changes needed are very drastic, the PR will be tagged with **needs inspection**. Once a PR is merged, it will be tagged with **ready-to-ship**. If it is closed before merging, it will be tagged with **invalid**.

Sometimes, there will be a very massive feature involving different components that needs to be implemented, thus a **parent-issue** will be created and it will reference the **child-issue** issues that are created for each component.

The developers are very active and will nudge me to ask the progress of a PR / an issue if I have not responded for more than 5 days. Thus I will also quickly finish up my PR within a week, if not I will let another person take the issue instead. The developers are very encouraging and for my first merged PR, the senior developer even commented that I did a very good job.

##### Suggestions for Open Event Android
Open Event Android and Open Event Organizer App only has mainly one active senior developer which goes through all the issues and PRs, thus I think they should try to promote more of the active developers to a senior developers as soon as possible so that the workload is reduced for that one senior developer.

At first, as a new contributor, I was also unclear of the direction that the project was going because the senior developer wanted to focus on implementing new features and changing the project architecture. I did not know where to start, until I introduced myself in one of the old issues (that was abandoned) and one of the developers directed me to an more urgent ViewModel issue. However, I appreciate their very quick responses and they are very happy to tell me which issues are more urgent to fix. Soon enough, the senior developer created an issue [Road map of features of the project #2266](https://github.com/fossasia/open-event-android/issues/2266) which made the direction of the project clearer for everyone.

I then realised that for old issues that do not have an active PR, even if they are already assigned to a person, we can actually ask if the assigned person is still working on the issue (Often, they are not, if the issue is already inactive for 2 weeks or more.) and offer to take up the issue instead. The developers are friendly and will often step in to tell you if you should take up this issue or not. This might not be clear to newcomers as this is not really mentioned on their Gitter.

They should have more issues tagged as **easy** or **good first issue** as currently there are none.
Open Event Android needs to have more **tests**, while Open Event Organizer app has many unit tests but not enough integration tests. PowerPointLabs has more tests than Open Event Android, and this is likely due to the latter project being very young. Focus is placed on implementing features rather than testing.

#### Open Event Organizer App
Open Event Organizer App is very similar to Open Event Android. The only major difference is that it has a Codecov bot that will comment about the change in testing coverage of the code.
Recently, the senior developer has been closing many old issues and tagging them with **waiting-for-status**, urging us to quicken the issue-PR-merge cycles and to make the issue tracker neater.

#### Suggestions for PowerPointLabs
We need to have more screenshots and documentation for newcomers on Github if we are going to open the project to new contributors. Many instructions and special tricks and tips are hidden in our private Google Drive folder instead. We also lack documentation about parts of our technology stack such as the ClickOnce installation process.

Currently, our discussions are on Slack but if we are going to open the project to new contributors, it could also be useful to use Gitter instead as Gitter has greater integration with Github. PowerPointLabs has many outstanding issues. We could also tag our issues with the **later** tag if these issues should be done later instead. We could also tag them with **high-priority** or **low-priority**, or even close some of the issues to make our issue tracker neater.

Additionally, it could also be good to have an automated bot like the open-event-bot. Having the **has-PR** tag is good as we will know which issues are currently being worked on. We could also have more **parent-issue** issues and a **road-map** issue to set the direction of the project. I think it will also be good to add whether a PR is a chore, feat, fix, test or bug in the PR title.

If we were to open the project to external contributors, I hope our developers will be as friendly and helpful as those from the Open Event projects. The senior developer even asked me on Gitter if I was going to submit my GSoC proposal.

## LU LECHUAN
**Project**: Exercism

**PRs to External Project**<br/>
[Implement new exercise: Zipper #1327](https://github.com/exercism/java/pull/1327)<br />
[Update ScrabbleScoreTest #1311](https://github.com/exercism/java/pull/1311)<br />
[Update RomanNumberalsTest #1309](https://github.com/exercism/java/pull/1309)<br />
[Update PrimeFactorsCalculatorTest #1308](https://github.com/exercism/java/pull/1308)<br />
[isbn-verifier: update tests and version file #1302](https://github.com/exercism/java/pull/1302)<br />
[Update AtbashTest #1307](https://github.com/exercism/java/pull/1307)<br />
[Update PigLatinTranslatorTest #1305](https://github.com/exercism/java/pull/1305/files)<br />

**Observations**: [Exercism](http://exercism.io/) is a portal to learn new programming languages, it has over 30 different languages and many problem sets of increasing difficulties for users to engage in progressive learning.
[Link to exercism github](https://github.com/exercism).

This project appears interesting to me as it contains many exercises that are inplemented in different languages. One can practice a particular languages effectively as there are increasing difficulties. It also always users to have cross references from several languages as some of the exercises are the same from those languages.

I have worked in the Java branch - the exercises that are implemented in Java. I started with implemented tests for certain excersises, then moves on to implement a new exercise. I have observed that the project has practiced some of the testing principles such as Equivalence Partition and Boundary Value Analysis to ensure both effectiveness and efficiency for the testing. The project has a folder which stores the "canonical test data" and the actual test cases are expected to match these "canonical test data" so that the principles are followed closely.

For my first PR, I have grouped some of the tests together based on the types of test data. The senior developers very kindly explained to me that I should seperate them individually. This is because the project is promoting TDD (Test Driven Development), it will be easier to keep track of the progress if tests are as granular as possible.

**Comparison with Teammates**:
The developer guide for Teammates is definitely better. Adequate diagrams are provided to allow contributes to understand quickly the architectural design of the project, how components are related, etc. Exercism on the other hand, does not provide diagrams as a complement for documents. However, different components of Exercism are quite well-organised. Documentations for exercises are provided both integratedly and separately - developers can check the document for a particular exercise in that exercise sub-folder, or in the main document.

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

**My contributions:**
- [#1316](https://github.com/exercism/java/pull/1316)
- [#1386](https://github.com/exercism/java/pull/1386)
- [#1292](https://github.com/exercism/java/pull/1292)


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

**Contributions**:
- [Coala: Coala-bears: Improve Docstring](https://github.com/coala/coala-bears/pull/2279)
- [Coala: Corobo: Add help message](https://github.com/coala/corobo/pull/504/files)

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
**Project**: [ESLint](https://github.com/eslint/eslint)
- [Contributing](https://eslint.org/docs/developer-guide/contributing/). This explains how to report bug, propose  new rule or rule change and submit a PR.
- [Setting up development Environment](https://eslint.org/docs/developer-guide/development-environment)
- [Maintainer Guide](https://eslint.org/docs/maintainer-guide). This explains how to manage issues, review PRs and manage releases.

**Contributions**:
- [Docs: Add modified variable examples for no-loop-func (fixes #9527)](https://github.com/eslint/eslint/pull/10098)
- [Fix: Make max-len ignoreStrings ignore JSXText (fixes #9954)](https://github.com/eslint/eslint/pull/9985)
- [Fix: valid-jsdoc does not know async function returns (fixes #9881)](https://github.com/eslint/eslint/pull/10161)

**Observations**:

I learnt the importance and effectiveness of good documentation. ESLint provides extensive and useful documentation for both users and developers on their website and throughout the code. This helped me to gain a sufficient understanding of their project, the codebase and the rationale being design choices and rules within a short time and make contributions. The instructions to set up the development environment, run tests and configure ESLint (as a user) were easy to follow. The rules also come with correct and incorrect examples. These documentation are likely to be valuable to other users and contributors as well as it aids understanding and can speed up their development process. I believe this is one of the reasons why ESLint attracted many external contributors and users. It also benefits the ESLint team as they will not need to answer questions or address issues already covered in their documentation.

Also, I learnt that effective and timely communication can speed up the development process and how such communication can be achieved. For ESLint, if contributors intend to work on an issue, they are advised to add a comment to that issue saying so and indicate when they will complete it (and if they no longer want to work on the issue). This avoids duplication of effort. Also, issues are labelled if they are blocked (require another change elsewhere), evaluating (not accepted) or breaking. This will help contributors to prioritize issues and identify what is available to work on. ESLint committers also respond to issues, questions and review PRs timely. The use of templates for bug reports, rule requests and pull requests further help to ensure that all relevant information and ideas were shared since the start. Together, such effective communication help to keep the development process go on efficiently.

**What MarkBind can adopt**:

1. Templates for bug report, feature requests/updates and PRs (can be auto-generated)
For bug report, ESLint requires the environment (which version), what did you do (actual source code causing the issue) and what the user expect to happen vs what actually happened (the actual, raw output). These are all useful information to Markbind as well.
Currently, Markbind does not have any structure that contributors are advised to follow. This makes it harder to determine if it is indeed a bug or intended behavior or caused by a difference in expectation of the user and the developer. It also makes it easier to reproduce the bug (especially since the bug only occur in specific scenarios e.g. when it is deeply nested) thus speeding up the development process. The version is important as Markbind is regularly updated.
For feature requests, the template should require the rationale for the request and clear examples of how the features will be used. If the requirements are specified and refined through discussion beforehand, there will be less confusion during implementation and we can get closer to the user-desired behavior which will make the feature more useful.
For pull requests, ESLint requires the type of the change, summary of what changes were made and what do you want the reviewers to focus on. I believe this is applicable to MarkBind as well. In addition, MarkBind's PR should include testing instructions as well. This can prevent some hiccups during Markbind's PR review progress. For example, sometimes the reviewers are unsure of what the changes were for and had to clarify them. Also, they might think that a feature is not working as tested - perhaps due to a difference in expectations and testing instructions. Furthermore, reviewers can also comment on the strengths/weaknesses of the changes (vs its alternatives) and introduce new testing suggestions for more robust testing.

2. Good documentation and hosting documentation on a website. ESLint host their well-written documentation on a separate website - this allows for better organization and support searching and navigation. We should improve the quality of Markbind documentation with more examples and host it on a website instead of a wiki (currently a WIP). This might make the documentation more easier to navigate though and for a user to find exactly what he wants.

3. Semantic commit messages. In ESLint, each commit must be prefixed by a tag (e.g Fix, Docs, New, Chore) which describes what the commit does, followed by a short summary. By enforcing these structure, contributors are less likely to include multiple changes in a single commit (e.g. a chore like code refactoring and a new feature). This is useful for Markbind as it can help reviewers identify what changed in a PR and future contributors to make sense of the code. Also, I believe Markbind can benefit from using commit message are a form of documentation as they will always stay with the code. Other contributors will only need to rely on `git log` or `git blame` to find out what changes are made (and why) instead of reading the pull requests and discussions on Github. Such neat commit messages can also be used in automatically creating a changelog which will let users and developers know what have changed from one version to another.


## SHRADHEYA THAKRE

I have contributed to two external projects:

### WikiMedia Commons App

**Project**: [WikiMedia Commons App](https://github.com/commons-app/apps-android-commons) <br>
[Project workflow](https://github.com/commons-app/apps-android-commons/wiki#contributor-documentation)

**My Contribution to WikiMedia Commons:**
- Revamped About Us page [#1080](https://github.com/commons-app/apps-android-commons/pull/1080)
- Fixed potential bug [#1148](https://github.com/commons-app/apps-android-commons/pull/1148)
- Improve Code Quality [#1149](https://github.com/commons-app/apps-android-commons/pull/1149)
- Give toast message when trying to upload image without giving a Title [#1211](https://github.com/commons-app/apps-android-commons/pull/1211)
- Add missing space between Licence and Coordinates in MediaDetailFragment [#1217](https://github.com/commons-app/apps-android-commons/pull/1217)
- Fix Toast Message for add_title_toast [#1254](https://github.com/commons-app/apps-android-commons/pull/1254)
- Wikimedia commons app added to "Who uses Fresco" on Fresco website [#2032 - fresco](https://github.com/facebook/fresco/pull/2032)

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


### Exercism.io - Java

**Project**: [Exercism.io - Java](https://github.com/exercism/java) <br>
[Project workflow](https://github.com/exercism/java/blob/master/CONTRIBUTING.md)

**My Contribution to Exercism.io - Java:**
- Version 2.1.0 added to food-chain [#1247](https://github.com/exercism/java/pull/1247)
- Modify Nucleotide Count tests and version [#1248](https://github.com/exercism/java/pull/1248)
- Updated Tests and Version number for Raindrops [#1317](https://github.com/exercism/java/pull/1317)

**Observations**

This project had a pretty satisfactory documentation considering that it was a small project. The project was mainly handled by 3-4 developers but they were very quick wit their review and merging duties. This helped contributors in doing stuff at a quick pace and wouldn't let them waiting for a review.
In fact, one of my PR's got merged the same night I had created a PR. Although this pace seems possible for them because most issue's are quite simple for well experienced contributors. Moreover, its possible to do most issues without even setting up the project, as it mainly required writing JUnit tests for their exercises.

There are very few tough issues but they haven't been created in the issue section and depend on contributors own interest whether they want to add a new exercise from different language.


**Comparison with TEAMMATES**

Both external projects that I had worked on didn't have a well defined contributing guidelines that were followed properly. It is surprising as one of them is a GSOC organization.

The TEAMMATES organization has a proper orientation guide for contributors which provides all details, unlike the others. Having insufficient data in contribution guide, creates doubts in mind of new contributor making them to not open their first PR. For e.g. TEAMMATES specifies to open an issue to communicate in case of any doubts, whereas other two projects don't, which leads to contributors to leave the project because they could not resolve their problem by asking the project maintainers in any way.

The only good thing about other two projects was that their review and merging process was very fast (although not efficient). TEAMMATES being a big organization makes it tougher for maintainers to do things in a faster manner. Although if the speed of reviewing can be increased, it would allow more contributors to do work faster and not keep them waiting for review. The other organizations seemed to be faster because they weren't very strict with code quality and other minor problems in PR. They would let it pass and it would lead to eventually another issue being created to solve it later on. Hence I think even if the pace is slower in TEAMMATES, if things are done perfectly in the first attempt, its better to keep it that way.

The best thing I liked about WikiMedia Commons App, was that if someone had asked to take up an issue, the organiazation would assign a label `assigned` so that no one else wastes their time working on it. However, the issue here was that since the team didn't effectively manage it, I could find many issues labeled as `assigned`, only to find out that the person who had requested to work on it had actually not even started it even after few weeks.

### Key Takeaways

- **GOOD** documentation is necessary for each project
- A more active senior developer team attracts more contributors
- Pace vs Perfection is a choice that the organization needs to makes
- Contributing Guidlines need to be explicit and followed religiously


## TAN JUN AN
**Project**: [mlpack](https://github.com/mlpack/mlpack)
* [Contribution Guide](https://github.com/mlpack/mlpack/blob/master/CONTRIBUTING.md)
* [Design Guidelines](https://github.com/mlpack/mlpack/wiki/DesignGuidelines)

**My Contributions**:
* [#1289](https://github.com/mlpack/mlpack/pull/1289)
* [#1310](https://github.com/mlpack/mlpack/pull/1310)
* [#1315](https://github.com/mlpack/mlpack/pull/1315)

**Observations**:

mlpack is a scalable machine learning library, written in C++ that provides these algorithms as simple command-line programs and C++ classes which can then be integrated into larger-scale machine learning solutions.

I chose mlpack as my external project as I wanted to gain some familiarity with working on large C++ projects, and also because I'm currently studying an Intro to Machine Learning module in NUS, and was interested in learning about the implementations of some of the algorithms.

Links to the instructions to build the project are easily found on the front page of both the github and website, and the instructions given are simple and clear to follow. Even the instructions to build on Windows Platform which is more complicated has a dedicated blog giving detailed step-by-step instructions to follow and screenshots to guide us along.

When looking for issues to fix, I noticed that some of the easy issues which were posted by the owner have detailed explanations on what the issue is and also gave hints or references to other PRs on how to solve the issue, which is very helpful especially for new developers hoping to learn more about the codebase on the go. We could try to bring these into SE-EDU with some of the `harder` issues, making some of those issues as `d.FirstTimer` instead but giving guidance on how to resolve the problem. This could attract and motivate some people to want to contribute over doing some trivial tasks such as removing 1 line of code, especially since we require them to write commit messages conforming to our conventions which takes up alot of time and effort, where they prefer to be actually working on the codebase.

For some issues which require doing multiple tasks, such as implementing of new binding tests, the owner maintains a to-do list on which task are still available for grabs and which are already taken/resolved. This allows contributors who wish to work on this issue to easily find a task to do without overlapping with other contributors and wasting their time on unnecessary work. This could be useful to bring over to SE-EDU, since we have an issue [Expand the scope of system tests](https://github.com/se-edu/addressbook-level4/issues/551) which also has a to-do list, but the list does not seem to be maintained, which would confuse and deter contributors from wanting to work on it.

The maintainers also takes care of their contributors well, thanking us for our contribution no matter how small, and offering to send us stickers to paste on our laptops after our first merged PR, which also serves to indirectly advertise their product as well. They also offer to open or  resolve minor issues found in our PRs by themselves if we are not free to do so ourselves.

However, 1 point in which mlpack can improve on would be to have a better commit organization. Compared to SE-EDU, the pull request process is very simple; There is no fixed naming convention for branches and pull requests, and no need for commit messages to explain what is done and organizing of commits. While this tends to make the life of new contributors easier and also makes the pull request process much faster, it may cause the project to become harder to maintain.

## TAN JUN KIAT
**Projects**:
1. [TEAMMATES](https://github.com/TEAMMATES/teammates)
1. [WikiMedia Commons App](https://github.com/commons-app/apps-android-commons)

**Contributions to External Projects**
- [#8377](https://github.com/TEAMMATES/teammates/pull/8377)
- [#8392](https://github.com/TEAMMATES/teammates/pull/8392)
- [#8376](https://github.com/TEAMMATES/teammates/pull/8376)
- [#1134](https://github.com/commons-app/apps-android-commons/pull/1134)

**Observations**:

Observations about Teammates/WikiMedia can be broadly divided into 2 categories: ***Documentation*** and ***Managing Contributions***. Each section would also suggest improvements for PowerPointLabs based on lessons learnt in the observations.

### Documentation

##### Contributor Information

Teammates is more structured in terms of its overall documentation and how they are displayed. Specifically, resources for new/current developers are very well organized. They have [Documentation for Developers](https://github.com/TEAMMATES/teammates/blob/master/docs/README.md), which details project architecture, set-up, workflow, and maintainer guide for core developers. There are even supplementary or how-to documents for further reading, and details important features like [God-mode](https://github.com/TEAMMATES/teammates/blob/master/docs/README.md#how-to-documents). There is also the [Contributor Orientation Guide](https://github.com/TEAMMATES/teammates/blob/master/docs/orientation-guide.md), which orientates new developers to project structure, set-up of dev environment and how to start contributing to Teammates.

WikiMedia is also another project that tries to include [extensive documentation](https://github.com/commons-app/apps-android-commons/wiki) in their github page. However they structure all these information differently than Teammates. Each of their articles exist almost in isolation, with very few links within each article linking to other articles. Each article is organised in a well-structured hierachcy, with related articles grouped together for clarity, e.g. "User Documentation", "Contributor Documentation", "Developer Documentation". This makes it very clear for users to know what information to look for and where.

While PowerPointLabs does have the basic [information](https://github.com/PowerPointLabs/PowerPointLabs) like project set-up and software design, it would be better to adopt a more formal structure like Teammates or WikiMedia in displaying information. A clear hierachcy of information can help to guide new contributors into the project. However, it is important to reduce the amount of information stored as well. One good thing about the approach of PowerPointLabs is that its instructions leave little room for set-up error because information displayed are kept to the bare minimum, hence instructions are understood easily.

Moving forward, perhaps we can consider adopting a structure as seen in WikiMedia or Teammates so that information can be more easily found whenever required. This is especially important as PowerPointLabs start to scale up in the future, and as we start to have more information that we need to display on the github page as would be mentioned below.

Another good example for future reference is the github page for [HTML5 Boilerplate](https://github.com/h5bp/html5-boilerplate), which concisely organises all essential information for easy reference.

##### Ideation

In Teammates, there is also the [Project Ideas Page](https://docs.google.com/document/d/1fAvYvQr0E93OsZgyneaXGX0jaMA-zptTIxqLn83xwN0/pub?embedded=true), which provides a structured way to discuss and store all ideas that can help to improve the project.

Currently, PowerPointLabs stores potential ideas in a private google doc. This doc is in a Google folder that is only accessible by the developers, hence it would be better if this doc can be made public, for new ideation from potential contributors, validation by existing developers and accountability/discussion/improvement of future ideas and features. Additional documents like “Common traps in PowerPoint Add-in Development”, and “Newcomer’s guide” would surely be useful for new contributors and can be considered for uploading on the PowerPointLabs github page for easier reference by incoming contributors.

### Managing Contributions

In terms of Teammates' Issues/PRs, their quality is enforced quite well. Issues are [documented](https://github.com/TEAMMATES/teammates/issues/8599) very well, with clear replicable steps listed and even screen shots posted so that any potential contributor can have clear information to work with. PRs are also checked at least twice by senior developers before requesting a review from the project mentor (Prof Damith). This layered check helps to ensure the quality of any PR that goes into the master branch. This is important because unlike PowerPointLabs which has a `dev-release` branch for dog-fooding, Teammates only has a main `master` branch, hence it is important to have many checks in place.

WikiMedia on the other hand, does not really enforce strict testing with their changes, and most of the time, only one senior developer would actually review the changes of the submitted PR. While this allows for greater flexibility in terms of implementation, it increases the responsibility of the contributor to ensure the quality of his work. I personally realised that some of their first timer issues are not well-scoped for new contributors as they can either be too [hard](https://github.com/commons-app/apps-android-commons/issues/1371), or requires an extensive changes to aspects like [UI](https://github.com/commons-app/apps-android-commons/issues/868). This, coupled with the lack of testing and ensuring of code quality, makes WikiMedia a less ideal project to learn best SE contributing practices from, as opposed to say Teammates or PowerPointLabs.

PowerPointLabs may be a smaller project comparatively, but it is good to learn from Teammates in how they structure their issues as well as review their PRs. With regards to whether PowerPointLabs would require the same amount of checks for each PR, I would say it's not compulsory for now because of the smaller project scale and better time efficiency, but I expect it to adopt the same quality of checks once it starts to scale up in the future.

In addition, PowerPointLabs can also learn from WikiMedia's mistakes, by scoping issues appropriately for each of the categories to ensure that new contributors are given an opportunity to gradually familiarise themselves with the project. This helps to motivate them long-term, ensuring better quality contributions in the future.

## TAN LI HAO
**Project**: [Servo](https://github.com/servo/servo)

[Contribution Guidelines](https://github.com/servo/servo/blob/master/CONTRIBUTING.md)

**My contributions**: [#18](https://github.com/servo/servo-warc-tests/pull/18), [#20495](https://github.com/servo/servo/pull/20495)

**Observations**:

Servo is a web browser engine written in the Rust language. Parts of Firefox has been and will be incrementally replaced with Servo.

#### Important things learned
Despite being a very large project spanning multiple repositories, Servo makes it relatively easy to contribute despite the complexity. It is interesting that such a complex project could make it so easy to contribute. I believe some of the factors that contributed to these are:
* It uses the familiar Github workflow for contributions
* Reviews are also done on Github but also optionally with a code review tool for more complicated changesets
* There are many quickstart guides to quickly get up to speed for contributions in different areas
* There are some issues that are mentored (a mentor will guide a contributor along the way) and there are many venues for help
* The engine is broke up into many much smaller components which are loosely coupled
* There is a lot of documentation, although not always in one place and not necessarily consistent or complete but done is probably better than perfect

Servo also don’t belong to the common category of applications, but in the category of system software such as operating systems and game engines. I made some observations that are interesting or differs from traditional applications:
* Performance improvements are of top priority and are more important if not more important than features
* The project is large and requires many concepts to understand, however the lines of code is only around ~300k for the main engine (excluding the dependencies)
* Other than following a Github workflow, there is really very little process required to contribute

#### Practices/Tools
Servo uses many tools to improve the developer experience. One of them that I believe can be almost immediately useful to TEAMMATES and other OSS-generic projects is Reviewable.

Reviewable is a code review tool that improves upon Github code review. I would some of the useful key features are:
* Review comments are not lost when there are changes to a line is pushed
* Supports rebased commits
* Tightly integrated with Github, which means that its features can be adopted incrementally

A common complaint is that Github’s code review system is lacking, and Gerrit code review is one of the alternatives. For example, there is a [discussion on Golang](https://github.com/golang/go/issues/21956) on this. However, the problem with external code review tools like Gerrit is that they increase the friction to contribution. While Reviewable does not have as many features as Gerrit, because it is tightly integrated with Github the reviewer and the author have complete freedom whether or not to use the tool and it will not affect any party.

Some other tools for general exploration (not related to any project):
* [Homu](https://github.com/barosl/homu) - automated merging
* [Highfive](https://github.com/servo/servo/wiki/Highfive) - Github bot that provides an encouraging atmosphere for new contributors, e.g. welcoming new contributors, assigning issues, assigning reviewers, etc.
* [Buildbot](https://buildbot.net/) - Continuous integration (e.g. Travis CI, Jenkins)
* [Saltstack](https://saltstack.com/community/) - Infrastructure management (Related: Kubernetes - container management)

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
* Contributions: [#1936](https://github.com/nltk/nltk/pull/1936)

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
* Contributions: [#503](https://github.com/opacapp/opacclient/pull/503)

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
[NUSMods R](https://github.com/nusmodifications/nusmods/tree/master/www)
* [contributing guideline](https://github.com/nusmodifications/nusmods/blob/master/CONTRIBUTING.md)
* [documentation](https://github.com/nusmodifications/nusmods/tree/master/www)
* my contribution: [#950](https://github.com/nusmodifications/nusmods/pull/950)

**Observations**:
- NUSMods R uses numerous well-known external libraries like [lodash](https://lodash.com/docs/4.17.5) and [react feather icons](https://feathericons.com/). This practice simplifies the code a lot, reduces the chances of the programmers writing duplicate code, and makes the search of the use of the function easy as most of these external libraries are well-documented.

- NUSMods R adopts [CSS modules](https://github.com/nusmodifications/nusmods/tree/master/www#writing-styles) to structure the style of the components. I find this approach very useful as eash style file is catered to one component, making it short and sweet. Moreover, the programmer doesn't have to worry about the complications of using the same tag identifier for different components.

- As they recently rewrote this website, there is not much technical debt and hence their first-timer issues are more about implementing a small feature, fixing a tiny bug or enhancing the codebase by adopting external libraries etc., which I find quite challenging for a beginer of React and Redux like me. (I think that is also one of the reasons why they do not have many external contributors.) However, I like how they guide the first time contributors in these issues by offering some suggestions on how to start and where to start in the description of the issue. For example, they will tell you which part of the code you can use as reference to make your life easier.

- And I have to praise them for their efficiency. One of the maintainers of the repository always responded to my questions within three minutes of posting with very detailed answers. A review is always followed immediately after each pushing of my code. One thing I find interesting (and a bit sad) is that the reviewer assigned to my PR started to help me rewrite my code after he realized I am new to React syntax and the file structure of NUSMods R. I felt a bit offended as that was only after the second round of review (which was done within one and a half hour of me making the PR), however I find it is a very efficient way to learn as it would take me rather long to understand his idea simply by describing what he wanted in the comments.

**Takeaways**:
- TEAMMATES can try to adopt the CSS modules approach to structure the stylings. Currently all the stylings are inside one big file (`teammatesCommon.css`) which I find rather unorganized, despite the fact that the within the files there are several sections segregated by comments about the use of each secion.

- TEAMMATES currently serves very well as a beginner-friendly platform. I like its current difficulty of first-timer issues, as it can give the beginner a sense of achievement as well as introducing them to our large code base. To make it a better learning platform, we can assist the beginners to progress into higher level issues by giving some guidance in the descriptions of the higher level issues which we think can act as a level-up for those who just completed their first-timer issues.


## YONG ZHI YUAN
**Project**: Exercism (Link to external project workflow: https://github.com/exercism/java/blob/master/CONTRIBUTING.md)

**My Contributions**:
[1188](https://github.com/exercism/java/pull/1188), [1118](https://github.com/exercism/problem-specifications/pull/1118), [1228](https://github.com/exercism/java/pull/1228), [1119](https://github.com/exercism/problem-specifications/pull/1119), [1232](https://github.com/exercism/java/pull/1232).

**Observations**:

I improved in my **resourcefulness** skills as I had to find out more about the project, understand the code base and look up on the processes on my own, instead of relying on senior developers as I did for the internal project. This is because it's more efficient to find out things on my own for the external project, since it is likely that my reviewers are living in a different time zone. As such, it may take me up to half a day before I receive a response; I respond in the day, and the other person responds at midnight or so. Whereas when I'm working on the internal project, the response is quicker, and we are able to converse & discuss multiple times throughout the day.

Working on the external project reminds me on the importance on having **proper documentation** in the Developer Guide. When I was choosing between the different external projects to contribute to, I first short-listed the projects based on those with better documentation, as it was easier for me to understand existing code and therefore allowing me to be able to better contribute to the project. For larger repositories, more effort must be made to write a good Developer Guide and to structure it well. The external project that I worked on had multiple repositories with lots of documentation, however it isn't structured well. As such, despite spending some time reading up the documentation, there were still portions that I missed out.

For example, in the AddressBook Level 4 Developer Guide, we can explicitly state something like, "For general information about how to contribute to AddressBook Level 4, please refer to the OSS-Generic Process", which will then bring them to the "process" repository. This isn’t done so at the moment.

Also, I noticed the need to have easy issues in the repository for newcomers, yet the issues should not be too easy either. For example, as I have already been working on OSS for a period of time, I am not too keen on working on simple first-timer issues such as fixing typos etc; it isn't exciting. Similarly, some of the potential contributors may have prior experience already and may feel the same way.

I noticed that the difference in difficulty between the 1st PR (which is a first timer issue) and the 2nd PR onwards that my CS3282 teammates have done, is quite steep. Linking to the previous point, it seems good to find **moderate sized issues** for potential contributors to work on. There are some in the code base, however we did not tag them according to the difficulty level (we do not such tags too), and as such it requires a bit of effort to source out which issues are moderate in difficulty.

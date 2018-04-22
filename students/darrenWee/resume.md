# Darren Wee Zhe Yu

<img src="darren.jpeg" width="100" /><br>

* **Email:** [`darren.wee@u.nus.edu`](mailto:darren.wee@u.nus.edu)
* **GitHub:** https://github.com/darrenwee
* **LinkedIn:** https://www.linkedin.com/in/darren-wee-668652148/
* **Google Scholar:** https://scholar.google.com.sg/citations?user=bmpJNasAAAAJ&hl=en
* **Website:** https://darrenwee.github.io

## Education
### National University of Singapore
Bachelor of Computing (Computer Science), 2015 - present <br>
(expected to graduate fall 2019)

* Specialization in Software Engineering
* University Scholars Program
* Minor in Public Health

## Professional Experience
### Institute for Infocomm Research, A\*STAR
Student Researcher/Research Assistant<br>
Nov 2013 - Jan 2017

- Acoustic modelling of whispered English and Mandarin speech using deep-learning algorithms.
- Collection of iWhisper-Mandarin speech corpus for speech technology applications.
- Investigation of phonological error patterns during acquisition of spoken Mandarin by Singaporean children and non-natives of European descent for developing computer-assisted language learning systems.
- Design and acoustic analysis of novel Singaporean children spoken English corpus for computer-assisted language learning systems.
- Visualization of linguistic and experimental data.

## Skills
### Computer Languages
* **Proficient:** Java, Python, Perl, Bash, R, LaTeX
* **Intermediate:** C, Go, HTML, CSS, Matlab

### Dev Ops
git, gradle, cucumber, travis-ci

### Computer Software
unix-like operating systems, Windows

## Expert Areas
### Go
- Delivered a talk on the features of Go and why you should learn Go ([slides](https://docs.google.com/presentation/d/1gjksgaZ2RK6crbZvGWQLnlCu1PcDBox_IibqsZS6VmI/edit?usp=sharing))
- Reviewed book chapter on introduction to Go ([chapter](https://github.com/se-edu/learningresources/blob/master/contents/go/Go.md), [PR](https://github.com/se-edu/learningresources/pull/48))
- Worked on [`github/hub`](https://github.com/github/hub), a command-line utility that wraps around git on a terminal. `hub` is implemented in Go.

### Git
- Delivered a talk on best practices with git ([slides](https://docs.google.com/presentation/d/1Wj9zmEKEnLbPzPz2Ifl7ZZcayJr6QjqfoJkt1zfwqpg/edit?usp=sharing))
- Wrote book chapter on git best practices ([chapter](https://github.com/se-edu/learningresources/blob/master/contents/revisionControl/bestPracticesGit.md), [PR](https://github.com/se-edu/learningresources/pull/40))
- Worked on [`github/hub`](https://github.com/github/hub), a command-line utility that wraps around git on a terminal. Developing on `hub` requires a decent understanding of how git works.

## Projects
### TEAMMATES
TEAMMATES is a free online tool for managing peer evaluations and other feedback paths of your students. It is provided as a cloud-based service for educators/students and is currently used by hundreds of universities across the world. TEAMMATES is implemented with Java EE.

Responsibilities:

- Review pull requests from other contributors
- Author issues on bugs discovered during development
- Refactored code base as part of migration to Java 8:
    - Part of team which migrated backend code to use Java 8's `java.time` API ([project](https://github.com/TEAMMATES/teammates/projects/3))
    - Migrate code base to use other Java 8 features such as streams for better code quality and brevity
    - Reduce technical debt while refactoring by improving code quality
- Guide new contributors when they have issues setting up the developer environment
- Miscellaneous duties: updating documentation, poster making, overhaul of the repository bot (work-in-progress)

### hub
hub is a command-line utility that acts as a wrapper around git made by GitHub. hub integrates GitHub functionality into your Terminal, allowing you to retrieve issues or make pull requests to GitHub from your terminal. hub is implemented in Go.

- Implemented new feature, `hub issue labels` to fetch the available issue labels in a GitHub repository ([PR](https://github.com/github/hub/pull/1667))
- Modified default protocol behavior of hub when cloning a new repository ([PR](https://github.com/github/hub/pull/1690))

### VOGLBot/AndreaBot
A set of Telegram bots made for the University Scholars Program's freshmen orientation.

* VOGLBot makes handling attendance and participant information easy and less clunky by relying on commands issued via Telegram
* AndreaBot handles announcements via a single interface and allows for group-based announcements. (*at the time of development/deployment, Telegram did not have read-only channels*)
* Both bots implemented using python3 and mongodb
* Users would issue simple text commands to perform CRUD operations for orientation attendees

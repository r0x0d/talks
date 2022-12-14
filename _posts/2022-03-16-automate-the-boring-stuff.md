---
title: Automate the boring stuff
author: r0x0d
date: 2022-03-16 12:00:00 +0300
theme: black
categories: [Automation, GitHub, "pre-commit"]
tags: [automation, github, "pre-commit"]
---

## Automate the boring stuff

----

## Hi there! 👋

For everyone here who doesn’t know me, let me make a quick introduction.

~~

## Who am I?

My name is Rodolfo Olivieri, and currently, living in Brazil 🇧🇷.

~~

## What do I do?

I work at Red Hat as a Software Engineer in the convert2rhel tool.

~~

## Where you can find me?

Check out my [personal website](https://r0x0d.github.io) that contain all the
info you might need!

----

## What is this all about?

This talk is an introduction to show that we can ~and should~ automate some of
the tools we use every day.

Notes:

This presentation has the intention to show how you can automate some of the
tools that we all use day-to-day. Probably most of the tools I will show here
some of you have already seen or used, but the intent is not to teach how to use
those tools, but rather, to show that you can use any CI system to automate
them!

----

## What is a CI?

CI stands for Continuous Integration. As the name suggests, it’s a way for us to
run our automatic workflows in a continuous way!

Notes:

Some other CI systems that you might know about are:

- Travis CI
- Azure Pipelines
- AppVeyor
- and others…

----

## Let’s focus on

Since there are a bunch of things we could do in a CI system, let’s focus on a
few selected categories to not lose track.

- Linters
- Formatters
- Testing

Notes:

I selected those three categories because they are the most common tools that we
run in our development workflow every day.

----

## What is a Linter?

It’s a tool that analyzes the source code to detected bugs, programming errors,
style, security alerts, and much more…

~~

## Example of linters

- [mypy](https://github.com/python/mypy)
- [bandit](https://github.com/PyCQA/bandit)
- [flake8](https://github.com/PyCQA/flake8)
- bunch of others…

----

## What is a Formatter?

It’s a tool that analyzes the source code (like a linter) but can modify and
apply consistent patterns to the source code.

~~

## Example of formatters

- [black](https://github.com/psf/black)
- [autopepe8](https://github.com/hhatto/autopep8)
- [isort](https://github.com/PyCQA/isort)
- bunch of others...

----

## Test runners

Test runners are a way to run your invocation flow for your tests, either being
a unit, integration, or any other type of tests.

~~

## Example of test runners

- [unittest](https://docs.python.org/3/library/unittest.html)
- [nose2](https://github.com/nose-devs/nose2)
- [pytest](https://github.com/pytest-dev/pytest)
- bunch of others...

----

## How do we automate those tools?

Let’s see how we can automate those tools with some CI systems.

----

## GitHub Actions

It’s an integrated CI system that just works with every repository in GitHub
(being public or private) with a minimal workflow configuration.

Notes:

So, the first one I want to talk about is the GitHub Actions. <>. This is a very
powerful CI system that facilitates our work when we want to do workflows that
are either simple, complex, or anything in that range actually.

~~

## Is there a guide to learn more?

GitHub has a very nice documentation on how their CI systems work in a very
detailed way [Understanding GitHub Actions](https://docs.github.com/en/actions/learn-github-actions/understanding-github-actions).

----

## pre-commit.ci

It’s a CI system that works exclusively with the pre-commit tool. It can run
your [pre-commit](https://github.com/pre-commit/pre-commit) configuration,
auto-update the dependencies, and auto fixes your code.

Notes:

The pre-commit tool is a very versatile tool that enables us to run a bunch of
different “hooks” before doing a commit. Those hooks (or dependencies) usually
are the tools I showed before, like flake8, black, mypy, and so on… The big
advantage we have with pre-commit is that it runs all of them at once and we
don’t need to individually call them.

~~

## Is there a guide to learn more?

[pre-commit](https://pre-commit.com/#intro) has nice documentation that shows
you how to configure the tool itself. And porting this out to
[pre-commit.ci](https://pre-commit.ci/) doesn’t require any changes, just
installing the app on your account/repo.

----

## Let’s see this in practice

Demo repository: [automate-the-boring-stuff-demo](https://github.com/r0x0d/automate-the-boring-stuff-demo)

Notes:

Now we will take a closer look at this demo repository I made to give you a
better visualization of what those CI systems look like!

----

## If you want something pre-made

Checkout my cookiecutter repository [cookiecutter-python-project](https://github.com/r0x0d/cookiecutter-python-projects)

Notes:

This is a template cookiecutter repository I made that has some pre-configured
things that I like to use when I’m working on new projects. It comes with all
the GitHub Actions CI configured, pre-commit, and other things too!

----

## References

- [What is a linter and why your team should use it](https://sourcelevel.io/blog/what-is-a-linter-and-why-your-team-should-use-it)
- [What Is a Linter? Here’s a Definition and Quick-Start Guide](https://www.testim.io/blog/what-is-a-linter-heres-a-definition-and-quick-start-guide/)
- [Python Code Quality: Tools & Best Practices](https://realpython.com/python-code-quality/)
- [Python code formatters](https://deepsource.io/blog/python-code-formatters/)
- [Getting Started With Testing in Python](https://realpython.com/python-testing/)
- [Understanding GitHub Actions](https://docs.github.com/en/actions/learn-github-actions/understanding-github-actions)
- [GitHub Repository: pre-commit](https://github.com/pre-commit/pre-commit)
- [Documentation of pre-commit.com](https://pre-commit.com)
- [Documentation of pre-commit.ci](https://pre-commit.ci)

----

## Thank you

# anacapa-skills-octokit
A skill builder repo for Octokit

# What is Octokit and why do we care

Octokit is a Ruby language wrapper around the github API.

We care because Anacapa Grader is layered on top of github.   Octokit is our main tool for interfacing our own code with github's features.

# Getting Started With Octokit

The first thing to understand is how to authenticate with Octokit without hard coding usernames and passwords.

So, in the octokit documentation, this is probably the place to start:

First, create a "github access token for command line use" by following the instructions below.  Note that when you make this personal access token, you need to save it somewhere, because you only get to see it once and then you never get to see it again---if you forget it, you have to just delete the old one and make a new one.

BUT: this access token can be used just like a hard coded password. So DON'T commit it into any github repo.   

You might want to make a temporary text document in a text editor and paste it in there, but then not save it right away.

* https://help.github.com/articles/creating-an-access-token-for-command-line-use/

Then, try reading this documentation:

* https://github.com/octokit/octokit.rb#oauth-access-tokens


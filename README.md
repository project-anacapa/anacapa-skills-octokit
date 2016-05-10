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

You'll get a 40-character access token, something like:

 92342983fae9098090990d098098b098098c0980e009989a

So then, you'll want to use an interactive Ruby REPL such as irb or pry (try `gem install pry` if `pry` doesn't work at the command line.)

In that REPL, first do:

 require('octokit')

Then you should be able to type:

 client = Octokit::Client.new(:access_token => "Your 40 character token here")

And it should work.  For example:

```
[2] pry(main)> require 'octokit'
=> true
[3] pry(main)> client = Octokit::Client.new(:access_token => "8987a98797b978987987c98797ed9879d")
=> #<Octokit::Client:0x3fd376dcdb18>
[4] pry(main)> 
```

Then what can you do?  Try reading this documentation for some clues:

* https://github.com/octokit/octokit.rb#oauth-access-tokens


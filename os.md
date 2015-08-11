Contributing to Other People's Projects
=======================================

Contributing to open source software is a difficult and rewarding process.
Contrary to popular belief, it does not require a lot of programming skill, but
rather patience, creativity, and diligence. In this post I will explain some
crucial steps and skills which even experienced contributors sometimes forget.
This is not a magic formula, and contributions will require focus and work, but
in the end I believe the feeling that you are part of a community and that you
have contributed to something greater than yourself is personally fulfilling.
It is also an accomplishment employers like to see and even many non-technical
people will respect.

The Open Source community is has a reputation of being hard on newbies. I think this
reputation is generally ill-deserved. Sure, some of the big names get a bad
rap, but in my experience people who have small projects will be ecstatic about
your contributions. And I mean Exclamation Points! and  merging code before you
think it's even ready. However, there is a rotten apple in every bunch, so don't
be afraid to stop, close your pull request, take a breather, and try again
somewhere else. Sometimes I've realized I'm in over my head, but in retrospect
those failures to have been my most valuable learning experiences.

Finding a Project
-----------------

Maybe you already have a project in mind. That's great! Skip to the next part,
but you may find the project isn't everything it seems at first, so don't be
afraid to come back here.


Evaluating a Project
--------------------

Is this project worth my time? Here are some quick ways to find out.

NOTE: Include pictures and links.

1. When was the last commit made? 
   If nobody has touched it in a month or so, you might not get a quick response. 
2. How many pull requests are open? How old are they? 
   If simple PRs don't get any attention for weeks or months, yours probably won't either. PRs more than a couple weeks old with no comments on them can be a red flag, whereas old PRs with a lengthy discussion attached are probably unmerged because they're controversial or challenging. 
3. Does one fork have a lot more activity than this one? 
   If a GitHub project looks abandoned, check the network graph (`https://github.com/OWNER/REPO/network`) to see whether there's a fork with newer commits. If so, it could mean that someone else has taken over maintaining the project. 
4. When was the last time a PR got merged by someone who isn't part of the core team? 
   Equivalently, are there contributions from multiple authors? Take a look at `https://github.com/OWNER/REPO/graphs/contributors`. 

That's a lot of questions, but GitHub's tools make them easy to answer.

What is a Valuable Contribution?
--------------------------------

A lot of people think that the most valuable open source contribution is code.
They have been mislead. Most projects lack the most basic documentation. Other
projects are in need of a good logo, so if you're a photoshop wizard it
might be cool to bounce a neat design off the author.
A good way to see if you want to contribute to a project is to read the README and set
everything up. Usually the directions are vague, inaccurate, or specific to a
certain operating system or package manager. If you run into problems reread
everything. If you find something to fix and improve, go ahead and submit something, even a one line
change which says something like:

	If you're running Ubuntu, install the libxml2 package:
	`$ sudo apt-get install libxml2`

Always remember to run a spell checker on your work. It makes it much more
professional-looking.

One rule of thumb for whether your contribution would be valuable is this: Did you have to Google for something about the project in order to get it installed? If so, it would be valuable to add the answer to the installation guide. 

Finding an Issue to Fix
-----------------------
Look for bugs labled "help wanted", "easy", "low priority", etc. Hop on IRC and ask the owners! Ask the owners what they want fixed. Grep for `TODO` or `FIXME`, they are sometimes one line changes, or things like "fix this regex, it matches too much".

Check the continuous integration badge in the README. If it's red, go look at the build and see if it has an error that you can fix. If the repo has a `.travis.yml` but no CI badge, your first commit can be to add it!

Diving In
---------
Now that you've found an issue to fix, it's time to propose your change! Just as it's usually rude to show up unexpectedly at someone's office and start shouting at them, there are some basic manners that you'll be more successful in open source if you observe. 

* Break changes into logical groups. 
  If you propose a compiler speedup and a website theme improvement and some typo fixes in the installation instructions all in the same commit or even pull request, the project maintainers will have a hard time reviewing your suggestions. Instead, you should propose the compiler speedup with its tests and documentation as one PR, the website theme changes with any relevant tests as another, and the documentation improvements as a third. This makes it easier for the project maintainers to give you focused, relevant feedback and merge those of your changes that they approve of immediately.

* Include tests and documentation if you're adding code. 
  There are 3 parts to any feature: The code, the tests, and the docs. Any PR that adds tests and docs to existing code, or code and docs to an existing test, is likely to be welcomed.

* Try to understand your target audience when writing, and state your assumptions. 
  To know your audience when writing code, look at the style guidelines if the project has them, and examine the existing code around your change. Do they use spaces (how many?) or tabs? Are their lines wrapped at 80 or 100 characters? Do they import new libraries whenever they're needed, or prefer to simply re-implement small features? Are they optimizing for speed or for readability? In your PR comments, anticipate the maintainers' questions and state the assumptions you made. 

* If the project has tests, run them.
  If it's hard to run the tests locally, file issues about the problems run into, or propose improvements to the documentation on how to run the tests.

You're comitted now. If it's a little change, get in, get out, make the change a little as possible. Don't touch things other than the bare minimum which needs to be fixed. Play the game "what is the smallest number of lines I need to change to fix the bug". It's like golf.

If it's a big project it's time to spend an hour with the debugger. Don't be afraid, it will all pay off. Once you've fixed one bug and understand how the project is laid out the second and third will come much easier.

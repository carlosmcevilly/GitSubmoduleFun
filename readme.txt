FakeProject
===========

This project was our playground for adding a git submodule to
a git repository.

It doesn't contain any code of its own, and it doesn't even
make use of the submodule it includes. But... read on...

What it does contain that is useful (I hope) is this readme
file, which tells how to use a project as a submodule in
your git repository.


-----------------------------------
As a person setting up a repository
-----------------------------------

To add a git project (say, the very useful json-framework
project) as a submodule in your repository, do:

(Since I'm mixing commands and comments here, I'll use $ to
indicate a command prompt followed by your command)

$ git submodule add git://github.com/stig/json-framework.git

then:

$ git submodule init

After doing the above line, you now have a .gitmodules
file in the top-level directory of your project.

The below step won't be needed since you just added the
submodule seconds ago, but it won't hurt anything:

$ git submodule update


---------------------------------------
As a person who has cloned a repository
---------------------------------------

After cloning a repository that uses submodules, you then
need to run these once:

$ git submodule init
$ git submodule update

Then from time to time, it's a good idea to run:

$ git submodule update

again to get the latest code from the submodule. If you
are the person who set up the repository using a submodule
in the first place, you'll need to tell any users who are
cloning your repository to do the above steps.



---------------------------------------------------------------------
This project was developed as sample code for the iOS Developer Study
Group that meets at the Hacker Dojo in Mountain View, CA.

It is provided under the terms of the Apache license.
---------------------------------------------------------------------


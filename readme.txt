FakeProject
===========

This project was our playground for adding a git submodule to
a git repository.

It doesn't contain any code of its own, and it doesn't even
make use of the submodule it includes. But... read on...

What it does contain that is useful is this readme file,
which tells how to use a project as a submodule in your
git repository.

As a person setting up a repository
-----------------------------------

To add a git project (say, the very useful json-framework
project) as a submodule in your repository, do:

git submodule add git://github.com/stig/json-framework.git

then:

git submodule init

# after doing the above line, you now have a .gitsubmodules
# file in the top-level directory of your project.

# this next step won't be needed since you just added the
# submodule seconds ago, but it won't hurt anything.

git submodule update

As a person who has cloned a repository
---------------------------------------

After cloning a repository that uses submodules, you then
need to run these once:

git submodule init
git submodule update

Then from time to time, it's a good idea to run

git submodule update

again to get the latest code from the submodule.



Robot-Framework Example Buildout:
---------------------------------

 https://github.com/plone/buildout.coredev/tree/4.1-robot
 
How to get started with Robot Framework:
----------------------------------------
To get started, you need to first fork the 4.1-robot repository and then clone and create the Robot Framework coredev buildout.
 
Fork the 4.1-robot repository:
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
 
    Go to https://github.com/plone/buildout.coredev/tree/4.1-robot

    Click the "Fork" Button

    A new fork will be available at https://github.com/<YOUR_GITHUB_USERNAME>/buildout.coredev/

   
Clone and create the Robot Framework coredev buildout:
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

::
 
    $ git clone https://github.com/<YOUR_GITHUB_USERNAME>/buildout.coredev
    $ cd buildout.coredev
    $ git checkout 4.1-robot
   
or use

::

    $ git clone -b 4.1-robot https://github.com/<YOUR_GITHUB_USERNAME/buildout.coredev

to clone the branch

::
   
    $ python2.6 bootstrap.py
    $ bin/buildout -c pybot.cfg

Once buildout is completed, to run the sample tests type

::

    $ bin/pybot acceptance-tests
 
If you want pybot to leave the browser up at the point of a failure so you can inspect the failure, you can use the following::
 
    $ bin/pybot --runmode SkipTeardownOnExit --runmode ExitOnFailure acceptance-tests
  
 
**If you get any of the following errors try these solutions**

*Error*
  Error: Couldn't find a distribution for 'robotframework-seleniumlibrary'.
*Solution*
  Make sure you have Mercurial installed on your system.

..

*Error*
  [ ERROR ] Parsing '/home/emanlove/buildout.coredev/acceptance-tests' failed: Data source does not exist.
*Solution*
  You need to re-fetch the repository and merge with your local repository. Try::

    $ git fetch plone
    $ git merge plone/4.1-plone


How to contibute to Plone's Robot Framework
-------------------------------------------

Write tests
~~~~~~~~~~~

The goal is to increase the test coverage of Plone's javascript.  We are looking for people to write tests to test Plone's javascript.

?? what do we want to test ??

?? do we want to provide guidelines or shall we push to just get more tests without restricting guidelines ??

In addition, we need to work out several issues including

1. keywords -  ?? explain issue and what we are trying to resolve ??
   
2. vocabulary/conventions -  ?? explain issue and what we are trying to resolve ??
   
3. directory structure -  ?? explain issue and what we are trying to resolve ??


Integrate robot framework into Plone's testing framework
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

For reasons of test isolation it is important to intergrate the robot framework into the Plone testing framework.

% title: Best Practices in Coding
% subtitle: Not just Python
% author: Tim van Boxtel
% thankyou: Thanks everyone!
% contact: <span>email</span> vanboxtj@mcmaster.ca
% contact: <span>github</span> <a href="http://github.com">SunPowered</a>
% favicon: favicon.ico
---
title: Contents

- Introduction
- Version Control (git)
- Open Sourced Projects
- Exercise: Collaborative Coding
- Conclusion

---
title: Introduction
subtitle: Why code properly?
class: segue dark nobackground

---
title: Introduction
subtitle: Why code properly?
build_lists: true

Proper coding practices should be considered ...

- if you are developing the code with others
- if you are distributing the code with users
- if you will be coming back to code later
- just cause ...
 
---
title: Version Control
subtitle: I like git
class: segue dark nobackground

---
title: Version Control
subtitle: Making the case
build_lists: true

Version control is all about keeping track of changes as well being able to quickly try new things and/or go back to a better time.

- What if you have 20 people working on a set of code?
- What if you want to try a new idea without interfering with a 'master' version?
- What if you want to have different versions to distribute?
- What if you realize you made a terrible mistake a month ago?

---
title: Version Control
subtitle: Short History
build_lists: true

The problem case has been known for decades, the solutions have evolved:

- Originally, people would work on a single codebase with file locks - <span class="red">bad</span>
- Later, centralized repositories evolved - <span class="yellow">better</span>
- Recently, a distributed approach has gained the most traction - <span class="green">best</span>

---
title: Version Control
subtitle: The idea
build_lists: true

The developer:

- Makes changes as they wish locally
- Commits the changes often
- Updates/push their changes to a network host
- Pull/Fetch other changes from the network host

---
title: Version Control
subtitle: Centralized Repositories
class: img-top-center

<img src="figures/centralized-version-control.png" style="width: 60%;">

<footer class="source">https://homes.cs.washington.edu/~mernst/advice/version-control.html</footer>

---
title: Version Control
subtitle: Centralized Repositories
build_lists: true

Centralized Version Control Systems:

- Solves the problem of having multiple copies of a codebase locally
- Requires a server hosting the master copy
- Each and every change must be updated to the server
- Difficult to try new ideas or share updates with only a few people

---
title: Version Control
subtitle: Decentralized Repositories
class: img-top-center

<img src="figures/decentralized-version-control.png" style="width: 60%;">

<footer class="source">https://homes.cs.washington.edu/~mernst/advice/version-control.html</footer>

---
title: Version Control
subtitle: Decentralized Repositories
build_lists: true

- No one master copy, every developer has the master
- No server required, though hosting of repositories on servers is common
- Can push many commits at once
- Easy to try new ideas with branching

---
title: Version Control
subtitle: Decentralized Repositories
build_lists: true

Common DVCS (Distributed Version Control System's):

- git (my preference)
- Mercurial
- Bazaar

---
title: Version Control
subtitle: git
class: img-top-center

<img src="figures/git-workflow.svg">

<footer class="source">https://www.atlassian.com/git/tutorials/comparing-workflows/gitflow-workflow</footer>

---
title: Version Control
subtitle: git
build_lists: true

Most DVCS allow you to:

- Branch from a commit point to a new lineage
- Merge from another branch
- Roll back to any previous state
- Take certain parts from any commit (cherry pick)

---
title: Version Control
subtitle: git GUI

Many use git straight from the command line, though many GUI's are available

<a href="http://git-scm.com/downloads/guis">http://git-scm.com/downloads/guis</a> 

- I recommend using one of these if the command line is a scary thought for you

---
title: Version Control
subtitle: git Repositories
build_lists: true

Repositories are shared, usually on a server.  There are many services set up for this, e.g.:

- GitHub <a href="https://github.com">www.github.com</a>
- Bitbucket <a href="https://bitbucket.org/">www.bitbucket.org</a>

---
title: Version Control
subtitle: git Repositories
build_lists: true

- You can 'clone' other people's repositories locally
- You can 'fork' other repositories, which copies it to your user space
- Different repository locations are handled via 'remotes'
- All of this is the heart of most open sourced projects

---
title: Open Sourced Projects
subtitle: Free (as in beer and speech)
class: segue dark nobackground

---
title: Open Sourced Projects
subtitle: Licenses
build_lists: true

Generally, code you write 

- belongs to you
- cannot be modified by anyone else
- cannot be copied by anyone else

---
title: Open Sourced Projects
subtitle: Licenses
build_lists: true

If you wish to share your code with the world, a license must be distributed with the codebase:

- The license grants certain privileges to other users
- The license can be as restrictive or as open as you wish
- There are many different types of free software licenses, some common ones:
    + GNU Public License
    + Apache License

---
title: Open Sourced Projects
subtitle: Distributing
build_lists: true

Typically, if you fork an open sourced project and modify it, it is required to re-release it under a similar license

- The power is not in the code, rather in the use of the code
- Old software models try to restrict code distribution
    + This limits who can use it
    + Makes learning how to code just as difficult

---
title: Open Sourced Projects
subtitle: Free Software
build_lists: true

There has been a real paradigm shift amongst developers:

- Software should be free
    + Free as in beer
    + Free as in speech
- We all use other people's code, so why not contribute ourselves?

---
title: Open Sourced Projects
subtitle: Corporate Development
build_lists: true

Many corporations are using open-sourced software.  Their developers improve  the source and contribute to the various projects.  

Typically:

- They can still make money off of free software
- The open source code is better
- The code is more robust

---
title: Collaborative Coding
subtitle: Exercise
class: segue dark nobackground

---
title: Collaborative Coding
subtitle: GitHub Repository

I have an empty repository set up for us to use today:

<a href="https://github.com/SunPowered/python-workshop-collab">https://github.com/SunPowered/python-workshop-collab</a>

---
title: Collaborative Coding
subtitle: Clone Repository

Clone the repository:

<pre class="code">git clone https://github.com/SunPowered/python-workshop-collab.git</pre>

---
title: Collaborative Coding
subtitle: Issue Tracking

Check out any open issues to contribute to at

<a href="https://github.com/SunPowered/python-workshop-collab/issues">https://github.com/SunPowered/python-workshop-collab/issues</a>

---
title: Collaborative Coding
subtitle: Useful git workflow

Create branch

<pre>
    git branch "branchname"
</pre>

Commit Changes

<pre>
    git add "filename"
    git commit -m "A descriptive commit message"
</pre>

Push Changes Remotely

<pre>
    git push origin
</pre>

---
title: Collaborative Coding
subtitle: Code Away!

- Pick an issue
- Create a branch for the fix
- Code the fix
- Commit often
- Push changes to repository
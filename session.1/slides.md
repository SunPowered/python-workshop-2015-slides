% title: Python Workshop for Grad Students
% subtitle: 1 - Getting Started
% author: Tim van Boxtel
% thankyou: Thanks everyone for attending!
% contact: <span>github</span> <a href="http://github.com/sunpowered">SunPowered</a>
% favicon: favicon.ico

---
title: Contents
subtitle: The Lineup

- Introduction / Goals
- System SetUp
- PyHistory
- Getting Help
- Running a Program
- Language Basics

---
title: Introduction
subtitle: Who is this guy?
class: segue dark nobackground

---
title: Introduction
subtitle: Workshop Code
build_lists: true

The code for this workshop is located online:

- Slides: 
    + <a href="http://github.com/SunPowered/python-workshop-2015-slides">http://tinyurl.com/macegs-python-2015-slides</a>
- Code: 
    + <a href="http://github.com/SunPowered/python-workshop-2015">http://tinyurl.com/macegs-python-2015</a>
---
title: Introduction
subtitle: Goals
build_lists: true

By the end of the session, you will:

-  Understand Python syntax
-  Have learned primitive object types
-  Grasp built in operators and control flow
-  Create simple functions
-  Work with the Spyder development environment

---
title: Setting Up
subtitle: Get all the things
build_lists:true

Let's all make sure we have our workspaces organized

- Workshop Folder
- Fork the workshop code repository on Github
- Clone your own fork locally into the workshop folder
- Add my repository as a remote called `parent`
- Set Workspace in Spyder to Worksop Folder
- Import local workshop code folder into Spyder

---
title: PyHistory
class: segue dark nobackground

---
title: PyHistory
subtitle: Humble Beginnings
class: img-top-center
build_lists: true

- First developed by Guido van Rossum
- <img style="width: 200px;" src="figures/Guido.jpg"/>

---
title: PyHistory
subtitle: Release History
build_lists: true

- First release in 1989
- Python 2.0 released in 2000, focus on community backed process
- Python 3.0 released in 2008, backwards incompatible

---
title: PyHistory
subtitle: The scourge of Python 3 (sort of)
build_lists: true

- The latest version, first released in 2008
- Backwards incompatible, in order to solve some longer standing 'issues'
- Disparity of new users vs legacy users
- As yet, somewhat unresolved, we really should be moving there eventually


---
title: PyHistory
subtitle: PEPs
build_lists: true

- PEP -- Python Enhancement proposals
    + <a href="https://www.python.org/dev/peps/">https://www.python.org/dev/peps/</a>
- Freely available design specs
- Well defined code patterns and style guides:
    + ie. <a href="https://www.python.org/dev/peps/pep-0008/">PEP8</a>

---
title: PyHistory
subtitle: The Python Software Foundation
build_lists: true

- A NFP committed to promoting and advancing the Python software language
    + <a href="https://www.python.org/psf-landing/">https://www.python.org/psf-landing/</a>
- Owns IP
- Organizes conferences (PyCon)
- Contributes to Python's overall awesomeness

---
title: PyHistory
subtitle: The Zen of Python

- <pre class="prettyprint" data-lang="python">
    >>> import this
    The Zen of Python, by Tim Peters
    Beautiful is better than ugly.
    Explicit is better than implicit.
    Simple is better than complex.
    Complex is better than complicated.
    ...</pre>


---
title: Getting Help
subtitle: Useful Resources
class: segue dark nobackground

---
title: Getting Help
subtitle: Python Docs

All core documentation available online at <a href="https://docs.python.org/2.7/">https://docs.python.org/2.7/</a>

Great reference for all levels

---
title: Getting Help
subtitle: Stackoverflow
build_lists: true

<a href="http://stackoverflow.com/">http://stackoverflow.com/</a>

- Social based question/answer community for programming languages
- Correct answers upvoted and marked as solutions
- All levels of questions
- Gamification makes it fun for the users

---
title: Running a Program
subtitle: Components
class: segue dark nobackground


---
title: Running a Program
subtitle: The Interpreter and its Environment
build_lists: true

- Interpreter
    + The core of the language
    + Evaluates lines and blocks of code
- Environment
    + Builtins
    + <pre data-lang="python">>>>len(dir(\__builtins__))
        145</pre>

---
title: Running a Program
subtitle: The Interpreter and its Environment
build_lists: true

- Environment:
    + Locally installed third party packages are also available on the PATH
    + <pre class="prettyprint" data-lang="python">
        >>> import sys
        >>> print sys.path
        ['',
        '/sys/path/1',
        '/sys/path/2',
        ...]</pre>

---
title: Running a Program
subtitle: Some Nomenclature
build_lists: true

- Module
    + A single Python '.py' file.  This can be run on its own or imported by other modules.
    + <pre class="prettyprint" data-lang-"python">import my_module</pre>

---
title: Running a Program
subtitle: Some Nomenclature
build_lists: true

- Package
    + A namespace that bundles modules and other packages, designated with '.'
    + Corresponds with a directory heierarchy
    + <pre class="prettyprint" data-lang-"python">
        import my_package
        my_package.my_function()
        from my_package import my_module
        my_module.another_function()</pre>
    

---
title: Running a Program
subtitle: REPL is hard
build_lists: true

- REPL: Read, Eval, Print, Loop
- But, Python is interpreted!
    + We can run files with many lines of code:
    + <pre class="prettyprint" data-lang="cmd">
        $> python do_all_the_things.py
        Started ... I have now done all the things
        $>
      </pre>
- Other IDE's can also run our code for us

---
title: Running a Program
subtitle: Importing Other Packages
build_lists: true

Use other packages in your code

- <pre class="prettyprint" data-lang="python">
    import time
    now = time.time()
    now_minus_five = now - 5
    print "5 seconds ago was " + now_minus_five</pre>
---
title: Running a Program
subtitle: Using Other Packages
build_lists: true

- I do not want to code everything I do from scratch
- Leverage the power of open-sourced
- `pip` a great tool for managing python packages
    + <pre class="prettyprint" data-lang="cmd">$> pip install numpy</pre>

---
title: Language Basics
subtitle: Show me some of the things
class: segue dark nobackground

---
title: Language Basics
subtitle: The Python Object
build_lists: true

Everything is an object!

- Python is largely type agnostic
- Many object types can share methods (or overwrite!)
- Gives much of Python it's *magic*

---
title: Language Basics
subtitle: Common Types of Objects
build_lists: true
class: tight-article

- Numerics
    + <pre>int, float, long</pre>
- Booleans:
    + <pre>True, False, None</pre>
- Mappings:
    + <pre>str, list, tuple, dict, set</pre>

---
title: Language Basics
subtitle: Common Types of Objects
build_lists: true

- Functions:
    + <pre>max, min, ...</pre>
    + <pre class="prettyprint" data-lang="python">
        def my_function(arguments):
            ... # Do some stuff
            return val
        >>> ret = my_function("Home")
        >>> ret2 = my_function(2)</pre>

---
title: Language Basics
subtitle: Common Types of Objects
build_lists: true

- Classes:
    + <pre class="prettyprint" data-lang="python">
        class Person(Animal):
            def \__init__(self, name, age):
                self.name = name
                self.age = age
            def birth_year(self):
                return 2015 - self.age</pre>
    + <pre class="prettyprint" data-lang="python">
        >>> jeb = Person("Jeb Springfield", 53)
        >>> batman = Person("Bruce Wayne", 45)</pre>

---
title: Language Basics
subtitle: Common Types of Objects

- Classes:
    + <pre class="prettyprint" data-lang="python">
        >>> print jeb.age
        53
        >>> print batman.name
        Bruce Wayne
        >>> jeb.birth_year()
        1962</pre>
---
title: Language Basics
subtitle: Numerics

- <pre class="prettyprint" data-lang="python">
    >>> myint = int(3.0)
    >>> print myint * 4
    12
    >>> print myint + 7
    10
    >>> myint - 2
    1
    >>> 3 / 2 # Division of ints rounds down, returns an int
    1
    >>> 3.0 / 2 # Division with a float in it returns a float
    1.5
    >>> 10 % 4 # %: Modulo
    2</pre>
---
title: Langugage Basics
subtitle: Booleans

- <pre  class="prettyprint" data-lang="python">
    >>> mybool = (True or False) | (True and True)
    >>> print mybool
    True
    >>> print not mybool
    False</pre>

---
title: Language Basics
subtitle: Mappings

- <pre  class="prettyprint" data-lang="python">
    >>> mylist = [1,2,3,4]
    >>> mylist.append(5)
    >>> print mylist
    [1, 2, 3, 4, 5]
    >>> print mylist[1]
    2
    >>> print mylist[1:3]
    [2, 3]
    >>> mylist.pop(1)
    2
    >>> print mylist
    [1, 3, 4, 5]</pre>

---
title: Language Basics
subtitle: Strings

- <pre class="prettyprint" data-lang="python">
    >>> mystr = "Hello there"
    >>> print mystr
    Hello there
    >>> mystr[2]
    'l'</pre>
---
title: Language Basics
subtitle: Functions
build_lists: true

- Functions can be called all on their own
    + <pre class="prettyprint" data-lang="python">
        >>> def hello_world():
        ...     print "Hello there, World!"     
        >>> hello_world()
        Hello there, World!</pre>
- Or they can be called with arguments
    + <pre class="prettyprint" data-lang="python">
        >>> def hello(val):
        ...     print "Hello there, " + val + "!"
        >>> hello("McMaster")
        Hello there, McMaster!</pre>

---
title: Language Basics
subtitle: Control Flow
build_lists: true

- Code is composed of functions that do stuff
- These functions need to be able to organize logically
- Python comes equipped with the standard control blocks found elsewhere:
    + <pre class="prettyprint">if/elif/else, for, while</pre>
- It also comes with some unique ones:
    + <pre class="prettyprint">with</pre>

---
title: Language Basics
subtitle: Control Flow
build_lists: true

- if
    + <pre class="prettyprint" data-lang="python">
        should_i_do_it = True
        if should_i_do_it:
            print "It was done"
        else:
            print "It was not done"
      </pre>

---
title: Language Basics
subtitle: Control Flow
build_lists: true

- for
    + <pre class="prettyprint" data-lang="python">
        some_numbers = [4, 7, 2, 9]
        for num in some_numbers:
            print "Your number is " + num
      </pre>
    + <pre class="prettyprint" data-lang="python">
        for i in range(5):
            if i == 4:
                break
            else:
                continue
            print "I should never get called"
      </pre>

---
title: Language Basics
subtitle: Control Flow
build_lists: true

- while
    + <pre class="prettyprint" data-lang="python">
        my_flag = True
        while my_flag:
            result = check_something()
            if result:
                # Let's get out of here
                my_flag = False
      </pre>

---
title: Language Basics
subtitle: Control Flow
build_lists: true

- while
    + <pre class="prettyprint" data-lang="python">
        while 1:
            # Danger, this must be able to break
            wait_a_while()
            result = check_something()
            if result:
                # We're out
                break
            else:
                continue
            print "This should never get called"
      </pre>

---
title: Language Basics
subtitle: Control Flow
build_lists: true

- with
    + <pre class="prettyprint" data-lang="python">
        with open('file.txt', 'r') as f:
            line = f.readline()
            do_stuff_to_the_line(line)
            print line
      </pre>

---
title: Language Basics
subtitle: Control Flow
build_lists: true

- try / except / else / finally
    + <pre class="prettyprint" data-lang="python">
        try:
            try_something_risky()
        except SpecificException as e:
            log_the_error(e)
        except:
            log_the_error()
        else:
            success_reward()
        finally:
            run_rain_or_shine()
      </pre>

---
title: Spyder
subtitle: Let's go!
class: segue dark nobackground

---
title: Next Session
subtitle: Going with the flow
build_lists: true

Next Session:

- Classes
- Exception Handling
- Important Builtin Libraries
- Extending with other libraries
- Writing Scripts with arguments / flags


---
title: Thanks!
subtitle: Any ?'s
class: segue dark nobackground
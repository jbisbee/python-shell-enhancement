# python-default-shell-enhancement #

Just a simple python startup script that will add the following to the standard python shell:

* Standard readline history between sessions
* Basic tab completion

Yes, I do know about about alternative python shells that support these features.  I just found it
odd that the default shell didn't out of the box.

* bpython http://bpython-interpreter.org/
* iPython http://ipython.org/

### Installation ###

**1. Checkout the project**

```console
jbisbee@tacquito:~ $ cd ~/src
jbisbee@tacquito:~/src $ git clone https://github.com/jbisbee/python-default-shell-enhancement.git
```

**2. Add PYTHONSTARTUP and possibly PYTHON_HISTORY_FILE to your shell**

```bash
# .bashrc

# path the the newly checked out project. I used ~/src
export PYTHONSTARTUP='/home/jbisbee/~/src/python-default-shell-enhancement/pythonstartup.py

# PYTHON\_HISTORY\_FILE default value is "$HOME/.pythonhistory"
export PYTHON_HISTORY_FILE="/some/path/you/specify"
```

**3. Now test it out***

The default shell now has persistent history and tab completion.  Enjoy!

console```
jbisbee@beni:~$ python
Python 2.7.1 (r271:86832, Jul 31 2011, 19:30:53)
[GCC 4.2.1 (Based on Apple Inc. build 5658) (LLVM build 2335.15.00)] on darwin
Type "help", "copyright", "credits" or "license" for more information.
Interactive mode history and tab completion are enabled.
>>> sys.[--TAB--]
sys.__class__(              sys.__delattr__(            sys.__dict__
sys.__displayhook__(        sys.__doc__                 sys.__egginsert
sys.__excepthook__(         sys.__format__(             sys.__getattribute__(
sys.__hash__(               sys.__init__(               sys.__name__
sys.__new__(                sys.__package__             sys.__plen
sys.__reduce__(             sys.__reduce_ex__(          sys.__repr__(
sys.__setattr__(            sys.__sizeof__(             sys.__stderr__
sys.__stdin__               sys.__stdout__              sys.__str__(
sys.__subclasshook__(       sys._clear_type_cache(      sys._current_frames(
sys._getframe(              sys.api_version             sys.argv
sys.builtin_module_names    sys.byteorder               sys.call_tracing(
sys.callstats(              sys.copyright               sys.displayhook(
sys.dont_write_bytecode     sys.exc_clear(              sys.exc_info(
sys.exc_type                sys.excepthook(             sys.exec_prefix
sys.executable              sys.exit(                   sys.exitfunc(
sys.flags                   sys.float_info              sys.float_repr_style
sys.getcheckinterval(       sys.getdefaultencoding(     sys.getdlopenflags(
sys.getfilesystemencoding(  sys.getprofile(             sys.getrecursionlimit(
sys.getrefcount(            sys.getsizeof(              sys.gettrace(
sys.hexversion              sys.long_info               sys.maxint
sys.maxsize                 sys.maxunicode              sys.meta_path
sys.modules                 sys.path                    sys.path_hooks
sys.path_importer_cache     sys.platform                sys.prefix
sys.ps1                     sys.ps2                     sys.py3kwarning
sys.setcheckinterval(       sys.setdlopenflags(         sys.setprofile(
sys.setrecursionlimit(      sys.settrace(               sys.stderr
sys.stdin                   sys.stdout                  sys.subversion
sys.version                 sys.version_info            sys.warnoptions
>>> sys.
```

### Acknowledgements ###

Thanks to Geoff Ford for the orignal code I took from his blog post.
http://geoffford.wordpress.com/2009/01/20/python-repl-enhancement/

### Authors ###

* **Jeff Bisbee**
* **Geoff Ford**

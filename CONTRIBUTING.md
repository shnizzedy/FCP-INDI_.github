# Contributing Guide 

[C-PAC Contributor Guide](https://docs.google.com/document/d/1IqXM_iaQRxYkByyeXIub-suMZdLrg-103_jKShnK0X0/edit?usp=sharing)

## Changelog

The CHANGELOG file is intended to be a human-readlable summary of changes to the codebase. The Git commit log is a fuller picture and need not be replicated in the changelog. Generally, you should add or update approximately one line in the "Unreleased" section per pull request, but depending on the scope of a pull request, you may need to add or update more than one line, or nothing at all.  

# C-PAC Coding Standard

## General Principles

### Documentation 

C-PAC documentation [\(1\)](#ref1) is ordered by quickstart, data config, pipeline config and preprocessing steps. For each new feature, GUI page, config parameter, potential values and description need to be updated correspondingly.

### Workflow

We use the git-flow workflow [\(2](#ref2), [3\)](#ref3) for version control in our version-controlled repositories.

![git-flow workflow flowchart](https://nvie.com/img/git-model@2x.png) [(2)](#ref2)

## Naming Conventions

- Follow numpy doc docstring [\(4\)](#ref4) naming conventions. The name of a variable/function should indicate its properties and functionalities clearly.

### Classes
- Class names follow the Python CapWords convention [\(5\)](#ref5) like `Strategy`, `VolumeDataset`.

### Global variables and constants
- Global variable names and names of constants use letters in uppercase connected by underscore like `UPPER_CASE_WITH_UNDERSCORES`.

### Local variables
- Local variables use letters in lowercase connected by underscore (snake_case [\(6\)](#ref6)). Note that some camelCasing parameters in pipeline config .yml file will be transferred to snake_case ultimately
- Variable names are nominal phrases.

### Class instances
- The name of an object includes an abbreviation of the object's class with the following abbreviations in place:
   - `wf`: a workflow object
   - `strat`: a strategy object
- Variables for preprocessing start with `anat` or `func` to differentiate anatomical or functional.

### Functions and methods
- Functions and methods use letters in lowercase connected by underscore (snake_case [\(6\)](#ref6)).
- Function and method names are verbal phrases like `connect_func_preproc()`, or nominal phrases for workflow functions like `slice_timing_wf()`.

## Error return handling and exceptions

- Check if input arguments are valid at the beginning of a function; if not, raise an error message specifying expected input options and current input.
- Check and handle potential errors whenever anticipated or discovered through usage.

## Code Commenting

- Use numpy doc docstrings [\(4\)](#ref4) in class and function definitions.
- Annotate the intended function of blocks of code.
- Add annotations where code is not self-explanatory.
- Remove unnecessary comments (e.g., commented-out code, pseudocode) when finalizing the code.

### Function

When a function is defined, there should be a comment block [\(4\)](#ref4) to describe the purpose of the function, its input parameters and return or yield types [\(7\)](#ref7). Notes, references and examples [\(7\)](#ref7) are optional.

#### Parameters
```Python
Parameters
----------
x : type
    Description of parameter `x`.
```
#### Returns / Yields
```Python
Returns
-------
int
    Description of anonymous integer return value.
```
```Python
Returns
-------
err_code : int
    Non-zero value indicates error code, or zero on success.
err_msg : str or None
    Human readable error message, or None on success.
```
#### Notes
- workflow input/output
- order of commands
#### References
#### Examples

### Workflow 
Before connecting each workflow, provide a descriptive name as a comment.
```
# Functional Image Preprocessing Workflow
workflow, strat_list = connect_func_preproc(workflow, strat_list, c)
```

## References

<span name="ref1">1.</span> The C-PAC Team. _C-PAC 1.6.2.a Beta documentation_. 2012 ‒ 2020. Available from: https://fcp-indi.github.io/docs/user/ ©

<span name="ref2">2.</span> Driessen V. A successful Git branching model. _nvie_. 2010. Available from: http://nvie.com/posts/a-successful-git-branching-model/ <a rel="license" href="http://creativecommons.org/licenses/by-sa/3.0/">![Creative Commons License BY-SA 3.0](https://i.creativecommons.org/l/by-sa/3.0/80x15.png)</a>

<span name="ref3">3.</span> Atlassian. Gitflow Workflow. _Atlassian Bitbucket Tutorials_. https://www.atlassian.com/git/tutorials/comparing-workflows/gitflow-workflow <a rel="license" href="http://creativecommons.org/licenses/by/2.5/au/">![Creative Commons License BY 2.5 AU](https://i.creativecommons.org/l/by/2.5/80x15.png)</a>

<span name="ref4">4.</span> numpydoc maintainers. Docstring Standard. numpydoc docstring guide. _numpydoc v1.2.dev0 Manual_. 2019 ‒ 2020. Available from: https://numpydoc.readthedocs.io/en/latest/format.html#docstring-standard ©

<span name="ref5">5.</span> Python Software Foundation. Class Names. PEP 8 -- Style Guide for Python Code. _Python Developer's Guide_. 2001 ‒ 2020. Available from: https://www.python.org/dev/peps/pep-0008/#class-names ©

<span name="ref6">6.</span> Wikipedia contributors. Snake case. _Wikipedia, The Free Encyclopedia_. 2020. Available from: https://en.wikipedia.org/w/index.php?title=Snake_case&oldid=964655840 <a rel="license" href="http://creativecommons.org/licenses/by-sa/3.0/">![Creative Commons License BY-SA 3.0](https://i.creativecommons.org/l/by-sa/3.0/80x15.png)</a>

<span name="ref7">7.</span> numpydoc maintainers. Sections. numpydoc docstring guide. _numpydoc v1.2.dev0 Manual_. 2019 ‒ 2020. Available from: https://numpydoc.readthedocs.io/en/latest/format.html#sections ©

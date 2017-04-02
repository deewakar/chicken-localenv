Introduction
------------

*localenv* creates a local CHICKEN scheme installation. It creates an alternative repository without polluting the system-wide repository.

In other words, it provides some of the features of *virtualenv* command for CHICKEN.

Installation
------------

Clone this repository and put the *localenv* script inside a directory included in your $PATH environment variable, e.g. a ~/bin folder.


Usage
-----

Create a local CHICKEN installation with the following.(let's call it sicp)


```$ localenv sicp ```


Activate the localenv with:


```$ . sicp/bin/activate ```


Install a new egg in the localenv with:


```$ chicken-install sicp ```


Check installed eggs in the localenv with:


```$ chicken-status ```


Deactivate localenv with:


```$ deactivate ```


Modify the .csirc file in your home folder as follows:

```scheme

(define local-csirc (get-environment-variable "LOCAL_CSIRC"))

(cond-expand
  (localenv

    (when (file-exists? local-csirc)(load local-csirc)))

  (else

   ;; put usual .csirc stuff here
))

```


localenv specific config should be written to *localenv_dir*/.init file.  For example, to load the sicp module at startup, include the following line inside sicp/.init file:


```scheme
(use sicp)
```


Notes
-----

* Tested on linux only

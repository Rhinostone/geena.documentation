Installing, updating or downgrading Geena
------------------------------------
------------------------------------


Thank you for your interest

Requirements
-----------

You need:

* [Node.js](http://nodejs.org/) v0.10.15+, [npm](https://npmjs.org/)
* Linux, Mac Os X or Windows
* 32-bit or 64-bit processor
* [Git](http://git-scm.com/) (latest if possible) or not...


From here, you have 2 different ways of installing Geena:

- thru **npm** (Node Package manager) - the easy way !
- or thru GitHub

Now you are ready to go ! Yeah... just ignore the next lines.


Without Git (Thanks to npm !)
----------------------

### Installing

Your are using svn or no scm at all, no problemo !

Open your terminal, and create a new project:

```
$ mkdir my_project
```

```
$ cd my_project
```

If you are looking for the last stable version, just hit:

```
$ npm install geena
```

Now you shoud be good to go. If not, check troubleshooting section down
this page.


## Updating

Once you have installed Geena,  you can get latest version of the
framework when they are available.

Let's say your current version is 1.0.0 and you want to get the 1.0.2.

Make sure you are still in your project path then, edit your
package.json by changing the version number for geena.
Once you've changes it, hit:

```
$ npm update geena
```

## Downgrading
You will need to reinstall using the version number you are targeting.

First, remove geena.

```
$ npm remove geena
```

Now reinstall. Let's say I want to go back to the v1.0.0,

```
$ npm install geena@1.0.0
```

With Git now
-----------

### Installing


Open your terminal, and create a new project:

```
$ mkdir my_project
```

```
$ cd my_project
```

If you are looking for the last stable version, just hit:

Dowloand the latest installer script and rename it ```geena```

```
$ curl -o geena
https://raw.github.com/Rhinostone/geena/master/core/template/command/geena.tpl
```
then

```
$ geena --install
```

## Updating

Once you have installed Geena,  you can get latest version of the
framework when they are available.

Let's say your current version is 1.0.0 and you want to get the 1.0.2.

Make sure you are still in your project path then hit:

```
$ geena --update 1.0.2
```

## Downgrading

Just use the same exact command. Let's say I want to go back to the v1.0.0,

```
$ geena --update 1.0.0
```

Now you are ready to go !

Troubleshooting
--------------

Well, it's not perfect yet. If for a reason or another you can't
complete the installation using Geena Installer, try to find out if the
following answer can help solving the problems you might encounter while
trying to install.

### I can't install with npm

 **Are** you behind a proxy ?

It might be some proxy problems. Check on this
[link](https://github.com/isaacs/npm/issues/1850)


### I can't install or update thru GitHub

Use ```https``` instead of ```ssh```for your remote origins and you
should be fine.

NB.: Now if you are installing with git and you decide to use
```https```mode, it would be nice to tell the Geena Installer.

If you don't have a package.json yet, It might be time to create one. If
you do have one, just edit it by adding the ```submodules``` section
with the key ```use_https```.

```
"submodules": {
      "use_https" : true
 }
```

**Were** you behind a proxy ?

```
fatal: unable to access 'https://github.com/Rhinostone/geena.git/':
Failed connect to github.com:80; Operation timed out
```
If you getting this message, I guess it's a yes.

Now that you are not any more behind one, There is 2 choices
1. Remove the proxy form your network connection
2. Change your git remote origin












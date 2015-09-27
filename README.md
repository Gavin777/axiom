# axiom
<!---
Everything you need to get started with PiE software development.
-->
axiom is an attempt to standardize a development environment for all things PiE software. In just a
few simple steps, you too can begin hacking away at your first PiE-related project!

## Uhhh...sure, but what is it?
The axiom environment is a vagrant machine provided by virtualbox that comes complete with all
dependencies necessary for every project in the PiE software stack. If all of these terms sound
like mindless techno-babble to you, they essentially mean that installing a few programs
(two, to be exact) and running few commands is enough to set up your system so you never have to
worry about installing anything ever again, at least when it comes to doing PiE related work.

## Installation
##### Dependencies

We use virtualbox as our vagrant provider, so head on over to their
<a href="https://www.virtualbox.org/wiki/Downloads">website</a>
and install the correct version for your operating system (the newest version is fine).

Note: You'll need to install Virtualbox *and* the extension pack.

You'll also need to have vagrant installed on your machine. This also should be relatively simple. Either
install it using your favorite package manager, or make your way down to
http://www.vagrantup.com/downloads and download/run the correct installer for your OS.

##### *Actually* installing things
Done? Good. Clone this repo into a directory of choice,
```
cd path/to/somewhere # replace this path with wherever you want to place your PiE-related stuff.
git clone git@github.com:pioneers/axiom.git
```
cd into the directory that you just cloned
```
cd axiom
```
and run `./setup.sh`.

After `./setup.sh` finishes, run `vagrant up`. Expect this command to
take awhile to finish, so find something fun to do and come back in 10-20 minutes.

If you're not familiar with git or have no idea what "clone this repo" or "cd into..." means, don't
be scared to ask a fellow PiE staff member for a bit of help.

After `vagrant up` completes, run `vagrant ssh`
to ssh into your shiny, new dev VM.
&nbsp;

That's it, you're good to go! Ask your PM about how to start contributing!

## Other stuff
- You can access files on your VM by opening up your file browser of choice (Windows Explorer,
  Finder, etc.) and navigating to `smb://10.31.3.14/vagrant`. Doing this, it's possible to edit code
  on your local machine and use the VM to build / compile your code.
- run `vagrant halt` in the directory with your Vagrantfile when you're done working. This will shut
  down the Vagrant VM until next time.
- unsurprisingly, `vagrant up` can be used to restart Vagrant when you decide to get back to work.
- look out for vagrant occasionally yelling at you to update your VM with
  `vagrant box update`

# Hermes, the firmware messenger
**This program is an active work in progress!**

Ever look at `/lib/firmware` and think to yourself, "there's so much useless crap in here"? Look no further than Hermes himself.

Hermes is meant to serve as a drop-in replacement for the firmware packages provided by Linux distributions. Rather than drop a load of files your machine won't use, Hermes fetches the latest firmware files from the Linux firmware tree and cherry-picks those that it is certain your PC absolutely needs to run properly. This promotes minimalism and preserves disk space, getting rid of the unnecessary garbage.

**Requirements**

Hermes requires a modern version of Python 3 and the `termcolor` Python module.

**Installation**

To install Hermes to the system, simply run setup.py. PyInstaller is necessary for the script to work properly.

**Usage**

To run Hermes and start the firmware process on a currently active system, simply run `hermes`.

To use Hermes on a mounted guest system (such as from an installation environment):

`hermes --target-system=<mount_location>`

To tell Hermes to use a specific firmware tarball (indicated by date):

`hermes --fw-date=<unix_date>`

More options can be accessed by running `hermes --help`.

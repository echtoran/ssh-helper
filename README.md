# ssh-helper

A helper script for using ssh-copy-id and ssh together.

## About ##

ssh-helper is a simple bash script designed to be a wrapper for both ssh and
ssh-copy-id, usable as an alias for ssh.  When you connect to a new host, i.e.
one that is not already in your known_hosts file, it will invoke ssh-copy-id
first, allowing you to automatically install your private key on the remote
server.  When connecting to hosts that are already in your known_hosts file,
only ssh will be executed.

ssh-helper depends upon bash-completion, meaning that you must have it
installed prior to using.  The dependancy on bash-completion is how the script
knows what's in your known_hosts file.  This will be changed in the future to
include that logic within the script itself.

Currently, this only works on Mac OS, but can be easily be modified by simply
changing a few paths in the script.

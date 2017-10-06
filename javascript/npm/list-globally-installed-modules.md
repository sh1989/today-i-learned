# List Globally Installed Modules

It's possible to see what your globally installed npm modules are, alongside their versions and the directory they're all installed to, using: `npm list -g --depth=0`.

The `depth` option can be changed to see the dependencies of each of your global modules, but as you increase this it takes longer to compute.

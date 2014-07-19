The following packages needed some minor fixes, mainly to make
.cmxs generation go away.

* ocamlfind.1.5.1 - fix HAVE_NATDYNLINK for bytes package
* cmdliner.0.9.5 - disable natdynlink in opam files
* dyntype.0.9.0 - released version is old, use git with specific hash
* lwt.2.4.5 - manually install base-unix and base-threads firsts (why?)
* optcomp.1.6 - didnt work...then did...very odd
* xmlm.1.2.0 - fix pkg-build to take natdynlink option
* conduit-0.5.0 - disable generation of cmxs 
* uutf.0.9.3 - fix pkg-build to take natdynlink option
* mirage-console-unix - disable generation of cmxs 

The following packages are also modified.  The changes here are not going to be minor
so the projects have been forked and we're working off a kfreebsd branch.

* mirage-platform - add kfreebsd backend
* mirage - got compiling (use byte code), need to add kfreebsd build stuff

For testing/porting I am trying to get the older mirari package to build.
This is so I can see what needs to be done to port it to mirage proper.
The following have also been patched, therefore, even though they are
out of date.

* mirage-net-direct - various build fixes and disable .cmxs
* mirari - build against latest world, bytecode only, uses pgj fork

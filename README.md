Rat Spaces
==========
 
Author: Daniel Noland (daniel.noland+ratspaces@gmail.com)

(I am most easily contacted via +Daniel Noland on Google +)

This is a simple hack which helps me stomach the Ratpoison window
manager's workspaces functionality, and generally aids in the
manipulation of ratpoison windows.  I hope it is useful to someone
else. 

Usage
-----

The script is entirely self contained and requires only that you have
ratpoison running (obviously).  The script can be called from the
command line, but it is MUCH more effective to bind it to hot keys in
your .ratpoisonrc file.

The script accepts the following arguments:

*scan*
This displays a summary of all the windows in all the active workspaces.
Like the built in 'windows' command, it places an \* next to the active
window.  It also wraps the name of the active workspace with \*'s.

*inc*
Move to the next workspace. That is increment the workspace.

*dec*
Move to the previous workspace. That is decrement the workspace.

*sendn*
Send the current window to the next workspace.

*sendp*
Send the current window to the previous workspace.

*follown*
Send the current window to the previous workspace. Also, move to the
next workspace.  That is, follow to the next workspace.

*followp*
Send the current window to the previous workspace. Also, move to the
previous workspace.  That is, follow to the previous workspace.

*swap*
Swap the current window with the first selected window on the next
monitor.  This is especially useful if you only have two monitors (which
I suspect covers most of us).

Example 
-------

You could (if you are like me) configure your .ratpoisonrc like so:

    bind w ecec ratSpaces.sh scan
    bind comma exec ratSpaces.sh dec
    bind period exec ratSpaces.sh inc
    bind greater exec ratSpaces.sh sendn
    bind less exec ratSpaces.sh sendp
    bind C-period exec ratSpaces.sh follown
    bind C-comma exec ratSpaces.sh followp
    bind slash exec ratSpaces.sh swap

Then simply add the ratSpaces.sh script to your PATH and start
experimenting.

License
-------

I am putting this up under the MIT License.  See the LICENSE document
for the full text of that license.

RatSpaces
=========

This is a simple hack which helps me stomach the Ratpoison window manager's workspaces functionality, and generally aids in the manipulation of ratpoison windows.  I hope it is useful to someone else. 

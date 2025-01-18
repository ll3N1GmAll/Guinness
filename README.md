# Guinness

Ever find yourself having to write a quick bash script to run, yet another, *new* tool against a long list of targets in an engagement? Of course you have. All the time..
Well, no more!
Now, you can just sit back and have yourself a Guinness!

Guinness is a *very* simple tool wrapper script for the endless number of simple scanners, PoC scripts, new attack tools, etc. that you have to deal with on a daily basis. Simply drop all your targets in an empty text file, one per line, then enter the first part of the command into the interface when Guinness asks you for it. Next, enter the rest of the command, after the target paramter, when Guinness asks you for that. Dead simple.

Genius? Nope, Guinness. :) 

# How To

This tool will take any tool or script you want to use, and will launch it against a list of targets that you provide in ``targets.txt``. 
Simply enter in the first part of the command, up to the parameter where you enter in your target, like this: ``nuclei-u``. Here the ``-u`` is wher you enter the URL you are targeting. So, you input ``nuclei -u``; but you leave out any actual target. Then hit enter and Guinness will ask you for the rest of the command. Here you enter the remainder of the command as though you had just entered in the target. To keep with the same example you would enter ``-t /home/user/nuclei/cmd/nuclei/cmd/nuclei/ProxyShell/proxyshell.yaml``. This runs the nuclei scanner, checking for the ProxyShell vuln, against a list of URLs that you would enter, one per line, into the ``targets.txt`` file.

To use Guinness with a tool that is not in a location in you system's PATH, or that is not installed system-wide, you simply enter the path at the beginning of the command when it asks you for the first part of the command, like so: ``/home/user/impacket-fortra/examples/GetUserSPNs.py``.

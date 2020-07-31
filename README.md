# MAUDE-CPS
Maude specification of car assembly CPS case study. In paper submitted to IEEE CPSCAPP @ IEEE AICCSA 2020 (submission 145)

This repository contains the Maude implementation presented in the paper.


The file "spec.maude" contains the CPS-SPEC functional module.
The file "behavior.maude" containts the CPS-BEH functional module.

In order to execute / simulate or simply play with the model, it is necessary to first install Maude.


---Maude installation---

This has been tested on Ubuntu 16.04, 18.02 and 20.04 versions.
Go to terminal : type "sudo apt install maude" then follow steps (Maude 2.7 version should be installed)



---Running Maude---

Once installed, simply run Maude by typing the "maude" command on the terminal.
This should appear : 

		     \||||||||||||||||||/
		   --- Welcome to Maude ---
		     /||||||||||||||||||\
	    Maude 2.7
	    Copyright 1997-2014 SRI International


---Compiling the specification---

Once maude running, the provided .maude files need to be loaded for compilation.
Type the following commands in the right order :
1- load *path*/spec.maude
2- load *path*/behavior.maude
*path* being the path of the folder containing both files.



---Running the model---

* To reproduce the presented simulation results, type the following command :

        search INIT =>* s:SYS such that isComplete(s:SYS) .  
        
[Don't forget the space and the dot, otherwise it won't work !)]
All 24 solutions and the complete path should be displayed.

* you can also simulate the execution to show one single path by using the following command :

        rewrite INIT .

For more details about the Maude language itself or the different commands, here is the official Maude documentation : http://maude.cs.illinois.edu/w/images/e/e0/Maude-2.7.1-manual.pdf


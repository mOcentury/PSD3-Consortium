PSD3 Consortium Sprint 1 - Implementation
=============
## Importing the project into Eclipse

1. Download zip folder and unzip
2. Import project to Eclipse as "General > Existing Projects into Workspace"
3. Select the root directory that u have unzip the project
4. Check "Copy projects into workspace" and click on "Finish"
5. From Terminal/Cygwin change directory to the project in your workspace and use the following command
  * ant resolve – Generate library required from build.xml
6. Go back to Eclipse
  * Configure your build path to include all the jar files in to the project
7. You are done importing and setting up the projects!

---

## Generate file for installation
1. 	After creating component, please edit the manifest folder and make sure that in bundles, you have already added your component so that your .jar file is being created. 

2. 	DO NOT DELETE THE build.xml FILE! 
	The build.xml is like your makefile. While running 'ant run' function, it will run 3 command all together.

		1. ant osgi.init
		2. ant osgi.run
		3. ant bundles

3. 	I've already added the bundles in so that it the stuff can be easily edited. The folder has already been 			customised that as long as you import this folder in, you can go into your cygwin/terminal and run 'ant 		resolve' and 'ant run'. PLEASE also remember that if you are running on Eclipse, you will need to add 			reference library too, if not you will face a lot of error. 

	As for running, install the file and start the bundle in the following sequence:

		install file:Attendance.jar
		install file:Course.jar
		install file:UI.jar

		start <id> 
		stop <id>

4.	If you have make changes to the .java file and want to test it out, just do the following code. 

		stop 0
		ant run
		update <id> 

5.	If you have no idea what is the id you have previously, type lb to check. 
	For my component, you should see the follow result.

		install file:login.jar
			[] g! Bundle ID: 5
		start 5
        		 [] g! Got Connection
        		 [] derrick derrick
        		 [] kevin kevin
        		 [] jason jason
        		 [] ngaifong ngaifong
        		 [] reuben reuben
        		 [] joe joe
        		 [] ian ian
        		 [] gene gene
        		 [] yuanhui yuanhui
        		 [] wenbing wenbing
        		 [] jiaxiong jiaxiong
        		 [] yve yve
        		 [] jasmine jasmine
        		 [] shiny shiny
        		 [] veronica veronica
        		 [] Got Connection
        		 [] derrick derrick
        		 [] kevin kevin
        		 [] jason jason
        		 [] ngaifong ngaifong
        		 [] reuben reuben
         		 [] joe joe
         		 [] ian ian
        		 [] gene gene
        		 [] yuanhui yuanhui
        		 [] wenbing wenbing
        		 [] jiaxiong jiaxiong
        		 [] yve yve
        		 [] jasmine jasmine
        		 [] shiny shiny
        		 [] veronica veronica
		stop 5
        		 [] g! Goodbye World!!

         
-Derrick

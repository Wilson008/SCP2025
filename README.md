# EATXT: [Project Name]

**[Please refer to our User Manual for detailed instructions](User_Manual.pdf)**

# User Manual of EATXT

## Preface

This document describes how to install and use the EATXT editor. EATXT is a textual concrete syntax designed for EAST-ADL, and we have developed a matching editor for it. EAST-ADL is a domain-specific language used to describe the structure of automotive embedded systems.
In this folder, we provide EATXT in the form of source code (including its grammar definition and editor generation code). This article will introduce how to install and use it.

## Prerequisites

1.	You must have installed Eclipse and Java on your computer, **with Java version no less than 11**.

2.	EMF is installed or You use the Eclipse Modeling Tools (EATXT projects have been tested on the following versions of Eclipse Modeling Tools:21-06, 22-03, 22-06, 23-03, 23-06).

3.	You must have installed Xtext for your Eclipse (You can simply install it via Eclipse Marketplace).

## Installation and Usage

1. Download the code of projects

	a. Paste the link https://github.com/blended-modeling/eatxt into the browser and open the page.
	
	b. Log into a Github account which has been invited to the project.
	
	c. Open a terminal/shell and navigate to a folder where you would like to store the project locally.
	
	d. Type `git clone https://github.com/blended-modeling/eatxt`. The source code will now be cloned in the sub-folder `eatxt`.

2. Open the code in Eclipse
	
	a. If you do not have Eclipse installed on your system, download an Eclipse RCP from https://eclipse.org/download and install it.
	
	b. Start Eclipse and select a suitable workspace. We recommend creating a new one.
	
	c. In the `File` menu, choose `Import...`
	
	d. Select `Existing projects into workspace`
	
	e. Select the folder into which you cloned the source code 
	
	**(Once you have imported the code, you will see a lot of errors which is normal and they will be disappeared in the later steps).**
	
3. Reload the target definition
	
	a. Find the project "org.bumble.eatxt.target"
	
	b. Double click on the file "org.bumble.eatxt.target.target" to open it in the target definition editor.
	
	c. In the right-top corner, click "Set as Active Target Platform"

	This can take a couple of minutes. Afterwards, most of compilation errors should have disappeared and a few of them will still be remaining **(This is normal, and the remaining errors will be fixed in the later steps)**.

4.	Generate the EATXT editor

	a. Open the project `src/org.bumble.eatxt` folder in the `org.bumble.eatxt` project **(Please check the java version in the “Java Build Path”, and it should be no lower than 17)**.
	
	b. Right click on the `.mwe2` file and choose `Run As` -> `MWE2 workflow` from the context menu. Because Eclipse may still display a few errors at this time, you may be asked if you want to continue. Please click “Proceed”. 
	
	**(If these Java projects are using Java 11 or above in your eclipse, then you can execute this step successfully and all the errors will disappear after this step. **
	**Otherwise you may not be able to execute this step.**
	**So, please check the Build Path of each project one by one to make sure they are using Java 11 or above.)**
	
	(Once you have completed the above steps, now the editor can be generated.)

# Important reminder:

If you still get errors after completing the above steps, this is usually due to missing dependencies, and you can look for possible explanations and solutions in the Section "Common Problems" of User_Manual.pdf.

# Use the EAText editor.

Here, we will start the EATXT editor in runtime mode. The steps are as follows:

	a. Find the project `org.bumble.eatxt`.
	
	b. Right click on it and select `Run As` -> `Eclipse Application` in the context menu. A new Eclipse RCP instance starts.
	
	c. Click `Create a project` or `File` -> `Project` and create a generic project.
	
	d. Create a new file with the extension `.eatxt` in the new project. On double click, it opens in the EATXT editor.
	
	e. Alternatively, import the `org.bumble.eatxt.example` project into your runtime Eclipse RCP and we have provided two files there, i.e., example.eatxt and example.eaxml.
	
	(the project `org.bumble.eatxt.example` is in the folder “examples”)
	
You can right click on the file and click "Convert to ..." to serialize EATXT model to EAXML or the other way round.

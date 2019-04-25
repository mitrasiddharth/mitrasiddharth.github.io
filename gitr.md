---
  layout: default
---
  
  Getting Started with Github and RStudio.
-------
  
This material was created for a guest lecture.

# WHY?

Before we start - why do this?! Writing up your code in `R` packages hosted on Github can make:

* Collaboration easier;
* Using cloud-based computing more efficient and less prone to errors;
* It easier to provide reproducable code alongside journal submissions.

# Our Main Resource

Jenny Bryan's [``Happy Git and GitHub for the useR''](https://happygitwithr.com) is a great resource for setting up Github and RStudio to work together. 

## An aside re: Dropbox.

I (irresponsibly) make repositories in Dropbox folders. People on the internet will tell you that you should never do this, and honestly they are probably right. However, based on a few years of experience working this way, my opinion is that it is fine to make repositories in Dropbox folders **if you are not collaborating with anyone on the repository**. If the Dropbox folder **and** repository are shared, it will be too easy for you and your collaborators to accidentally overwrite each others' work without realizing it.


# Going Beyond Our Main Resource

Because we're focusing on the idea of using Github and RStudio to make packages, I'll talk a bit about several extra things:

* Debugging functions that you have put in a package;
* Making packages that use RCpp.


# Troubles

99% of the time, Github and RStudio work great together and everything is copacetic! However 1% of the time everything goes to hell. Some examples:

* I once tried to push a large data file to a Github repository. I then just deleted the file on my local machine and tried to commit the deletion. Unfortunately, Github insisted that in order to delete the file it had to push the file to the repository first, so this didn't help. Ultimately, I had to get into the command line to remove the original push request.

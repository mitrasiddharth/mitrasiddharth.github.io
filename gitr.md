---
  layout: default
---
  
Getting Started with Github and RStudio
-------
  
This material was created for a guest lecture, and I figured it could be useful to others so here it is!

# WHY?

Before we start - why do this?! Writing up your code in `R` packages hosted on Github can make:

* Collaboration easier 
    * Multiple people can edit the same files without overwriting each other's work without realizing it, and your collaborators can easily run your code without you having to send them all the files every time they want to use it
* Using cloud-based computing more efficient and less prone to errors 
    * No moving your code from one computer to another if you prototype code on one computer and run it elsewhere
* The submission process less painful 
    * The more work you do now, the less work you have to do later

# Our Main Resources and Basic Steps

Jenny Bryan's ["Happy Git and GitHub for the useR"](https://happygitwithr.com) is a great resource for setting up Github and RStudio to work together. Assuming you have already [installed `R` and RStudio](https://happygitwithr.com/install-r-rstudio.html#install-r-rstudio), the basic steps are:

- [Make a GitHub account](https://happygitwithr.com/github-acct.html#github-acct)
- [Make sure you have Git downloaded and installed](https://happygitwithr.com/install-git.html#install-git)
- [Introduce your GitHub account to your computer](https://happygitwithr.com/hello-git.html#hello-git)
- [Make sure you can set up a repository on your computer that connects to your Github account](https://happygitwithr.com/push-pull-github.html#push-pull-github)
- [Set things up so you don't have to enter your GitHub username and password over and over](https://happygitwithr.com/credential-caching.html#credential-caching)
- [Make sure you can set up a repository connected to your GitHub account within RStudio](https://happygitwithr.com/rstudio-git-github.html#rstudio-git-github)
    - Jenny's instructions are for one way of doing this, which starts with a Github repository. Alternatively, you could start with an `R` project or package on your computer. If you want to start with a package, you can follow the steps below:
        - Within RStudio, click *File->New Project->New Directory->R Package*
        - Give the package a name, add any `.R` files that contain functions you will want in the package, pick where you want your package to live, and check "Create a git repository"
            - You don't actually have to check "Create a git repository." If you *do not* check it, then you need to take an additional step of clicking *Tools->Version Control->Project Setup* and selecting Git as your version control software.
            - This creates a bunch of auxiliary files you'll want to have around, for instance DESCRIPTION and NAMESPACE files
        - Go to https://github.com, and make sure that you're logged in. Create a new repository with the same name as your package/project. It's up to you whether or not you want to initialize the package with a README, I usually do not and then add one manually.
        - GitHub will provide you with some instructions. Make a note of the instructions to "...push an existing repository from the command line." We'll use them shortly.
        - Go back to RStudio, where your project is hopefully open. Open the "Git" pane, which should be next to the "Environment," "History," "Connections," and "Build" panes. There is a blue gear to the right of "Diff" and "Commit." Click the gear and select "Shell."
        - Type `touch README.md` in the terminal window. This creates an empty README file.
        - Go back to RStudio and return to the "Git" pane. Check the box next to "README.md," which indicates that you would like to add it to the GitHub repository. 
        - Click "Commit" and fill in a few words in the "Commit message" box, e.g. "Initializing repository." Click the "Commit" button below the "Commit message" box.
        - Go back to the terminal window you opened to create the README, and revisit the instructions from Github to "push an existing repository from the command line." Type the Github instructions into the terminal window. If you are me and your package and repository are named `test`, you would type:
            - `git remote add origin https://github.com/maryclare/test.git`
            - `git push -u origin master`
        - You should be all set! Now you can continue working on your package and commit and push your commits as you see fit!
            

Jenny Bryan's ["Data wrangling, exploration, and analysis with `R`"](https://stat545.com/index.html) course site has some very helpful material on creating `R` packages and hosting them on GitHub including:

- [Advice on preparing your system to make `R` packages](https://stat545.com/packages01_system-prep.html)
- [Basic `R` package creation and versioning instructions](https://stat545.com/packages04_foofactors-package-01.html)
- [Additional instructions for documenting your package and its functions and installing it from GitHub](https://stat545.com/packages05_foofactors-package-02.html).



## An aside re: Dropbox.

I (irresponsibly) make repositories in Dropbox folders. People on the internet will tell you that you should never do this, and honestly they are probably right. However, based on a few years of experience working this way, my opinion is that it is fine to make repositories in Dropbox folders **if you are not collaborating with anyone on the repository**. If the Dropbox folder **and** repository are shared, it will be too easy for you and your collaborators to accidentally overwrite each others' work without realizing it.


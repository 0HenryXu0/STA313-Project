# STA313-Final-Project

Hi everyone, follow these steps to clone the project to your local RStudio environment and set up your connection so you can keep track of any changes. Note that the following procedures are written by AI, but it will work.

Step 1: Give Me Your GitHub Username (Completed by everyone i guess)

Before you do anything else, send me your GitHub username.
I need to add you as a collaborator on the repository. Once I add you, check your email or go directly to the repository link on GitHub to accept the invitation. You cannot push any work until you accept it.

Step 2: Install Git & Helper R Packages

Make sure you have Git installed on your computer. Then, open RStudio and run this command in your console to install the necessary tools:

install.packages(c("usethis", "gitcreds"))

Step 3: Introduce Yourself to Git

Run the following code in your RStudio console to tell Git who you are.
• Note: The email address must match the email you use for your GitHub account.

usethis::use_git_config(
  user.name = "Your Name", 
  user.email = "your.github.email@example.com"
)


Step 4: Generate a GitHub Personal Access Token (PAT)

GitHub does not allow you to use your regular password when logging in via RStudio. You need a secure Token instead.
1. Run this command in your RStudio console to go straight to the GitHub settings page:

usethis::create_github_token()

2. Log in to GitHub if asked.
3. Give your token a name (e.g., "STA302-Project"), leave all the pre-checked boxes exactly as they are, and click Generate token at the bottom.
4. Important: Copy the long string of letters/numbers immediately. You will never see it again.

Step 5: Save Your Token in RStudio

Go back to your RStudio console and run:

gitcreds::gitcreds_set()

When prompted in the console, paste your copied token and press Enter. RStudio will remember this so you don't have to enter it every time.

Step 6: Clone the Repository to Your Computer

Now you are ready to pull the project into your RStudio!
1. Go to our group project page on GitHub.
2. Click the green Code button and copy the HTTPS URL link.
3. Open RStudio and go to the top left menu: File > New Project...
4. Select Version Control, then select Git.
5. Paste our repository URL into the Repository URL field.
6. Choose where you want to save the project folder on your computer under "Create project as subdirectory of:".
7. Click Create Project.
The project will download, and RStudio will automatically open our STA302 Final Project environment. You will see a Git tab appear in your top-right panel.

Workflow: How We Edit & Share Work

Whenever you want to write code or update the project, follow this 4-step cycle:
1. Pull First: Before starting any work, open the project and click the Blue Down Arrow (Pull) in the Git tab. This updates your computer with the latest changes made by other group members.
2. Do Your Work: Edit your .Rmd files, write your scripts, and save your work as normal.
3. Commit: When you finish a task, go to the Git tab, check the Staged boxes next to the files you modified, click Commit, type a short note about what you changed (e.g., "Added data cleaning section"), and click Commit.
4. Push: Click the Green Up Arrow (Push) to send your updates to GitHub so the rest of the team can see them!

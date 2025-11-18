#### This project is for the Devops bootcamp exercise for 
#### "Build Tools and Package Managers" 

# Exercises for Module "Build Tools and Package Manager" 

Use repository: https://gitlab.com/twn-devops-bootcamp/latest/04-build-tools/build-tools-exercises

🔸 [EXERCISE 0: Clone project and create own Git repository]

To work with the project for the exercises:

✅ How to Clone the Provided Project and Create Your Own Git Repository

You were given this repository:
https://gitlab.com/twn-devops-bootcamp/latest/04-build-tools/build-tools-exercises

Your task:

### - Clone that project
git clone https://gitlab.com/twn-devops-bootcamp/latest/04-build-tools/build-tools-exercises
### - Move into the folder:
cd build-tools-exercises
### - Remove the Original Git History
rm -rf .git
### - Create your own project/repository using its content
git init
git add .
git commit -m "Initial commit based on build-tools-exercises"
### — Create Your Own Remote Repository

Depending on where you want your new repo:
If using GitLab
Go to GitLab ➜ “New Project”
Create an empty repository
Copy the remote URL, e.g.:

https://gitlab.com/your-username/your-new-repo.git


### - Add it as your remote:

git remote add origin https://gitlab.com/your-username/your-new-repo.git

### - Push your project:

git push -u origin main

🔸 [EXERCISE 1: Build jar artifact]

You want to deploy the artifact to share that library with all team members. So:

### - try to build the jar file
    gradle build

The Build will fail, because of a compile error in a test, so you can't build the jar.


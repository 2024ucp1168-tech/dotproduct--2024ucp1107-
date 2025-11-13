Assignment 12 - GitHub

TW Lab 2025

In today’s lab, you will learn to collaborate with peers and work on open source
software. Although, this assignment is about GitHub, the workflow remains similar
on other Git service providers such as GitLab, BitBucket etc.
Instructions
You should have already completed prior lab exercises where you wrote code for vector
dot-product. You will reuse that code in the tasks below. Follow the steps in order.
Document each step with screenshots (to be uploaded separately as a PDF).
1 Create a GitHub Account and add SSH key
1. Create an account on GitHub at https://github.com.
2. Delete all existing ssh keys from the system using:
rm ∼/.ssh/id*
3. Generate a new SSH key pair on your local machine using:
ssh-keygen -t ed25519 -C "rollno@mnit.ac.in"
4. Copy your public key from ∼/.ssh/id ed25519.pub and add it to GitHub under:
Settings → SSH and GPG Keys → New SSH Key.
2 Create a new repository for code and clone it
1. On GitHub, create a new public repository named: dotproduct-<rollno>.
2. Do not opt to add a README or .gitignore.
3. In a separate folder, clone the repository to your machine using SSH (not
HTTPS):
git clone git@github.com:<your-username>/dotproduct-<rollno>.git

1

3 Make changes and push to GitHub
1. Use git remote -v to list all configured remotes. Also observe the output of git
branch -a.
2. Copy your existing vector addition code from previous labs into this repository.
3. Create a file named README.md describing the purpose of your program.
4. Commit both the files.
5. Then run the following command:
git push origin master

4 Fork a friend’s repository, clone it, modify, push,
and create a PR
1. Ask a friend to share the URL of their GitHub repository.
2. On GitHub, click “Fork” to create your own copy of their code.
3. On your local machine, create a new folder and inside that, clone your fork:
git clone git@github.com:<your-username>/<friend-repo-name>.git

4. Make a small modification to your friend’s vector addition code.
5. Commit and push the change to your fork:
git push origin master

6. On GitHub, open a Pull Request (PR) from your fork to your friend’s original
repository.
5 Merge your friend’s PR and update your local
repository
Meanwhile, your friend must have created a Pull Request on your repository.
1. Go to your repository on GitHub.
2. Under Pull Requests, find your friend’s request and merge it.
3. Verify that all your friend’s commits are visible.

2

6 Update your local repository
1. Return to your own repository’s local clone.
2. Pull the changes made by your friend that you just merged on GitHub.

git pull origin master

3. Resolve merge conflicts if they occur.
7 A real-world GitHub project: TeXstudio
To understand how open-source software development works in real-world, explore the
GitHub repository of the TeXstudio project: https://github.com/texstudio-org/texstudio
1. Inspect the commit history to observe coding conventions, commit message styles,
and contribution patterns.
2. Examine open Pull Requests (PRs) to see how contributors propose changes and
how maintainers review them.
3. Review open and closed issues to understand how bugs and feature discussions are
tracked.
4. Browse the branch structure to understand how release workflows are managed.
5. Read the project’s developer guidelines under the Contribute section.
This will provide a realistic picture of how large open-source projects operate and how
you can begin contributing to them.
Submission Requirements

• Add a link to your own repository and another link to the Pull Request you sub-
mitted to your friend in the document that you create.

• A PDF containing screenshots of each major step.

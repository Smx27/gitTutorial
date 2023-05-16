# Basic and advance git command 
## Basic Git Commands Tutorial

Git is a version control system that allows you to track changes and collaborate on projects efficiently. This tutorial will guide you through some of the most commonly used Git commands.

### Initialize a Repository

To start using Git in your project, you need to initialize a Git repository. Follow these steps:

1. Open your terminal or command prompt.

2. Navigate to the project directory using the `cd` command:

   ```bash
   cd /path/to/your/project
   ```

3. Initialize a Git repository using the following command:

   ```bash
   git init
   ```

### Track Changes

Git allows you to track changes made to your project files. Here's how you can track changes and commit them:

1. Add files to the staging area using the `git add` command:

   ```bash
   git add file1.txt file2.txt
   ```

   This command stages `file1.txt` and `file2.txt` for the next commit.

2. Commit the changes to the repository using the `git commit` command:

   ```bash
   git commit -m "Add file1.txt and file2.txt"
   ```

   The commit message should be descriptive, indicating the changes made in the commit.

### Check Repository Status

You can check the status of your repository to see which files are modified or staged. Use the following command:

```bash
git status
```

Git will display the current status of your repository.

### View Commit History

To view the commit history of your repository, use the `git log` command:

```bash
git log
```

Git will display a list of commits, including the commit hash, author, date, and commit message.

### Create and Switch Branches

Branches allow you to work on different features or versions of your project. Here's how you can create and switch branches:

1. Create a new branch using the `git branch` command:

   ```bash
   git branch new-feature
   ```

   This command creates a new branch named "new-feature" based on the current branch.

2. Switch to the new branch using the `git checkout` command:

   ```bash
   git checkout new-feature
   ```

   You are now working on the "new-feature" branch.

### Merge Branches

Once you have made changes on a branch and want to incorporate them into another branch, you can merge branches. Follow these steps:

1. Switch to the branch where you want to merge changes:

   ```bash
   git checkout main
   ```

2. Merge the branch you want to merge into the current branch:

   ```bash
   git merge new-feature
   ```

   This command merges the "new-feature" branch into the current branch.

### Push and Pull Changes

To collaborate with others or sync your local repository with a remote repository, you need to push and pull changes. Here's how:

1. Push local changes to a remote repository using the `git push` command:

   ```bash
   git push origin main
   ```

   This command pushes the changes in the current branch to the "main" branch of the remote repository.

2. Pull changes from a remote repository using the `git pull` command:

   ```bash
   git pull origin main
   ```

   This command pulls the latest changes from the "main" branch of the remote repository into your current branch.

### Conclusion

This tutorial covered some of the basic Git commands to get you started with version control in your projects. Git offers many more features and commands for managing your codebase. To learn more, refer to the official Git documentation or explore advanced Git tutorials


## Advanced Git Tutorial

In this advanced Git tutorial, we'll explore some powerful commands and concepts to enhance your Git workflow.

### Garbage Collection and Pruning

Git's garbage collection (GC) is responsible for cleaning up unnecessary data and optimizing repository performance. You can manually trigger GC and prune unused objects using the following command:

```bash
git gc --prune=now
```

This command forces an immediate garbage collection and prunes all unreferenced objects in the repository.

### Git Rebase

Git rebase allows you to apply changes from one branch onto another, providing a cleaner commit history. Follow these steps to rebase a branch:

1. Switch to the branch where you want to apply changes:

   ```bash
   git checkout target-branch
   ```

2. Rebase the branch containing changes onto the target branch:

   ```bash
   git rebase source-branch
   ```

   This command applies the commits from `source-branch` onto `target-branch`.

### Git Cherry-Pick

Git cherry-pick allows you to pick specific commits from one branch and apply them to another branch. Use the following steps to cherry-pick a commit:

1. Switch to the branch where you want to apply the commit:

   ```bash
   git checkout target-branch
   ```

2. Cherry-pick the desired commit:

   ```bash
   git cherry-pick commit-hash
   ```

   Replace `commit-hash` with the hash of the commit you want to cherry-pick.

### Git Reset

Git reset allows you to move the current branch to a specific commit, discarding subsequent commits. Here's how you can use it:

1. Identify the commit you want to reset to using `git log`.

2. Perform a soft reset to move the branch pointer to the desired commit:

   ```bash
   git reset --soft commit-hash
   ```

   The `--soft` option keeps the changes from the discarded commits as uncommitted changes.

### Git Stash

Git stash allows you to temporarily save changes that you don't want to commit immediately. Follow these steps to stash changes:

1. Stash your changes:

   ```bash
   git stash save "Stash message"
   ```

   Replace `"Stash message"` with a descriptive message for the stash.

2. Apply the stashed changes:

   ```bash
   git stash apply
   ```

   This command applies the most recent stash.

### Git Submodules

Git submodules enable you to include external repositories within your project. To add a submodule:

```bash
git submodule add repository-url
```

Replace `repository-url` with the URL of the external repository.

To update submodules after cloning or pulling changes:

```bash
git submodule update --init --recursive
```

This command fetches the latest commits from the submodule repositories.

### Git Worktree

Git worktree allows you to work on multiple branches simultaneously in separate working directories. Here's how to create a new worktree:

```bash
git worktree add <path> <branch-name>
```

Replace `<path>` with the directory path where you want to create the worktree, and `<branch-name>` with the name of the branch you want to work on.

### Git Hooks

Git hooks are scripts that run before or after specific Git events. You can use them to automate tasks or enforce project-specific rules. Hooks reside in the `.git/hooks` directory of your repository.

To create a hook, add an executable script with the appropriate name (e.g., `pre-commit`, `post-merge`) to the hooks directory.

### Conclusion

This advanced Git tutorial covered additional Git

 commands and concepts to further improve your version control workflow. Experiment with these commands and explore the Git documentation to discover even more features and capabilities of Git.

### Git Branching Strategies

Explore different branching strategies that can improve collaboration and code management in larger projects. Some popular branching strategies include:

- Feature Branching: Creating separate branches for each feature or task.
- GitFlow: A branching model that emphasizes release management.
- Forking Workflow: Each contributor maintains their own fork of the repository.

Discuss the benefits and considerations of each strategy and how to effectively use them.

### Git Aliases

Introduce Git aliases, which allow you to create shortcuts for frequently used Git commands. Show examples of creating aliases for common commands like `status`, `commit`, and `log`. Explain how to set up global or project-specific aliases.

### Git Bisect

Demonstrate the `git bisect` command, which helps identify the specific commit that introduced a bug or regression. Explain how to use `git bisect` to perform a binary search through the commit history to pinpoint the problematic commit.

### Git Hooks

Cover different types of Git hooks, including pre-commit, pre-push, and post-commit hooks. Explain how to write custom scripts for these hooks to automate tasks like code linting, testing, and documentation generation.

### Git Subtree

Discuss the `git subtree` command, which allows you to incorporate external repositories into your project as a subtree. Explain how to add, update, and manage subtrees, and the benefits of using this approach for including external code.

### Git Revert and Reset

Explain the difference between `git revert` and `git reset` commands. Show examples of reverting commits using both commands and discuss when to use each approach based on the requirements of the situation.

### Git Reflog

Introduce the `git reflog` command, which shows a log of all reference changes, including branch checkouts and resets. Explain how `git reflog` can be useful for recovering lost commits or branches.

### Git Workflows with CI/CD

Discuss integrating Git workflows with Continuous Integration/Continuous Deployment (CI/CD) systems. Explain how to set up automated builds, tests, and deployments triggered by Git events like pushes or pull requests.

Certainly! Git workflows with CI/CD involve automating the build, test, and deployment processes of your codebase using Continuous Integration/Continuous Deployment (CI/CD) systems. This ensures that changes made to your Git repository are automatically built, tested, and deployed in a controlled and efficient manner. Here's an explanation with an example and code snippets:

## Git Workflow with CI/CD

1. **Continuous Integration (CI):** CI focuses on integrating code changes from multiple contributors into a shared repository. It ensures that the codebase is always in a functional state by automatically building and testing changes. Here's an example workflow:

   - Developers work on feature branches and push their changes to a shared Git repository.
   - The CI system detects the new changes and triggers a build process.
   - The build process compiles the code, runs tests, and performs static code analysis.
   - If the build and tests pass, the changes are considered valid and ready for further steps. Otherwise, the CI system reports the issues for developers to fix.

2. **Continuous Deployment (CD):** CD focuses on automating the deployment of code changes to production or staging environments. It allows you to release software more frequently and reliably. Here's an example workflow:

   - When changes are merged into a specific branch (e.g., `main` or `release` branch), the CD system detects the updates.
   - The CD system pulls the latest changes and triggers the deployment process.
   - Deployment steps can include tasks such as building artifacts, running additional tests, creating container images, or deploying to servers or cloud platforms.
   - If all deployment steps are successful, the new version of the software is deployed to the target environment, ensuring a seamless release process.

## Example CI/CD Configuration

Let's consider an example using popular CI/CD tools, such as GitHub Actions and Docker, to demonstrate a basic CI/CD configuration for a web application.

1. Create a `.github/workflows/ci-cd.yml` file in your Git repository to define the CI/CD workflow:

   ```yaml
   name: CI/CD Pipeline

   on:
     push:
       branches:
         - main

   jobs:
     build:
       runs-on: ubuntu-latest

       steps:
         - name: Checkout code
           uses: actions/checkout@v2

         - name: Build and test
           run: |
             # Build steps
             npm install
             npm run build

             # Test steps
             npm run test

     deploy:
       needs: build
       runs-on: ubuntu-latest

       steps:
         - name: Checkout code
           uses: actions/checkout@v2

         - name: Build and push Docker image
           uses: docker/build-push-action@v2
           with:
             context: .
             push: true
             tags: your-docker-repo/image-name:latest

         - name: Deploy to server
           run: |
             # SSH into server and pull the latest Docker image
             ssh user@server-ip "docker-compose pull && docker-compose up -d"
   ```

2. In the above example, the workflow is triggered on pushes to the `main` branch.
3. The workflow consists of two jobs: `build` and `deploy`.
4. The `build` job checks out the code, builds the application, and runs tests.
5. The `deploy` job, which depends on the `build` job, checks out the code, builds a Docker image, pushes it to a Docker repository, and deploys it to a server using `docker-compose`.
6. Adjust the commands and steps based on your specific project requirements and environment setup.

By configuring this CI/CD workflow

, any changes pushed to the `main` branch will trigger the pipeline. The code will be built, tested, and automatically deployed to the specified server, ensuring a streamlined and automated process.

Remember to customize the workflow according to your project's specific needs, such as incorporating additional testing steps, environment-specific configurations, or notifications for build and deployment statuses.

Note: The example provided uses GitHub Actions and Docker, but there are various CI/CD tools available, such as Jenkins, GitLab CI/CD, CircleCI, and Travis CI. The specific configuration and syntax may vary depending on the chosen tool, but the underlying principles of CI/CD remain the same.

Keep in mind that CI/CD pipelines can be more complex and tailored to your project's unique requirements. The provided example serves as a starting point, and you can extend and enhance it as needed.

I hope this example helps you understand Git workflows with CI/CD and how to set up a basic configuration.

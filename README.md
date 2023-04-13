# Initialize git.

1. Go to the directory
2. Execute command: git init


# After the LOCAL git repo initialization, it is important to configure: 
1. User email
2. User name

You can set the configs with help of the following git command:
git config --local <config_name> <config_value>

User email = user.email
User name = user.name

# Then we should create .gitignore file

# To create the commit we should add the files that going to be a part of the commit:

git add <filename>
git commit -m "commit message"

### To upload our commit to the repo:
1. We sould configure remote repo
2. We sould push our commit to the remote repo.
git push -u origin HEAD

# Unstage changes from stage
git reset <file name>

# Check last commits.
git log -5 --oneline

# Remove last commit.
git reset --soft HEAD~1

# Rewrite the history on the remote with local history
git push -fu origin HEAD


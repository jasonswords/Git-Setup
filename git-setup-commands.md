# Git command-line setup

Update system
```bash
sudo apt update && sudo apt upgrade
```

Install git
```bash 
sudo apt install git
```
Verify version
```bash
git --version
```

Save configuration details of github account
> Replace name and email with your own username and email
```bash
git config --gloabl user.name "name"
git config --gloabl user.email "email"
```

Make a directory to work from
```bash
mkdir test
```

Move into new directory
```bash
cd test
```

Create new text file with some content
```bash
echo "This is new text file with some content" > README.md
```

Tell git to track new file
```bash
git add --all     or     git add *   or     git add README.md 
```
Commit new file with message for reason of commit, update, minor changes etc
```bash
git commit -m "This is a commit message"
```

## Creating a new repository on github

Upload file to github
```bash
git remote add origin http://github.com/account-name/repo-name
git push -u origin master
```

### Install hub for remote repository creation
```bash
sudo snap install hub
git config --global hub.protocol https
```

Create repository
```bash
hub create
```
>If this fails to create repo, run the previous command git push -u origin master again.

>With hub, if a credentials problem occurs, change of user-name, email. etc
```bash
sudo rm ~/.config/hub
```
> This will delete previous hub settings and hub will ask for user-name and email again.

```bash
hub create
```

## Switching remote url`s from ssh to https 
```bash
git remote -v
```

Change remote URL`s from ssh to https
```bash
git remote set-url origin http://github.com/user-name/repo-name.git
```


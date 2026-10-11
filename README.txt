Practical 2 — Git Configuration
git --version
git config --global user.name "Your Name"
git config --global user.email "your@email.com"
git config --global core.editor "code --wait"
git config --list
notepad ~/.gitconfig

Practical 3 — SSH Keys
ssh-keygen -t ed25519 -C "your@email.com"
eval "$(ssh-agent -s)"
ssh-add ~/.ssh/id_ed25519
ssh -T git@github.com
cat ~/.ssh/id_ed25519.pub

Practical 4 — Git Repository
mkdir foldername
ls
cd foldername
cd ..
pwd
git init
echo "writeanystuff">README.md
git add README.md
git commit -m "write any comment"
git clone REPOSITORY_URL
ls
cd reponame
echo "writeanystuff">hello.txt
git status
git add hello.txt
git commit -m "hello.txt"
git push -u origin main

Practical 5 — Files and .gitignore
cat filename
touch .gitignore
echo "*.filepattern">.gitignore
echo "foldername/">>.gitignore
git add .gitignore
git commit -m "writeanycomment"
git log
git log --oneline
git rm -f filename
git commit -m "remove file"
git rm --cached filename
git mv originalfilename newfilename
git commit -m "rename file"

Practical 6 — Git History, Reset and Revert
git log --graph
git log --graph --oneline --all
git add filename
git reset filename
git log --oneline
git revert COMMIT_ID
git push -u origin main

Practical 7 — Remotes and Tags
git remote add origin https://github.com/YOUR_USERNAME/YOUR_REPOSITORY.git
git remote -v
git fetch origin
git pull origin main
git tag -a tagname -m "writeanycomment"
git tag tagname
git tag
git show tagname
git push origin tagname
git push https://github.com/modhnishita/prac5 tagname
git push --tags

Practical 8 — Commits and Branching
git commit -m "fix: correct validation bug in signup form"
git commit -m "feat: add search functionality to dashboard" -m "implemented search filters and optimised database queries"
git add filename1 filename2
git commit -m "any message" -m "any message"
git add -p
git checkout -b branchname
git checkout main
git branch
git merge branchname
git rebase main

Practical 9 — Git Push
git push repositoryurl
git checkout branchname
git add .
git push --force origin main
git push origin branchname
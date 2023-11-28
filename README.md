# X-Cart-test-task
For test purposes

# Setting up git workspace

ssh-keygen -t rsa -b 4096 -C "evil.tanch1k@gmail.com"
cat ~/.ssh/id_rsa.pub
gh auth login
gh repo create X-Cart-test-task --public --add-readme -c
gh repo clone Eviltanch1k/X-Cart-test-task
cd X-Cart-test-task

# Creating sample html outside cli

git add cv.html
git commit -m "Created first iteration of my cv"
git push origin main

# Creating branch-1

git checkout -b branch-1
git add cv.html
git commit -m "Updating work details"
git push origin branch-1
gh pr create --base main --title "PR1" --body "Pull request to merge branch-1 to main"
gh pr merge 1

# Creating branch-2

git checkout -b branch-2
git commit -m "Updating description"
git push origin branch-2
gh pr create --base main --title "PR2" --body "Conflicting pr"
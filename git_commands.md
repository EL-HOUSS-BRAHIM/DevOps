git clone git@github.com:EL-HOUSS-BRAHIM/DevOps.git
git branch -m master
mkdir Task1
echo "this the readme.md on the master branch" > README.md
git add .
git commit -m "adding the task1 folder and the README.md file"
git push
git checkout -b dev
touch test
git add .
git commit -m "adding a test file inside the dev branch"
git push --set-upstream origin dev
git checkout -b %USERNAME-new_feature
echo "this the readme.md on the %USERNAME-new_feature branch" > README.md
echo ".*" > .gitignore
git add -f .
git commit -m "adding the readme and .gitignore file inside the %USERNAME-new_feature branch"
git push --set-upstream origin %USERNAME-new_feature
< go to github and create a pull request base is dev and compare is %USERNAME-new_feature>
git checkout dev
git merge %USERNAME-new_feature
git push origin dev
< go to github and create a pull request base is master and compare is dev>
git checkout master
git merge dev
git push origin master
<done merge>
git checkout %USERNAME-new_feature
echo "this the New readme.md on the %USERNAME-new_feature branch" > README.md
git add .
git commit -m "editing the readme file on the %USERNAME-new_feature branch"
git revert HEAD
git checkout master
git log > log.txt
git add .
git commit -m "adding the git log to the master branch"
git push
git branch -d %USERNAME-new_feature
git branch -D %USERNAME-new_feature
git push origin --delete %USERNAME-new_feature

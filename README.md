Zanimalnq
=========

Installation

Clone this repo

cd to repo location

sudo apt-get install mysql mysql-server mysql-python

pip install south

mysql -u root -p

CREATE DATABASE mdrsDatabase;

CREATE USER 'mdrs'@'localhost' IDENTIFIED BY 't34mt34mt';

GRANT ALL PRIVILEGES ON mdrsDatabase.* TO 'mdrs'@'localhost';

quit

python manage syncdb

python manage migrate

python runserver 0.0.0.0:8080

=========

1. Always, always run 'git status' before you do anything. It will tell you excactly whats happening!

2.a. You've added a new file and status says it's un tracked. That's fine! Use 'git add <file path>' to track it, now git will keep up with any changes you make to it.

2.b. You've got a tracked file and you don't want it tracked any more. Either delete it and commit that or use 'git checkout -- <filepath>' to untrack it and not delete the file.

3. Ok status should now list all your file changes, if you're happy with it time to tell git you've done some work. Run 'git commit -am "Commit message"' to make a commit and return to a clean working directory. This commit is LOCAL only! Git hub doesn't know about it and neither do we. Commit often so you can keep up with your own changes and you can revert to a old commit if you fuck up majorly.

4. So you've commited a lot and you are ready to push your changes for the day. Now it's time to tell git, but not before you make sure it's ok to go! Firstly run status, make sure you have nothing new to commit and everything you dont want to push is untracked. Now run 'git pull' this will update your local files with the ones from github, there may be none, there may be many that don't effect you or there may be many that do.

5.a. Merge conflicts. Don't panic! Git might scream a little but this is normal. Run 'git mergetool' and make edits to the center file from your version on the left and the new, pulled version to the right. Once you are happy, save the middle file and quit merge tool and continue through conflicts.

5.b. No conflicts! Now simply run 'git push' and it will push your changes to github and some other poor developer has to deal with your merge conflicts!


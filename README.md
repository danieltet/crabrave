

REFERENCES:
http://rogerdudler.github.io/git-guide/
https://git-scm.com/docs
https://dzone.com/articles/top-20-git-commands-with-examples




SETUP:

1. Go to this website and setup a free github account:
https://github.com/
(do not setup a team or company, as soon as you have an account you are good to go)

2. Give, in chime, your github login name to the team

3. Daniel Tet will add you to the github repo
https://github.com/danieltet/crabrave.git

4. Download and install GIT software on your computer:
https://gist.github.com/derhuerst/1b15ff4652a867391f03
(you will need to be comfortable with command prompt: CMD on PC, or Terminal on mac)


FIRST TIME USE OF REPO:

5. Go to the directory where you want to keep your code on your machine

6. Clone the repository from github
% git clone https://github.com/danieltet/crabrave.git crabrave
enter username and password if necessary
this will create a directory called crabrave with the files inside of it


BEFORE STARTING TO WORK:

7. See if there are any changes on the github
cd to the directory created in #6 above
% cd crabrave

get status - this will tell you if there are changes on the github
%git status


8. Get latest changes from github (work others have done)
cd to the directory created in #6 above
% cd crabrave
% git pull 


MAKE AN EDIT AND COMMIT YOUR CHANGES

9. edit the file with any editor you want

10. See that the file is modified
% cd crabgrass
% git status
you should the file appear with the word modified in front of it

now commit the change you made to the file: FILENAME
% git add FILENAME
or, if you want to add changes made to multiple files, or new files
% git add .

see if the changes were added; you will now see the word added
% git status

now commit them to local repo (all the added changes)
% git commit -m "describe changes here"

now you can see you are ahead of brain on github
% git status

now push the changes to github for everyone else 
to be able to access and pull on their computer
% git push origin master

see what the status is
% git status


DEALING WITH CONFLICTS

Conflicts happen when you try to push a change to a file but don't have the
latest form github; in other words someone else made changes without telling you.
This is common. Here is what to do.

11. Notice the problem
while doing a push (like in step #10 above)
% git push origin master

you will get an error like this:
To https://github.com/danieltet/crabrave.git
 ! [rejected]        master -> master (fetch first)
error: failed to push some refs to 'https://github.com/danieltet/crabrave.git'
hint: Updates were rejected because the remote contains work that you do
hint: not have locally. This is usually caused by another repository pushing
hint: to the same ref. You may want to first integrate the remote changes
hint: (e.g., 'git pull ...') before pushing again.
hint: See the 'Note about fast-forwards' in 'git push --help' for details.

12. Pull the changes from github
% git pull

# this will produce a message like this, as it automatically merges (puts all the changes in one file, separated by ===========
Auto-merging README.md
CONFLICT (content): Merge conflict in README.md
Automatic merge failed; fix conflicts and then commit the result.

13. Clean up the changes manually by editing the file

14. Make sure the file still compiles and works

15. Now pretend it's a newly edited file and commit and push it like in #10 above








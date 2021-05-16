# GitFlow Class

This repository was used for me to learn about GitFlow, how it works and how to use it in a project.

## How to use GitFlow in a project 

. Create a repository;<br />
. From the terminal, go to the folder where you want to insert the project;<br />
. If I start the project with a README.md, make a git clone:<br />
git clone link_repository<br />
. Go to the project folder:<br />
cd project_name<br />
. Start gitflow: <br />
git flow init<br />
. Type the name of the production branch (main) (or just press enter);<br />
. Type the name of the development branch (develop) (or just press enter);<br />
. Type the name of the feature (feature) branch (or just enter);<br />
. Type the name of the bugfix branch (bugfix) (or just press enter);<br />
. Type the name of the release branch (or just press press enter);<br />
. Type the name of the hotfix branch (or just press enter);<br />
. Type the name of the support (support) branch (or just press enter);<br />
. Type if you want a prefix tag in the version (the v that appears before 1.0, for example) (if you don't, just press enter);<br />
. If you want to list the branches, do:<br />
git branch —list<br />
. If I want to changing a file, just do:<br />
code README.md<br />
<br />
. Save the file<br />
. git add .<br />
. git commit -m “”<br />
. If I want to create a new feature in the project, we have to create a new feature. For this:<br />
git flow feature start feature_name<br />
. Create any file:<br />
code giropops.txt<br />
. Save it<br />
git add.<br />
git commit -m “”<br />
. So, we have to take these changes to the remote server (Github, Gitlab, ...). For this:
git flow feature publish<br />
. After finishing the development of this new feature, end it with: (with that, the contents of the branch feature_name will be merged with the branch develop, and we are redirected to the branch develop)<br />
git flow feature finish feature_name<br />
. To get a feature from the remote repository (already started to be developed by other developers), we have to pull:
Git flow feature pull feature_name<br />
. After that, to send it to the release branch:<br />
git flow release start release_name (can start with name 1.0)<br />
. When I finish developing and the release is ready, do:<br />
git flow release finish release_name<br />
git commit -m “”<br />
. If I want to publish to the remote repository, just:<br />
git flow release finish release_name<br />

. To work on the hotfix:<br />
git flow hotfix start hotfix_name<br />
. Change any file you want<br />
git add .<br />
git commit -m “”<br />
git flow hotfix finish hotfix_name<br />
. control^C para sair<br />
git commit -m ""
git push —all<br />
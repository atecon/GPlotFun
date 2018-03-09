Create a new repository
----------------------
git clone git@scm.darnold.org:atecon/GPlotFun.git
cd GPlotFun
touch README.md
git add README.md
git commit -m "add README"
git push -u origin master

Existing folder
---------------
cd existing_folder
git init
git remote add origin git@scm.darnold.org:atecon/GPlotFun.git
git add .
git commit
git push -u origin master

Existing Git repository
----------------------
cd existing_repo
git remote add origin git@scm.darnold.org:atecon/GPlotFun.git
git push -u origin --all
git push -u origin --tags

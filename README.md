# Team-Git-Commands-Ref

### Our Gitflow ###

1. make a branch under develop in GitHub, say, testing-branch
2. git clone files onto local machine the first time, or git pull subsequent
3. git branch -a
4. list won't show branch under develop
5. git checkout development
6. git checkout testing-branch (same name as the one up on GitHub)
7. git branch -a
8. make your changes
9. git add -A
10. git commit -m "asdf"
11. git push
12. PR up on GitHub, wait for review, then finish the merge into development
13. repeat from number 2

### General Reference ###

#### DISPLAY BRANCH NAMES LOCALLY & REMOTE: ####
git branch -a                                    

#### DISPLAY LOCAL BRANCH NAMES ONLY: ####
git branch                                        

#### CREATE A NEW BRANCH: ####
git branch [new_branch_name]    

#### MOVE TO A NEW BRANCH: ####
git checkout [new_branch_name]      

#### CREATE A NEW BRANCH & MOVE TO IT: ####
git checkout -b [new_branch_name]

#### PULL DOWN REMOTE INTO CURRENT BRANCH (COMBINES FETCH AND MERGE): ####
git pull 

#### COMMANDS TO RESET LOCAL TO BE IDENTICAL TO REMOTE: ####
git fetch --prune origin
 
#### STAGE MODIFIED & UNTRACKED FILES FROM ALL LOCAL BRANCHES FOR COMMIT: ####
git add -A

#### STAGE MODIFIED & UNTRACKED FILES FROM ONLY CURRENT LOCAL BRANCH FOR COMMIT: ####
git add .    

#### UNDO STAGING PRIOR TO A COMMIT FOR ALL FILES IN STAGING: ####
git reset  

#### UNDO STAGING PRIOR TO A COMMIT FOR A SPECIFC FILE IN STAGING: ####
(git reset filename )
git recommended to undo staging:
git restore --staged <file>

#### COMMIT STAGED FILES SINGLE LINE (INCLUDE BRANCH NAME IN MESSAGE): ####
git commit -m "asdf"  

#### COMMIT STAGED FILES WITH DESCRIPTION: ####
git commit -m "asdf" -m "Description:  asdf" 

#### STAGE & COMMIT IN ONE COMMAND (USED FOR FILES ALREADY BEING TRACKED): ####
git commit -am "asdf"   

#### UNDO LAST COMMIT TO RESET POINTER TO LAST COMMIT AND GO BACK 1 COMMIT: ####
git reset HEAD~1 

#### UNDO MORE THAN THE LAST COMMIT: ####
git log     
(copy hash# from the commit you want to revert to)                   
git reset hash#  
git status  

#### UNDO AND HARD RESET AS IF YOU NEVER MADE CHANGES: ####
git log
(copy hash# from the commit you want to revert to)  
git reset --hard hash# 

#### PUSH COMMITTED FILES TO GITHUB DEFAULT BRANCH: ####
git push origin [new_branch_name] 

#### DELETE LOCAL BRANCH ONCE MERGED (PR REVIEWED): ####
git checkout main   
git pull 
git branch -d [new_branch_name] 

#### UNDOING A PULL REQUEST (PR): ####
use the revert on GitHub

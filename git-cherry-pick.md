### Here we want to rollback to the specified commit point and cherry pick some usefull commit  
  
   
#### Usecase  

eg. When you merged some commits but some day you want rollback to a specified commit but stay some usefull commits.

  
   
#### Commands
// Clone repository  
git clone `https://xxx/xxx/xxx.git`  
 
// Check all exist remote branches  
git branch -r

// Checkout and push a branch for reset   
git checkout `origin/branch-for-reset` -b `branch-for-reset`  
git push origin -u `branch-for-reset`  

// Take a look at log  
git log  

// Reset to the specified commit  
git reset --hard `commit_id`  

// Push origin  
git push origin `branch-for-reset`:`branch-for-reset`  

// Recover commits which you do not want to delete  
git cherry-pick `commit - 1`  
git cherry-pick `commit - 2`  

// Push origin  
git push origin `branch-for-reset`:`branch-for-reset`

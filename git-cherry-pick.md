### Here we want to rollback to the specified commit point and cherry pick some usefull commit  
  
   
#### Usecase  

eg. When you merged some commits but some day you want rollback to a specified commit but stay some usefull commits.

  
   
#### Commands
// Clone repository  
git clone `https://xxx/xxx/xxx.git`  
 
// Check all exist remote branches  
git branch -r

// Delete remote repository   
git push origin :branch-for-delete  

// If you have any other deleted remote branch locally, clean them  
git remote prune origin

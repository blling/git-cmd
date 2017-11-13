### Here we want to delete remote branch and clean deleted remote branch locally  
  
   
#### Usecase  

eg. When you want to delete remote branch and clean deleted remote branch locally.

  
   
#### Commands
// Clone repository  
git clone `https://xxx/xxx/xxx.git`  
 
// Check all exist remote branches  
git branch -r

// Delete remote repository   
git push origin :branch-for-delete  

// If you have any other deleted remote branch locally, clean them  
git remote prune origin

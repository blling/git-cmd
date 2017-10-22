### Here we want to merge a different branch from another repository.  
  
   
#### Usecase  

eg. When you forked a repository and you want to synchronize it with the origin repository someday.

  
   
#### Commands
// Clone repository  
git clone `https://xxx/xxx/xxx.git`  
 
// Checkout branch for merge, here do not merge on master branch directly  
git checkout -b `master-merge` `origin/master`

// Take a look at the current upstreams   
git remote -vv

// Add another repository upstream named "forigin"   
git remote add `forigin` `https://yyy/yyy/yyy.git`  

// Fetch "forigin"  
git fetch `forigin`  

// Confirm branches and it`s related remote  
git branch -avv  

// Here assume we want to merge "forigin/master" branch into current local branch   
git merge `forigin/master`  
   
// When there is no conflict then check out master and do merge and delete `master-merge` branch  
git checkout `master`  
git merge `master-merge`  
git branch -d `master-merge`  

// Push to remote repository   
git push

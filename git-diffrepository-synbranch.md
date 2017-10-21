### Here we want to merge a different branch from another repository.  
  
   
#### Usecase  

eg. When you forked a repository and you want to synchronize it with the origin repository someday.

  
   
#### Commonds

// Take a look at my current upstreams    
git remote -v  

// Add another repository upstream named "forigin"   
git remote add `forigin` git@github.com:xxx/xxx.git  

// Fetch "forigin"  
git fetch `forigin`  

// Confirm current branch and it`s related remote  
git branch -avv  

// Here assume we want to merge "forigin/master" branch into current local branch   
git merge `forigin/master`   

// push to remote repository   
git push

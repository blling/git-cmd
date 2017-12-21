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

// Show all the relationship between remote and local  
git remote show origin  

// If you have any other deleted remote branch locally, clean them  
git remote prune origin  

// Or you can do like this  
git fetch -p  

// Here will prune local tracking branches  
git branch -r | awk '{print $1}' | egrep -v -f /dev/fd/0<(git branch -vv | grep origin) | awk '{print $1}' | xargs git branch -D  

// All in one
```shell
git remote prune origin; git branch -r | awk '{print $1}' | egrep -v -f /dev/fd/0 <(git branch -vv | grep origin) | awk '{print $1}' | xargs git branch -d
```

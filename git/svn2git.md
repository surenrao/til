in wsl 2 (ubuntu), make sure git and subversion is installed.

    git svn clone --no-minimize-url -T trunk -b branches -t tags -A "C:\Projects\authors.txt" "http://your-svn-domain/svn/main/Project"

if want all branches to be pushed then we need to add all branches locally. using code from https://git-scm.com/book/en/v2/Git-and-Other-Systems-Migrating-to-Git modified to exclude origin 
 
    for b in $(git for-each-ref --format='%(refname:short)' refs/remotes/origin/); do new_branch=$(echo $b | sed 's/origin\///'); git branch $new_branch refs/remotes/$b && git branch -D -r $b; done


Warning: you wont be able to merge svn back to git after deleting the trunk.
    git branch -d trunk

    git remote add origin http://your-git-domain/Project.git

    git push origin --all

# PLPBasicGitAssignment
Trying to gain mastery in GitHub
when I tried to "git push -u origin main", the following error appeared

To https://github.com/uweoma/PLPBasicGitAssignment.git
 ! [rejected]        main -> main (fetch first)
error: failed to push some refs to 'https://github.com/uweoma/PLPBasicGitAssignment.git'
hint: Updates were rejected because the remote contains work that you do not
hint: have locally. This is usually caused by another repository pushing to
hint: the same ref. If you want to integrate the remote changes, use
hint: 'git pull' before pushing again.
hint: See the 'Note about fast-forwards' in 'git push --help' for details. 
(The error message you're encountering indicates that the remote repository (GitHub) has commits that you don't have locally in your repository. This situation can occur if changes have been made to the repository on GitHub since your last pull or if you have multiple collaborators)

So I started troubleshooting by doing this "git pull origin main" and then got a fatal error 

remote: Enumerating objects: 3, done.
remote: Counting objects: 100% (3/3), done.
remote: Compressing objects: 100% (2/2), done.
remote: Total 3 (delta 0), reused 0 (delta 0), pack-reused 0
Unpacking objects: 100% (3/3), 897 bytes | 6.00 KiB/s, done.
From https://github.com/uweoma/PLPBasicGitAssignment
 * branch            main       -> FETCH_HEAD
 * [new branch]      main       -> origin/main
fatal: refusing to merge unrelated histories
(The error message "fatal: refusing to merge unrelated histories" typically occurs when Git detects that the histories of the branches you're trying to merge have diverged significantly and don't have a common base commit)

So I went further to do this: "git pull origin main --allow-unrelated-histories" and I was able to commit


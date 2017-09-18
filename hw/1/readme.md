Michael O'Lear  
(A)
```bash  
Michael O'Lear@DESKTOP-LMVEA0K MINGW64 ~/git/ICP2017F/hw/1 (master)
$ git branch test1

Michael O'Lear@DESKTOP-LMVEA0K MINGW64 ~/git/ICP2017F/hw/1 (master)
$ git branch test2  
```  
(B)  
```bash  
Michael O'Lear@DESKTOP-LMVEA0K MINGW64 ~/git/ICP2017F/hw/1 (master)
$ git checkout test1
Switched to branch 'test1'

Michael O'Lear@DESKTOP-LMVEA0K MINGW64 ~/git/ICP2017F/hw/1 (test1)
$ touch test.txt
```  
(C)  
```bash  
Michael O'Lear@DESKTOP-LMVEA0K MINGW64 ~/git/ICP2017F/hw/1 (test1)
$ vim test.txt
```  
(D)  
```bash  
Michael O'Lear@DESKTOP-LMVEA0K MINGW64 ~/git/ICP2017F/hw/1 (test1)
$ git commit -a
[test1 99608ed] j
 1 file changed, 1 insertion(+)
 create mode 100644 hw/1/test.txt
```  
(E)  
```bash  
Michael O'Lear@DESKTOP-LMVEA0K MINGW64 ~/git/ICP2017F/hw/1 (test1)
$ git checkout test2
Switched to branch 'test2'
M       hw/1/readme.md

Michael O'Lear@DESKTOP-LMVEA0K MINGW64 ~/git/ICP2017F/hw/1 (test2)
$ ls
readme.md
```  
I don't see the test.txt file because we are in a different branch than where the test.txt file  
was created, and files don't automatically transcend branches.  

(F)  
```bash  
Michael O'Lear@DESKTOP-LMVEA0K MINGW64 ~/git/ICP2017F/hw/1 (test2)
$ touch test.txt

Michael O'Lear@DESKTOP-LMVEA0K MINGW64 ~/git/ICP2017F/hw/1 (test2)
$ vim test.txt
```  
(G)  
```bash  
Michael O'Lear@DESKTOP-LMVEA0K MINGW64 ~/git/ICP2017F/hw/1 (test2)
$ git checkout test1
error: The following untracked working tree files would be overwritten by checkout:
        hw/1/test.txt
Please move or remove them before you switch branches.
Aborting

Michael O'Lear@DESKTOP-LMVEA0K MINGW64 ~/git/ICP2017F/hw/1 (test2)
$ rm test.txt

Michael O'Lear@DESKTOP-LMVEA0K MINGW64 ~/git/ICP2017F/hw/1 (test2)
$ git checkout test1
Switched to branch 'test1'
```  
(H)  
```bash  
Michael O'Lear@DESKTOP-LMVEA0K MINGW64 ~/git/ICP2017F/hw/1 (test1)
$ git checkout master
Switched to branch 'master'
Your branch is up-to-date with 'origin/master'.

Michael O'Lear@DESKTOP-LMVEA0K MINGW64 ~/git/ICP2017F/hw/1 (master)
$ git merge test1
Merge made by the 'recursive' strategy.
 hw/1/test.txt | 1 +
 1 file changed, 1 insertion(+)
 create mode 100644 hw/1/test.txt
```  
(I)  
```bash  
Michael O'Lear@DESKTOP-LMVEA0K MINGW64 ~/git/ICP2017F/hw/1 (master)
$ ls
readme.md  test.txt
```  
(J)  
```bash  
Michael O'Lear@DESKTOP-LMVEA0K MINGW64 ~/git/ICP2017F/hw/1 (master)
$ git merge test2
Merge made by the 'recursive' strategy.
```  
No error; When asked to resolve the error caused by the test.txt file earlier in this assignment, my solution was  
to simply delete the file. Therefore, that file no longer exist in branch test2 to conflict with the test.txt file  
in branch test1 and generate the error that was expected by the assignment.
(K)  
```bash  
Michael O'Lear@DESKTOP-LMVEA0K MINGW64 ~/git/ICP2017F/hw/1 (master)
$ git checkout test2
Switched to branch 'test2'
M       hw/1/readme.md
```  
No error; See above
(L)  
```bash  
Michael O'Lear@DESKTOP-LMVEA0K MINGW64 ~/git/ICP2017F/hw/1 (test2)
$ git status
On branch test2
Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git checkout -- <file>..." to discard changes in working directory)

        modified:   readme.md

Untracked files:
  (use "git add <file>..." to include in what will be committed)

        ../../20170415_105555.jpg

no changes added to commit (use "git add" and/or "git commit -a")

```  
No error; See above  

(M)  
Deleting the file was far more efficient.  

(N)  
```bash  
Michael O'Lear@DESKTOP-LMVEA0K MINGW64 ~/git/ICP2017F/hw/1 (test2)
$ git status
On branch test2
Changes to be committed:
  (use "git reset HEAD <file>..." to unstage)

        new file:   ../../20170415_105555.jpg

Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git checkout -- <file>..." to discard changes in working directory)

        modified:   readme.md


Michael O'Lear@DESKTOP-LMVEA0K MINGW64 ~/git/ICP2017F/hw/1 (test2)
$ git commit -a
warning: LF will be replaced by CRLF in hw/1/readme.md.
The file will have its original line endings in your working directory.
[test2 a1c3444] s
 2 files changed, 43 insertions(+), 5 deletions(-)
 create mode 100644 20170415_105555.jpg

Michael O'Lear@DESKTOP-LMVEA0K MINGW64 ~/git/ICP2017F/hw/1 (test2)
$ git checkout test2
Already on 'test2'
```  
(O)  
```bash  
Michael O'Lear@DESKTOP-LMVEA0K MINGW64 ~/git/ICP2017F/hw/1 (test2)
$ git branch -d test1
error: The branch 'test1' is not fully merged.
If you are sure you want to delete it, run 'git branch -D test1'.
```  

(P)  
```bash  
Michael O'Lear@DESKTOP-LMVEA0K MINGW64 ~/git/ICP2017F/hw/1 (master)
$ git branch -d test1
Deleted branch test1 (was 99608ed).

Michael O'Lear@DESKTOP-LMVEA0K MINGW64 ~/git/ICP2017F/hw/1 (master)
$ git branch
  development
* master
  test2
```  
(Q)  
The messages are different because branches don't normally have linear authority, only top down authority.
(R)  
```bash  
Michael O'Lear@DESKTOP-LMVEA0K MINGW64 ~/git/ICP2017F/hw/1 (master)
$ git checkout test2
Switched to branch 'test2'

Michael O'Lear@DESKTOP-LMVEA0K MINGW64 ~/git/ICP2017F/hw/1 (test2)
$ git branch -d test2
error: Cannot delete branch 'test2' checked out at 'C:/Users/Michael O'Lear/git/ICP2017F'
```
A branch cannot delete itself  
(S)  
```bash  
Michael O'Lear@DESKTOP-LMVEA0K MINGW64 ~/git/ICP2017F/hw/1 (test2)
$ git checkout master
Switched to branch 'master'
Your branch is ahead of 'origin/master' by 4 commits.
  (use "git push" to publish your local commits)

Michael O'Lear@DESKTOP-LMVEA0K MINGW64 ~/git/ICP2017F/hw/1 (master)
$ git branch -D test2
Deleted branch test2 (was a1c3444).

Michael O'Lear@DESKTOP-LMVEA0K MINGW64 ~/git/ICP2017F/hw/1 (master)
$ git branch
  development
* master
```  
(T)  
```bash  
```  


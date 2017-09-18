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

(B)  
```bash  
```  
(B)  
```bash  
```  
(B)  
```bash  
```  
(B)  
```bash  
```  
(B)  
```bash  
```  
(B)  
```bash  
```  
(B)  
```bash  
```  
(B)  
```bash  
```  
(B)  
```bash  
```  
(B)  
```bash  
```  
(B)  
```bash  
```  
(B)  
```bash  
```  
(B)  
```bash  
```  
(B)  
```bash  
```  
(B)  
```bash  
```  



# Linux commands-Shell scripting
Linux commands-Shell scripting

# AIM:
To practice Linux Commands and Shell Scripting

# DESIGN STEPS:

### Step 1:

Navigate to any Linux environment installed on the system or installed inside a virtual environment like virtual box/vmware or online linux JSLinux (https://bellard.org/jslinux/vm.html?url=alpine-x86.cfg&mem=192) or docker.

### Step 2:

Execute the following commands

### Step 3:

Testing the commands for the desired output. 

# COMMANDS:
### Create the following files file1, file2 as follows:
cat > file1
```
chanchal singhvi
c.k. shukla
s.n. dasgupta
sumit chakrobarty
^d
```
cat > file2
```
anil aggarwal
barun sengupta
c.k. shukla
lalit chowdury
s.n. dasgupta
^d
```
### Display the content of the files
cat < file1
<img width="1581" alt="cat file1" src="https://github.com/user-attachments/assets/321fb4d1-b0f3-453e-8d18-fcbcabdfa5b0" />



cat < file2
## OUTPUT
<img width="1581" alt="cat file2" src="https://github.com/user-attachments/assets/e650db97-a091-42f6-94f8-892510581cdb" />


# Comparing Files
cmp file1 file2
## OUTPUT
<img width="1593" alt="comp" src="https://github.com/user-attachments/assets/b036a974-5b96-4257-ad58-9a5574e21981" />

 
comm file1 file2
 ## OUTPUT
<img width="1581" alt="comm" src="https://github.com/user-attachments/assets/1a8901fa-f0c4-4cad-b210-22dc684ffba6" />

 
diff file1 file2
## OUTPUT

<img width="1581" alt="diff" src="https://github.com/user-attachments/assets/7d1f7f21-0e2e-4f13-9e6d-bf6a03fbec3e" />

#Filters

### Create the following files file11, file22 as follows:

cat > file11
```
Hello world
This is my world
^d
```
cat > file22
```
1001 | Ram | 10000 | HR
1002 | tom |  5000 | Admin
1003 | Joe |  7000 | Developer
^d
```


cut -c1-3 file11
## OUTPUT

<img width="1581" alt="cut-c1-c3file11" src="https://github.com/user-attachments/assets/58fa2591-5c88-44c5-9282-b2e4716d867a" />



cut -d "|" -f 1 file22
## OUTPUT

<img width="1669" alt="cut-d-f1file22" src="https://github.com/user-attachments/assets/b8425d35-b16b-49eb-a164-5b04c945d5ec" />


cut -d "|" -f 2 file22
## OUTPUT
<img width="1669" alt="cut-d-f2file22" src="https://github.com/user-attachments/assets/15b5be2b-ee24-4449-b723-253f677c91d3" />



cat < newfile 
```
Hello world
hello world
^d
````
cat > newfile 
Hello world
hello world
 
grep Hello newfile 
## OUTPUT

<img width="1669" alt="grepHello" src="https://github.com/user-attachments/assets/5106f43e-2656-4646-9c09-2d0dffdefd71" />


grep hello newfile 
## OUTPUT

<img width="1669" alt="grep_hello" src="https://github.com/user-attachments/assets/cbaf8849-1b7c-46f8-87de-7a71203737a8" />



grep -v hello newfile 
## OUTPUT


<img width="1669" alt="grep-v" src="https://github.com/user-attachments/assets/bfa3fa1f-7818-471b-87d5-583e62376032" />

cat newfile | grep -i "hello"
## OUTPUT


<img width="1781" alt="catgrepi" src="https://github.com/user-attachments/assets/358a1065-203f-447a-80f8-13eadbfe4dd2" />


cat newfile | grep -i -c "hello"
## OUTPUT

<img width="1827" alt="catgrepic" src="https://github.com/user-attachments/assets/268e6be4-9a9e-4192-92c3-6cd8548ceda9" />



grep -R ubuntu /etc
## OUTPUT
<img width="1039" alt="grep -r ubuntu" src="https://github.com/user-attachments/assets/1f64bcc8-71b9-4f8a-81d0-203d5901f965" />



grep -w -n world newfile   
## OUTPUT
<img width="1108" alt="grep newworld" src="https://github.com/user-attachments/assets/fce49f5f-eadd-46ec-b718-acaa9ee207a3" />


cat < newfile 
```
Hello world
hello world
Linux is world number 1
Unix is predecessor
Linux is best in this World
^d
```

cat > newfile
```
Hello world
hello world
Linux is world number 1
Unix is predecessor
Linux is best in this World
^d
 ```
egrep -w 'Hello|hello' newfile 
## OUTPUT
<img width="1172" alt="egrep1" src="https://github.com/user-attachments/assets/90ddc705-6c97-4a46-af70-387223daf35a" />



egrep -w '(H|h)ello' newfile 
## OUTPUT
<img width="1172" alt="egrep2" src="https://github.com/user-attachments/assets/32a27f75-ec39-453d-b72d-5fa6ef0fd89c" />



egrep -w '(H|h)ell[a-z]' newfile 
## OUTPUT
<img width="1191" alt="egrep3" src="https://github.com/user-attachments/assets/c0e048d5-def5-45d2-b5af-f199d58a913c" />





egrep '(^hello)' newfile 
## OUTPUT

<img width="1191" alt="egrep4" src="https://github.com/user-attachments/assets/af9d230b-7038-4dc0-a7b7-840fd2e4ac14" />


egrep '(world$)' newfile 
## OUTPUT

<img width="1191" alt="egrep5" src="https://github.com/user-attachments/assets/3a6cebec-3f87-40e0-a591-cf51e510ee33" />


egrep '(World$)' newfile 
## OUTPUT
<img width="1191" alt="egrep6" src="https://github.com/user-attachments/assets/74d0d408-ab75-4faa-87bd-1de9df999e57" />


egrep '((W|w)orld$)' newfile 
## OUTPUT

<img width="1191" alt="egrep7" src="https://github.com/user-attachments/assets/1296900e-e01c-4ffa-a731-d1f1a7ff7131" />


egrep '[1-9]' newfile 
## OUTPUT

<img width="1191" alt="egrep8" src="https://github.com/user-attachments/assets/95b5e0e0-fb50-4aad-a26d-5f335ffadfd2" />


egrep 'Linux.*world' newfile 
## OUTPUT
<img width="1191" alt="egrep9" src="https://github.com/user-attachments/assets/0e2ea44c-3130-47ae-8d85-66fef3e84c55" />


egrep 'Linux.*World' newfile 
## OUTPUT

<img width="1191" alt="egrep10" src="https://github.com/user-attachments/assets/09e2c2ee-16f7-43f4-ae35-e6ae1bd1eb4b" />

egrep l{2} newfile
## OUTPUT
<img width="1191" alt="egrep11" src="https://github.com/user-attachments/assets/9d36ba13-5431-4647-bc82-1196afce2024" />



egrep 's{1,2}' newfile
## OUTPUT 
<img width="1191" alt="egrep12" src="https://github.com/user-attachments/assets/e7b33ab0-b297-4786-bfec-550b89a4b7c4" />


cat > file23
```
1001 | Ram | 10000 | HR
1001 | Ram | 10000 | HR
1002 | tom |  5000 | Admin
1003 | Joe |  7000 | Developer
1005 | Sam |  5000 | HR
1004 | Sit |  7000 | Dev
1003 | Joe |  7000 | Developer
1001 | Ram | 10000 | HR
^d
```


sed -n -e '3p' file23
## OUTPUT

<img width="1191" alt="sed1" src="https://github.com/user-attachments/assets/7ce206ad-216a-4bd8-aa72-e4f0ac95e770" />


sed -n -e '$p' file23
## OUTPUT
<img width="1191" alt="sed2" src="https://github.com/user-attachments/assets/47770e6b-3c65-4015-8fd7-d2367829fcf3" />




sed  -e 's/Ram/Sita/' file23
## OUTPUT

<img width="1191" alt="sed3" src="https://github.com/user-attachments/assets/2d98ff67-5999-4434-bebc-d180f83728ff" />


sed  -e '2s/Ram/Sita/' file23
## OUTPUT
<img width="1191" alt="sed4" src="https://github.com/user-attachments/assets/6bcc480c-daff-4679-8ff7-3e232b4271e1" />



sed  '/tom/s/5000/6000/' file23
## OUTPUT

<img width="1191" alt="sed5" src="https://github.com/user-attachments/assets/0067d01f-6845-49df-b841-11b35b2605ce" />


sed -n -e '1,5p' file23
## OUTPUT
<img width="1191" alt="sed6" src="https://github.com/user-attachments/assets/d41f22f0-20dc-4fc5-969a-c6cfc42b7a6e" />



sed -n -e '2,/Joe/p' file23
## OUTPUT

<img width="1191" alt="sed7" src="https://github.com/user-attachments/assets/cb089d7e-ae48-4d2e-897a-ad7b1cec56b5" />



sed -n -e '/tom/,/Joe/p' file23
## OUTPUT

<img width="1191" alt="sed8" src="https://github.com/user-attachments/assets/5b41966d-aae6-403b-b636-8a59c5195918" />


seq 10 
## OUTPUT

<img width="1191" alt="seq1" src="https://github.com/user-attachments/assets/d2d79471-6bde-4777-9657-136e0f248791" />


seq 10 | sed -n '4,6p'
## OUTPUT

<img width="1191" alt="seq2" src="https://github.com/user-attachments/assets/846623a8-eedd-4b94-a610-680c6178279b" />


seq 10 | sed -n '2,~4p'
## OUTPUT

<img width="1191" alt="seq3" src="https://github.com/user-attachments/assets/576c416c-6a8d-49b8-a403-94928e39e8e2" />


seq 3 | sed '2a hello'
## OUTPUT

<img width="1191" alt="seq4" src="https://github.com/user-attachments/assets/a0d1d2a0-8ee5-48f8-a26c-01837f8bf504" />


seq 2 | sed '2i hello'
## OUTPUT
<img width="1191" alt="seq5" src="https://github.com/user-attachments/assets/4136f92e-76f1-482b-8c1b-98bacd52a44b" />


seq 10 | sed '2,9c hello'
## OUTPUT

<img width="1191" alt="seq6" src="https://github.com/user-attachments/assets/7572a7c5-b120-404a-944a-a0fb44a34c39" />

sed -n '2,4{s/^/$/;p}' file23
## OUTPUT
<img width="1191" alt="seq7" src="https://github.com/user-attachments/assets/fee93d2b-e820-405d-829c-cb3ac77d6913" />



sed -n '2,4{s/$/*/;p}' file23

<img width="1191" alt="seq8" src="https://github.com/user-attachments/assets/d315d25b-0171-4c89-bf27-598b2ce1de6e" />


#Sorting File content
cat > file21
```
1001 | Ram | 10000 | HR
1002 | tom |  5000 | Admin
1003 | Joe |  7000 | Developer
1005 | Sam |  5000 | HR
1004 | Sit |  7000 | Dev
``` 
sort file21
## OUTPUT
<img width="1191" alt="sort" src="https://github.com/user-attachments/assets/5333cc08-329e-4da2-8233-3095e90b7d7a" />


cat > file22
```
1001 | Ram | 10000 | HR
1001 | Ram | 10000 | HR
1002 | tom |  5000 | Admin
1003 | Joe |  7000 | Developer
1005 | Sam |  5000 | HR
1004 | Sit |  7000 | Dev
``` 
uniq file22
## OUTPUT

<img width="1191" alt="uniq" src="https://github.com/user-attachments/assets/245bb0b0-0255-4f81-8d8b-c4d29b50d05a" />


#Using tr command

cat file23 | tr [:lower:] [:upper:]
 ## OUTPUT


<img width="1220" alt="catfile23" src="https://github.com/user-attachments/assets/b0085bbf-9a45-402f-b14c-ece48e2602fe" />

cat < urllist.txt
```
www. yahoo. com
www. google. com
www. mrcet.... com
^d
 ```
cat > urllist.txt
```
www. yahoo. com
www. google. com
www. mrcet.... com
 ```
cat urllist.txt | tr -d ' '
 ## OUTPUT
<img width="1150" alt="caturl1" src="https://github.com/user-attachments/assets/e03f12ce-785a-45ef-9624-4563248f0b34" />


 
cat urllist.txt | tr -d ' ' | tr -s '.'
## OUTPUT

<img width="1262" alt="caturl2" src="https://github.com/user-attachments/assets/ccc45ef6-7b2e-49e5-bb75-ebbac286edd5" />


#Backup commands
tar -cvf backup.tar *
## OUTPUT
<img width="983" alt="tar1" src="https://github.com/user-attachments/assets/7dda13ca-4234-4c36-a5c9-adb5ec42b766" />





mkdir backupdir
 
mv backup.tar backupdir
 
tar -tvf backup.tar
## OUTPUT

<img width="983" alt="mv1" src="https://github.com/user-attachments/assets/6b40597b-d048-42ce-934a-818b56688bce" />



tar -xvf backup.tar
## OUTPUT


<img width="983" alt="tar2" src="https://github.com/user-attachments/assets/fe693983-4dbf-4cdf-8152-65628495ab33" />

gzip backup.tar

ls .gz
## OUTPUT
 <img width="983" alt="ls1" src="https://github.com/user-attachments/assets/876904f8-34e8-4580-b53a-ffeb3af31649" />

gunzip backup.tar.gz
## OUTPUT
<img width="1112" alt="ls2" src="https://github.com/user-attachments/assets/aa3cc13c-ba98-4aeb-939f-a4606374ff64" />

 
# Shell Script
```
echo '#!/bin/sh' > my-script.sh
echo 'echo Hello World‘; exit 0 >> my-script.sh
```
chmod 755 my-script.sh
./my-script.sh
## OUTPUT
<img width="1303" alt="echo1" src="https://github.com/user-attachments/assets/326b813b-3add-459f-b2fd-338b43528e77" />

 
cat << stop > herecheck.txt
```
hello in this world
i cant stop
for this non stop movement
stop
```

cat herecheck.txt
## OUTPUT

<img width="1303" alt="catherecheck" src="https://github.com/user-attachments/assets/5c12b41c-eee4-4d2e-8349-cf8bb6a94019" />

cat < scriptest.sh 
```bash
\#!/bin/sh
echo “File name is $0 ”
echo "File name is " `basename $0`
echo “First arg. is ” $1
echo “Second arg. is ” $2
echo “Third arg. is ” $3
echo “Fourth arg. is ” $4
echo 'The $@ is ' $@
echo 'The $\# is ' $1#
echo 'The $$ is ' $$
ps
^d
 ```

cat scriptest.sh 
```bash
\#!/bin/sh
echo “File name is $0 ”
echo "File name is " `basename $0`
echo “First arg. is ” $1
echo “Second arg. is ” $2
echo “Third arg. is ” $3
echo “Fourth arg. is ” $4
echo 'The $@ is ' $@
echo 'The $\# is ' $\#
echo 'The $$ is ' $$
ps
```
 
chmod 777 scriptest.sh
 
./scriptest.sh 1 2 3

## OUTPUT
<img width="1303" alt="catscriptcheck" src="https://github.com/user-attachments/assets/a1d01a1b-620c-49f0-af5c-b40f49969e3e" />

 
ls file1
## OUTPUT
<img width="1303" alt="ls_1" src="https://github.com/user-attachments/assets/91dbf86e-7838-4f5a-b9eb-1e397b632533" />

echo $?
## OUTPUT 

<img width="1303" alt="echo_3" src="https://github.com/user-attachments/assets/1feae372-1cc6-402a-9c5c-f3be43581725" />

./one
bash: ./one: Permission denied
 
echo $?
## OUTPUT 
 <img width="1303" alt="echo_3" src="https://github.com/user-attachments/assets/3386c71f-9b56-4054-8d20-c32b458ff88a" />

abcd
 
echo $?
 ## OUTPUT

<img width="1303" alt="echo_2" src="https://github.com/user-attachments/assets/b3c78bca-e8d4-467d-87fe-0413e4ae6b9c" />

 
# mis-using string comparisons

cat < strcomp.sh 
```bash
\#!/bin/bash
val1=baseball
val2=hockey
if [ $val1 \> $val2 ]
then
echo "$val1 is greater than $val2"
else
echo "$val1 is less than $val2"
fi
^d
```

cat strcomp.sh 
```bash
\#!/bin/bash
val1=baseball
val2=hockey
if [ $val1 \> $val2 ]
then
echo "$val1 is greater than $val2"
else
echo "$val1 is less than $val2"
fi
```
##OUTPUT

<img width="1303" alt="cat_Strcmp" src="https://github.com/user-attachments/assets/ef3087fe-ada2-4949-8add-8535c550bbfb" />


chmod 755 strcomp.sh
 
./strcomp.sh 
## OUTPUT

<img width="1303" alt="strcmp" src="https://github.com/user-attachments/assets/c90593e2-4593-47b0-a659-84b7b0694bfa" />

# check file ownership
cat < psswdperm.sh 
```bash
\#!/bin/bash
if [ -O /etc/passwd ]
then
echo “You are the owner of the /etc/passwd file”
else
echo “Sorry, you are not the owner of the /etc/passwd file”
fi
^d
```

cat psswdperm.sh 
```bash
/#!/bin/bash
if [ -O /etc/passwd ]
then
echo “You are the owner of the /etc/passwd file”
else
echo “Sorry, you are not the owner of the /etc/passwd file”
fi
 ```
./psswdperm.sh
## OUTPUT
<img width="1303" alt="psswdperm" src="https://github.com/user-attachments/assets/0a51caa3-16be-4d68-99cb-0e6f1a0dd884" />

# check if with file location
cat>ifnested.sh 
```bash
\#!/bin/bash
if [ -e $HOME ]
then
echo “$HOME The object exists, is it a file?”
if [ -f $HOME ]
then
echo “Yes,$HOME it is a file!”
else
echo “No,$HOME it is not a file!”
if [ -f $HOME/.bash_history ]
then
echo “But $HOME/.bash_history is a file!”
fi
fi
else
echo “Sorry, the object does not exist”
fi
^d
```
cat ifnested.sh 
```
\#!/bin/bash
if [ -e $HOME ]
then
echo “$HOME The object exists, is it a file?”
if [ -f $HOME ]
then
echo “Yes,$HOME it is a file!”
else
echo “No,$HOME it is not a file!”
if [ -f $HOME/.bash_history ]
then
echo “But $HOME/.bash_history is a file!”
fi
fi
else
echo “Sorry, the object does not exist”
fi
```

./ifnested.sh 
## OUTPUT
<img width="1303" alt="ifnested" src="https://github.com/user-attachments/assets/3da26632-b35a-4002-badf-4eb936d859fc" />



# using numeric test comparisons
cat > iftest.sh 
```bash
\#!/bin/bash
val1=10
val2=11
if [ $val1 -gt 5 ]
then
echo “The test value $val1 is greater than 5”
fi
if [ $val1 -eq $val2 ]
then
echo “The values are equal”
else
echo “The values are different”
fi
^d
```


cat iftest.sh 
```bash
\#!/bin/bash
val1=10
val2=11
if [ $val1 -gt 5 ]
then
echo “The test value $val1 is greater than 5”
fi
if [ $val1 -eq $val2 ]
then
echo “The values are equal”
else
echo “The values are different”
fi
```

$ chmod 755 iftest.sh
 
$ ./iftest.sh 
##OUTPUT
<img width="1303" alt="iftest" src="https://github.com/user-attachments/assets/d3707e4f-5b05-4165-b7c4-54d71467dbe3" />

# check if a file
cat > ifnested.sh 
```bash
\#!/bin/bash
if [ -e $HOME ]
then
echo “$HOME The object exists, is it a file?”
if [ -f $HOME ]
then
echo “Yes,$HOME it is a file!”
else
echo “No,$HOME it is not a file!”
if [ -f $HOME/.bash_history ]
then
echo “But $HOME/.bash_history is a file!”
fi
fi
else
echo “Sorry, the object does not exist”
fi
^d
```

cat ifnested.sh 
```bash
\#!/bin/bash
if [ -e $HOME ]
then
echo “$HOME The object exists, is it a file?”
if [ -f $HOME ]
then
echo “Yes,$HOME it is a file!”
else
echo “No,$HOME it is not a file!”
if [ -f $HOME/.bash_history ]
then
echo “But $HOME/.bash_history is a file!”
fi
fi
else
echo “Sorry, the object does not exist”
fi
```

$ chmod 755 ifnested.s
$ ./ifnested.sh 
##OUTPUT

<img width="1303" alt="ifnested" src="https://github.com/user-attachments/assets/03b3d541-ae43-49fe-a679-b8bf018815f1" />


# looking for a possible value using elif
cat elifcheck.sh 
```bash
\#!/bin/bash
if [ $USER = Ram ]

then
echo "Welcome $USER"
echo "Please enjoy your visit"
elif [ $USER = Rahim ]
then
echo "Welcome $USER"
echo "Please enjoy your visit"
elif [ $USER = Robert ]
then
echo "Special testing account"
elif [ $USER = gganesh ]
then
echo "$USER, Do not forget to logout when you're done"
else
echo "Sorry, you are not allowed here"
fi
```

$ chmod 755 elifcheck.sh
 
$ ./elifcheck.sh 
## OUTPUT
<img width="1303" alt="elifcheck" src="https://github.com/user-attachments/assets/b1919683-5d80-4cbb-8c3a-01a1e6ea0afa" />




# testing compound comparisons
cat> ifcompound.sh 
```bash
\#!/bin/bash
if [ -d $HOME ] && [ -w $HOME ]
then
echo "The file exists and you can write to it"
else
echo "I cannot write to the file"
fi
```
$ chmod 755 ifcompound.sh
$ ./ifcompound.sh 
## OUTPUT

<img width="1303" alt="ifcompound" src="https://github.com/user-attachments/assets/9bc65215-3ed3-443c-9bf8-59c2fea04b30" />


# using the case command
cat >casecheck.sh 
```bash
case $USER in
Ram | Robert)
echo "Welcome, $USER"
echo "Please enjoy your visit";;
Rahim)
echo "Special testing account";;
gganesh)
echo "$USER, Do not forget to log off when you're done";;
*)
echo "Sorry, you are not allowed here";;
esac
```
$ chmod 755 casecheck.sh 
 
$ ./casecheck.sh 
 <img width="1303" alt="casecheck" src="https://github.com/user-attachments/assets/de882c6a-f548-4fbe-8eb7-f3e11aa3f7a4" />

cat > whiletest
```bash
#!/bin/bash
#while command test
var1=10
while [ $var1 -gt 0 ]
do
echo $var1
var1=$[ $var1 - 1 ]
done
```
$ chmod 755 whiletest.sh
 
$ ./whiletest.sh
 <img width="1303" alt="whiletest" src="https://github.com/user-attachments/assets/46ef979e-69bf-4c0b-b3c2-d4c696605c94" />

 
cat untiltest.sh 
```bash
\#using the until command
var1=100
until [ $var1 -eq 0 ]
do
echo $var1
var1=$[ $var1 - 25 ]
done
``` 
$ chmod 755 untiltest.sh
 
 
 <img width="1303" alt="untiltest" src="https://github.com/user-attachments/assets/3f62dc3a-31bb-4eb0-a6c7-8529d13fce33" />

cat forin1.sh 
```bash
\#!/bin/bash
\#basic for command
for test in Alabama Alaska Arizona Arkansas California Colorado
do
echo The next state is $test
done
 ```
 
$ chmod 755 forin1.sh
 <img width="1303" alt="forin1" src="https://github.com/user-attachments/assets/a888656f-4867-4a46-9750-3b4272408f5b" />

 
cat forin2.sh 
```bash
\#!/bin/bash
\# another example of how not to use the for command
for test in I don't know if this'll work
do
echo “word:$test”
done
 ```
 
$ chmod 755 forin2.sh
 <img width="1303" alt="forin1" src="https://github.com/user-attachments/assets/7bb432e5-d9ee-4599-bf13-5438cc5f4e6e" />

cat forin2.sh 
```bash
\#!/bin/bash
\# another example of how not to use the for command
for test in I don't know if this'll work
do
echo “word:$test”
done
```
$ chmod 755 forin2.sh
 
$ ./forin2.sh 
 <img width="1303" alt="forin2" src="https://github.com/user-attachments/assets/237ad428-e9b7-4ac3-821e-3da854d3074d" />

cat forin3.sh 
```bash
\#!/bin/bash
\# another example of how not to use the for command
for test in I don\'t know if "this'll" work
do
echo "word:$test"
done
```
$ ./forin3.sh 
<img width="1303" alt="forin3" src="https://github.com/user-attachments/assets/13b0597a-c4e7-4911-bc4b-aacde0ab3821" />


 
cat forin1.sh 
```bash
#!/bin/bash
# basic for command
for test in Alabama Alaska Arizona Arkansas California Colorado
do
echo The next state is $test
done
```
$ chmod 755 forin1.sh

## OUTPUT

cat forinfile.sh 
```bash
#!/bin/bash
# reading values from a file
file="cities"
for state in `cat $file`
do
echo "Visit beautiful $file“
done
```
$ chmod 777 forinfile.sh
$ cat cities
Hyderabad
Alampur
Basara
Warangal
Adilabad
Bhadrachalam
Khammam

## OUTPUT


cat forctype.sh 
```bash
#!/bin/bash
# testing the C-style for loop
for (( i=1; i <= 5; i++ ))
do
echo "The value of i is $i"
done
````
$ chmod 755 forctype.sh
$ .
/forctype.sh 
## OUTPUT

<img width="1303" alt="forctype" src="https://github.com/user-attachments/assets/d025e8ab-8914-4773-b7b8-20af63ecd3a2" />


cat forctype1.sh 
```bash
#!/bin/bash
# multiple variables
for (( a=1, b=5; a <= 5; a++, b-- ))
do
echo "$a - $b"
done
```

$ chmod 755 forctype.sh
$ ./forctype1.sh 
## OUTPUT

<img width="1303" alt="forctype1" src="https://github.com/user-attachments/assets/4f1d5d1c-9596-47ef-9846-241cfbf36477" />


cat fornested1.sh 
```bash
#!/bin/bash
# nesting for loops
for (( a = 1; a <= 3; a++ ))
do
echo "Starting loop $a:"
for (( b = 1; b <= 3; b++ ))
do
echo " Inside loop: $b"
done
done
```
$ chmod 755 fornested1.sh
 
$ ./fornested1.sh 
 ## OUTPUT

 <img width="1303" alt="forneseted1" src="https://github.com/user-attachments/assets/5dab4256-25ff-4602-a718-93d078bc5b83" />

cat forbreak.sh 
```bash

#!/bin/bash
# breaking out of a for loop
for var1 in 1 2 3 4 5
do
if [ $var1 -eq 3 ]
then
break
fi
echo "Iteration number: $var1"
done
echo "The for loop is completed“


$ chmod 755 forbreak.sh
 
$ ./forbreak.sh 
 
 <img width="1303" alt="forbreak" src="https://github.com/user-attachments/assets/3431b61f-2c18-4009-ac0b-7ffd295f6d2d" />

cat forbreak.sh 
```bash
#!/bin/bash
# breaking out of a for loop
for var1 in 1 2 3 4 5
do
if [ $var1 -eq 3 ]
then
continue
fi
echo "Iteration number: $var1"
done
echo "The for loop is completed“
```

 
$ chmod 755 forcontinue.sh
 
$ ./forcontinue.sh 
## OUTPUT
 
 <img width="1303" alt="forcontinue" src="https://github.com/user-attachments/assets/2c3004a2-8341-49fe-99d2-7d733e2d738f" />

cat exread.sh 
```bash
#!/bin/bash
# testing the read command
echo -n "Enter your name: "
read name
echo "Hello $name, welcome to my program. "
 ```
 
$ chmod 755 exread.sh 
 
$ ./exread.sh 
## OUTPUT
<img width="1303" alt="exread" src="https://github.com/user-attachments/assets/67e32e61-c7fe-41e2-8a25-6d7f5083b7e4" />


 cat exread1.sh
```bash
#!/bin/bash
# testing the read command
read -p "Enter your name: " name
echo "Hello $name, welcome to my program. “
``` 
$ chmod 755 exread1.sh$ ./exread1.sh 
 <img width="1303" alt="exread1" src="https://github.com/user-attachments/assets/54d08463-e8d4-44e0-a8b5-fe2769e83721" />

cat funcex.sh

```bash
#!/bin/bash
# trying to access script parameters inside a function
function func {
echo $[ $1 * $2 ]
}
if [ $# -eq 2 ]
then
value=`func $1 $2`
echo "The result is $value"
else
echo "Usage: badtest1 a b"
fi
```
## OUTPUT
 ./funcex.sh 

 <img width="1303" alt="funcex" src="https://github.com/user-attachments/assets/40654afd-9dbe-402d-8eee-49993bd05766" />

 ./funcex.sh 1 2
<img width="1303" alt="funcex123" src="https://github.com/user-attachments/assets/36b0ca02-3fff-4225-b684-e0f9cba56ec4" />

 
cat argshift.sh
```bash
#!/bin/bash 
 while (( "$#" )); do 
  echo $1 
  shift 
done
```
$ chmod 777 argshift.sh

## OUTPUT
$ ./argshift.sh 1 2 3

<img width="1303" alt="argshift" src="https://github.com/user-attachments/assets/6ab174df-28db-4227-a7c0-437897d6c105" />

 
 cat argshift1.sh
```bash
 #/bin/bash 
 # store arguments in a special array 
args=("$@") 
# get number of elements 
ELEMENTS=${#args[@]} 
 # echo each element in array  
# for loop 
for (( i=0;i<$ELEMENTS;i++)); do 
    echo ${args[${i}]} 
done
```
$ chmod 777 argshift.sh
## OUTPUT
<img width="1303" alt="argshift1" src="https://github.com/user-attachments/assets/68844e48-a0f0-4f21-8755-f08681b35ebe" />



$ ./argshift.sh 1 2 3
 
cat argshift.sh
```bash
#!/bin/bash 
set -x 
while (( "$#" )); do 
  echo $1 
  shift 
done
set +x
```
## OUTPUT
 ./argshift.sh 1 2 3
 <img width="1303" alt="argshift3" src="https://github.com/user-attachments/assets/0c1a0221-6aa6-4d54-a7bf-f1dd413f5f54" />

 
cat > nc.awk
```bash
BEGIN{}
{
print len=length($0),"\t",$0 
wordcount+=NF
chrcnt+=len
}
END {
print "total characters",chrcnt 
print "Number of Lines are",NR
print "No of Words count:",wordcount
}
 ```
cat>data.dat
```bash
bcdfghj
abcdfghj
bcdfghj
ebcdfghj
bcdfghj
ibcdfghj
bcdfghj
obcdfghj
bcdfghj
ubcdfghj
```
awk -f nc.awk data.dat
## OUTPUT 
<img width="1303" alt="awk" src="https://github.com/user-attachments/assets/ae636339-1207-4ec2-8669-e590f9fad49c" />

 
cat > palindrome.sh
```bash
#num=545
echo "Enter the number"
read num
s=0
rev=""
temp=$num
while [ $num -gt 0 ]
do
	# Get Remainder
	s=$(( $num % 10 ))
	# Get next digit
	num=$(( $num / 10 ))
	# Store previous number and
	# current digit in reverse
	rev=$( echo ${rev}${s} )
done
if [ $temp -eq $rev ];
then
	echo "Number is palindrome"
else
	echo "Number is NOT palindrome"
fi
```
## OUTPUT 
<img width="1303" alt="pallindrome" src="https://github.com/user-attachments/assets/b32df0c4-a18c-4a9e-81f7-d3036a27a88e" />


# RESULT:
The Commands are executed successfully.

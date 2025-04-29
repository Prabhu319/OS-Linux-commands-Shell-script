# OS-Linux-commands-Shell-scripting
Operating systems Lab exercise
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
## OUTPUT

![1](https://github.com/user-attachments/assets/967a622c-6563-4855-ab6e-bd33f3e1a973)


cat < file2
## OUTPUT

![2](https://github.com/user-attachments/assets/9cb30c01-6ca1-4508-b567-920317d92ce7)


# Comparing Files
cmp file1 file2
## OUTPUT
 ![3](https://github.com/user-attachments/assets/356f08aa-5611-4bb9-bc5e-02c43c13d403)

comm file1 file2
 ## OUTPUT
![4](https://github.com/user-attachments/assets/9b4f494f-3764-4004-89a7-b6554328d7c4)

 
diff file1 file2
## OUTPUT
![5](https://github.com/user-attachments/assets/dfe29c5f-7b65-4a49-b361-9bd4c5cb9430)


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

![6](https://github.com/user-attachments/assets/f1d13611-bbec-432e-b9cb-85ffb7538742)



cut -d "|" -f 1 file22
## OUTPUT
![7](https://github.com/user-attachments/assets/be89e8ec-8d82-46ca-90f7-516446ea7551)



cut -d "|" -f 2 file22
## OUTPUT
![8](https://github.com/user-attachments/assets/06251dfd-c2e1-4033-b83c-699161f82a7d)


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

![9](https://github.com/user-attachments/assets/027acbdf-56a3-46b0-862e-dadefb65295a)


grep hello newfile 
## OUTPUT

![10](https://github.com/user-attachments/assets/66c88133-9569-4d73-a191-9b74b320b70c)



grep -v hello newfile 
## OUTPUT

![11](https://github.com/user-attachments/assets/54d7af23-a79e-46cb-b549-57664f1d5c57)


cat newfile | grep -i "hello"
## OUTPUT

![12](https://github.com/user-attachments/assets/415d2950-f5c4-4d72-9a82-4eada399247b)



cat newfile | grep -i -c "hello"
## OUTPUT

![13](https://github.com/user-attachments/assets/45757001-bf07-41a0-9ca0-f7d1ed2b84ab)



grep -R ubuntu /etc
## OUTPUT

![14](https://github.com/user-attachments/assets/41e662bb-ca4d-4dd5-94e5-10cf130c572d)


grep -w -n world newfile   
## OUTPUT

![15](https://github.com/user-attachments/assets/2959a482-0122-46d1-9c2b-bcf9d17cc219)

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
![16](https://github.com/user-attachments/assets/78d128c6-04bc-40c6-bf8e-d8abbf76b086)



egrep -w '(H|h)ello' newfile 
## OUTPUT

![17](https://github.com/user-attachments/assets/4bf9423d-4115-4702-b77d-652036301cc0)


egrep -w '(H|h)ell[a-z]' newfile 
## OUTPUT

![18](https://github.com/user-attachments/assets/14924440-952c-480e-83e3-68d0742c897f)



egrep '(^hello)' newfile 
## OUTPUT

![19](https://github.com/user-attachments/assets/1d2da7f4-7edd-4697-a5ab-08b3b15cbe93)


egrep '(world$)' newfile 
## OUTPUT

![20](https://github.com/user-attachments/assets/f8d8366d-ded2-41eb-83e4-ebdfba968dd2)


egrep '(World$)' newfile 
## OUTPUT

![21](https://github.com/user-attachments/assets/3c0717c6-f676-4ea9-b28f-8850ea51a52c)

egrep '((W|w)orld$)' newfile 
## OUTPUT

![22](https://github.com/user-attachments/assets/f9c9d21b-2bc4-4b7d-8585-ac393785db8b)


egrep '[1-9]' newfile 
## OUTPUT

![23](https://github.com/user-attachments/assets/df7c6665-f757-49cb-ac27-e218c651c7fe)


egrep 'Linux.*world' newfile 
## OUTPUT

![24](https://github.com/user-attachments/assets/e6f5f5cc-1313-415b-babd-30bf5c4828b9)

egrep 'Linux.*World' newfile 
## OUTPUT
![25](https://github.com/user-attachments/assets/af4ce7ef-128f-4e4a-b1c9-6fe459f9cc59)


egrep l{2} newfile
## OUTPUT

![26](https://github.com/user-attachments/assets/b8033a58-9387-4802-8ae1-e082b998bf40)


egrep 's{1,2}' newfile
## OUTPUT 

![27](https://github.com/user-attachments/assets/31237cb8-66ad-42f9-a942-5bd7478096c1)

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

![28](https://github.com/user-attachments/assets/7b94549c-1754-4c4c-8d1c-3b4ef4057d90)


sed -n -e '$p' file23
## OUTPUT

![29](https://github.com/user-attachments/assets/d6c1017b-dcfe-4ba2-9968-6fd515f70ccc)


sed  -e 's/Ram/Sita/' file23
## OUTPUT

![30](https://github.com/user-attachments/assets/defc7fe9-c3e9-43e5-9466-e52556533f6e)


sed  -e '2s/Ram/Sita/' file23
## OUTPUT

![31](https://github.com/user-attachments/assets/592fe0f8-f473-480d-afae-21201455bd13)


sed  '/tom/s/5000/6000/' file23
## OUTPUT

![32](https://github.com/user-attachments/assets/29a39431-6510-4cfa-97e7-4bcc7ff0899a)


sed -n -e '1,5p' file23
## OUTPUT

![33](https://github.com/user-attachments/assets/b575e87f-9fb9-45a2-adb0-094b8315abb1)


sed -n -e '2,/Joe/p' file23
## OUTPUT

![34](https://github.com/user-attachments/assets/b6783de6-e36c-48db-9ee8-1089bd9f6e99)



sed -n -e '/tom/,/Joe/p' file23
## OUTPUT

![35](https://github.com/user-attachments/assets/523a4b3c-1180-4cf8-8e3e-b7663c01c022)


seq 10 
## OUTPUT

![36](https://github.com/user-attachments/assets/4f177b06-7938-4755-9924-6a3464e1bcc4)


seq 10 | sed -n '4,6p'
## OUTPUT

![37](https://github.com/user-attachments/assets/c722792b-646b-4b85-9124-a8f20ef42d96)


seq 10 | sed -n '2,~4p'
## OUTPUT

![38](https://github.com/user-attachments/assets/330d96a5-d3d9-4a7f-beee-12e46a4ad98f)


seq 3 | sed '2a hello'
## OUTPUT

![39](https://github.com/user-attachments/assets/805a4134-3397-4783-be68-6d1d061c650c)


seq 2 | sed '2i hello'
## OUTPUT

![40](https://github.com/user-attachments/assets/c59f4705-58a5-47ff-b223-06733cbcb06e)

seq 10 | sed '2,9c hello'
## OUTPUT

![41](https://github.com/user-attachments/assets/9395f677-52f8-4f75-b137-adcc767a2519)


sed -n '2,4{s/^/$/;p}' file23
## OUTPUT

![42](https://github.com/user-attachments/assets/4f70c8ec-cc80-47a2-8095-4215f0fa18f2)


sed -n '2,4{s/$/*/;p}' file23

![43](https://github.com/user-attachments/assets/da603a99-e502-4770-8fc3-bb2ad1a032db)

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

![44](https://github.com/user-attachments/assets/66fa5f6e-5852-46e9-b870-b38b84b512e6)

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

![45](https://github.com/user-attachments/assets/787b56a3-f849-4513-a704-237e72aa2ac6)


#Using tr command

cat file23 | tr [:lower:] [:upper:]
 ## OUTPUT

![46](https://github.com/user-attachments/assets/2381e510-0bf0-4450-bc39-de38ea034bb9)

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

![48](https://github.com/user-attachments/assets/098afbcc-076c-4f85-b9d6-c51cf0fb0d46)

 
cat urllist.txt | tr -d ' ' | tr -s '.'
## OUTPUT

![49](https://github.com/user-attachments/assets/62e2fa63-7f75-481d-b9b0-cbd070534217)


#Backup commands
tar -cvf backup.tar *
## OUTPUT

![50](https://github.com/user-attachments/assets/c28c08b3-4839-4fa5-af49-da520d25b9f4)
mkdir backupdir
 
mv backup.tar backupdir
 
tar -tvf backup.tar
## OUTPUT

![51](https://github.com/user-attachments/assets/95ee4d5e-81f5-46aa-b221-9d84cf353090)

tar -xvf backup.tar
## OUTPUT

![52](https://github.com/user-attachments/assets/a3ea4426-447a-423d-b238-37cfd64a32c2)


gzip backup.tar

ls .gz
## OUTPUT

 ![53](https://github.com/user-attachments/assets/0f4f0e96-53c3-4e67-ae22-3ff83d31cdad)

gunzip backup.tar.gz
## OUTPUT

 ![54](https://github.com/user-attachments/assets/1545a8ab-15b6-4fea-b67c-d6778656d289)

# Shell Script
```
echo '#!/bin/sh' > my-script.sh
echo 'echo Hello World‘; exit 0 >> my-script.sh
```
chmod 755 my-script.sh
./my-script.sh
## OUTPUT

![55](https://github.com/user-attachments/assets/2cb093bc-b1c0-4927-9f44-8648e99bdee7)


cat << stop > herecheck.txt
```
hello in this world
i cant stop
for this non stop movement
stop
```

cat herecheck.txt
## OUTPUT

![56](https://github.com/user-attachments/assets/6503d8ea-f020-4a33-bc54-d80d3bc44a30)

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

 ![57](https://github.com/user-attachments/assets/5eb11545-912f-44d6-bff7-fbc0cfbe09fe)

ls file1
## OUTPUT

![58](https://github.com/user-attachments/assets/8e0c0b06-7fa2-404f-8f27-57da942b2b3f)

echo $?
## OUTPUT 
./one
bash: ./one: Permission denied

 ![59](https://github.com/user-attachments/assets/fa3cc91f-4dc8-4c9c-b285-58fe15eead88)

abcd
 
echo $?
 ## OUTPUT

![60](https://github.com/user-attachments/assets/f01acb5d-8c5e-4542-8978-82bfef0a3ea5)

 
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

![61](https://github.com/user-attachments/assets/6b566efb-6d31-498e-9c54-72874711055e)

chmod 755 strcomp.sh
 
./strcomp.sh 
## OUTPUT

![62](https://github.com/user-attachments/assets/83070a40-be1d-4d2a-9c54-3ef580be930a)

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

![63](https://github.com/user-attachments/assets/9b815b7d-899c-4084-be1a-1a71b889e898)

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

![64](https://github.com/user-attachments/assets/3d1162a1-7204-4f55-97b5-b77317da78f6)


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
## OUTPUT

![65](https://github.com/user-attachments/assets/d16f07c4-9edf-45f7-9286-86dd9ac47242)

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

$ chmod 755 ifnested.sh
 
$ ./ifnested.sh 
## OUTPUT

![66](https://github.com/user-attachments/assets/df476fb2-bedd-4247-a5bf-b6e4ee9cbc67)

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

![67](https://github.com/user-attachments/assets/fb6e93b7-597a-4a0d-ac44-6ae3c8006f04)

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

![68](https://github.com/user-attachments/assets/2ab8d86f-3071-40f3-a001-a61e19bd85ba)

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

 ![69](https://github.com/user-attachments/assets/f6846a1c-12ee-40bf-9922-0115741fd0c1)

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
 
![70](https://github.com/user-attachments/assets/e42d36e7-94c0-4d9a-bfab-6dce811876f2)

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
 
 ![71](https://github.com/user-attachments/assets/9cc518d6-6d3d-40b3-96ce-e07af2ba7387)

 
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
 
 ![72](https://github.com/user-attachments/assets/10a7b7fc-bc85-41ec-9d29-c49e824c0d45)

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

 ![73](https://github.com/user-attachments/assets/243b7eef-0e93-4b51-a93c-3af8a9284148)

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

 ![74](https://github.com/user-attachments/assets/c514697f-d795-4272-94cc-1e3b8945d19f)

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
$ ./forctype.sh 
## OUTPUT

![75](https://github.com/user-attachments/assets/7f28d4a7-d821-4e95-8f38-e8223113babc)

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

![76](https://github.com/user-attachments/assets/b26f7b95-3af3-4d24-a1ae-2a51477a4d19)

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

 ![77](https://github.com/user-attachments/assets/352b921d-9e6f-491c-a625-08f4181bad6d)

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
```
## OUTPUT

![78](https://github.com/user-attachments/assets/c103e0a5-3476-4c84-8cbd-f17b9bae9e2d)

$ chmod 755 forbreak.sh
 
$ ./forbreak.sh 
 
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

 ![79](https://github.com/user-attachments/assets/cf727495-c935-4877-b8c3-27a2f53f51c9)

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

![80](https://github.com/user-attachments/assets/2abd07e2-1944-4c70-a029-cd41d7f60800)

 cat exread1.sh
```bash
#!/bin/bash
# testing the read command
read -p "Enter your name: " name
echo "Hello $name, welcome to my program. “
``` 
$ chmod 755 exread1.sh 

## OUTPUT

![81](https://github.com/user-attachments/assets/fad684d9-006c-4bd7-bab5-50c8169f716b)


$ ./exread1.sh 
 
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

 
 ./funcex.sh 1 2

 
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

 ![82](https://github.com/user-attachments/assets/aae1f16d-9ff5-4d5b-8768-27f634a70e1f)

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

 ![83](https://github.com/user-attachments/assets/01d807d9-9604-47db-80e4-04d90919cbe0)

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

![84](https://github.com/user-attachments/assets/ee6e9199-b040-49fd-90ee-f769859de031)

# RESULT:
The Commands are executed successfully.
# OS-Linux-commands-Shell-scripting
Operating systems Lab exercise
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
## OUTPUT

![1](https://github.com/user-attachments/assets/967a622c-6563-4855-ab6e-bd33f3e1a973)


cat < file2
## OUTPUT

![2](https://github.com/user-attachments/assets/9cb30c01-6ca1-4508-b567-920317d92ce7)


# Comparing Files
cmp file1 file2
## OUTPUT
 ![3](https://github.com/user-attachments/assets/356f08aa-5611-4bb9-bc5e-02c43c13d403)

comm file1 file2
 ## OUTPUT
![4](https://github.com/user-attachments/assets/9b4f494f-3764-4004-89a7-b6554328d7c4)

 
diff file1 file2
## OUTPUT
![5](https://github.com/user-attachments/assets/dfe29c5f-7b65-4a49-b361-9bd4c5cb9430)


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

![6](https://github.com/user-attachments/assets/f1d13611-bbec-432e-b9cb-85ffb7538742)



cut -d "|" -f 1 file22
## OUTPUT
![7](https://github.com/user-attachments/assets/be89e8ec-8d82-46ca-90f7-516446ea7551)



cut -d "|" -f 2 file22
## OUTPUT
![8](https://github.com/user-attachments/assets/06251dfd-c2e1-4033-b83c-699161f82a7d)


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

![9](https://github.com/user-attachments/assets/027acbdf-56a3-46b0-862e-dadefb65295a)


grep hello newfile 
## OUTPUT

![10](https://github.com/user-attachments/assets/66c88133-9569-4d73-a191-9b74b320b70c)



grep -v hello newfile 
## OUTPUT

![11](https://github.com/user-attachments/assets/54d7af23-a79e-46cb-b549-57664f1d5c57)


cat newfile | grep -i "hello"
## OUTPUT

![12](https://github.com/user-attachments/assets/415d2950-f5c4-4d72-9a82-4eada399247b)



cat newfile | grep -i -c "hello"
## OUTPUT

![13](https://github.com/user-attachments/assets/45757001-bf07-41a0-9ca0-f7d1ed2b84ab)



grep -R ubuntu /etc
## OUTPUT

![14](https://github.com/user-attachments/assets/41e662bb-ca4d-4dd5-94e5-10cf130c572d)


grep -w -n world newfile   
## OUTPUT

![15](https://github.com/user-attachments/assets/2959a482-0122-46d1-9c2b-bcf9d17cc219)

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
![16](https://github.com/user-attachments/assets/78d128c6-04bc-40c6-bf8e-d8abbf76b086)



egrep -w '(H|h)ello' newfile 
## OUTPUT

![17](https://github.com/user-attachments/assets/4bf9423d-4115-4702-b77d-652036301cc0)


egrep -w '(H|h)ell[a-z]' newfile 
## OUTPUT

![18](https://github.com/user-attachments/assets/14924440-952c-480e-83e3-68d0742c897f)



egrep '(^hello)' newfile 
## OUTPUT

![19](https://github.com/user-attachments/assets/1d2da7f4-7edd-4697-a5ab-08b3b15cbe93)


egrep '(world$)' newfile 
## OUTPUT

![20](https://github.com/user-attachments/assets/f8d8366d-ded2-41eb-83e4-ebdfba968dd2)


egrep '(World$)' newfile 
## OUTPUT

![21](https://github.com/user-attachments/assets/3c0717c6-f676-4ea9-b28f-8850ea51a52c)

egrep '((W|w)orld$)' newfile 
## OUTPUT

![22](https://github.com/user-attachments/assets/f9c9d21b-2bc4-4b7d-8585-ac393785db8b)


egrep '[1-9]' newfile 
## OUTPUT

![23](https://github.com/user-attachments/assets/df7c6665-f757-49cb-ac27-e218c651c7fe)


egrep 'Linux.*world' newfile 
## OUTPUT

![24](https://github.com/user-attachments/assets/e6f5f5cc-1313-415b-babd-30bf5c4828b9)

egrep 'Linux.*World' newfile 
## OUTPUT
![25](https://github.com/user-attachments/assets/af4ce7ef-128f-4e4a-b1c9-6fe459f9cc59)


egrep l{2} newfile
## OUTPUT

![26](https://github.com/user-attachments/assets/b8033a58-9387-4802-8ae1-e082b998bf40)


egrep 's{1,2}' newfile
## OUTPUT 

![27](https://github.com/user-attachments/assets/31237cb8-66ad-42f9-a942-5bd7478096c1)

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

![28](https://github.com/user-attachments/assets/7b94549c-1754-4c4c-8d1c-3b4ef4057d90)


sed -n -e '$p' file23
## OUTPUT

![29](https://github.com/user-attachments/assets/d6c1017b-dcfe-4ba2-9968-6fd515f70ccc)


sed  -e 's/Ram/Sita/' file23
## OUTPUT

![30](https://github.com/user-attachments/assets/defc7fe9-c3e9-43e5-9466-e52556533f6e)


sed  -e '2s/Ram/Sita/' file23
## OUTPUT

![31](https://github.com/user-attachments/assets/592fe0f8-f473-480d-afae-21201455bd13)


sed  '/tom/s/5000/6000/' file23
## OUTPUT

![32](https://github.com/user-attachments/assets/29a39431-6510-4cfa-97e7-4bcc7ff0899a)


sed -n -e '1,5p' file23
## OUTPUT

![33](https://github.com/user-attachments/assets/b575e87f-9fb9-45a2-adb0-094b8315abb1)


sed -n -e '2,/Joe/p' file23
## OUTPUT

![34](https://github.com/user-attachments/assets/b6783de6-e36c-48db-9ee8-1089bd9f6e99)



sed -n -e '/tom/,/Joe/p' file23
## OUTPUT

![35](https://github.com/user-attachments/assets/523a4b3c-1180-4cf8-8e3e-b7663c01c022)


seq 10 
## OUTPUT

![36](https://github.com/user-attachments/assets/4f177b06-7938-4755-9924-6a3464e1bcc4)


seq 10 | sed -n '4,6p'
## OUTPUT

![37](https://github.com/user-attachments/assets/c722792b-646b-4b85-9124-a8f20ef42d96)


seq 10 | sed -n '2,~4p'
## OUTPUT

![38](https://github.com/user-attachments/assets/330d96a5-d3d9-4a7f-beee-12e46a4ad98f)


seq 3 | sed '2a hello'
## OUTPUT

![39](https://github.com/user-attachments/assets/805a4134-3397-4783-be68-6d1d061c650c)


seq 2 | sed '2i hello'
## OUTPUT

![40](https://github.com/user-attachments/assets/c59f4705-58a5-47ff-b223-06733cbcb06e)

seq 10 | sed '2,9c hello'
## OUTPUT

![41](https://github.com/user-attachments/assets/9395f677-52f8-4f75-b137-adcc767a2519)


sed -n '2,4{s/^/$/;p}' file23
## OUTPUT

![42](https://github.com/user-attachments/assets/4f70c8ec-cc80-47a2-8095-4215f0fa18f2)


sed -n '2,4{s/$/*/;p}' file23

![43](https://github.com/user-attachments/assets/da603a99-e502-4770-8fc3-bb2ad1a032db)

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

![44](https://github.com/user-attachments/assets/66fa5f6e-5852-46e9-b870-b38b84b512e6)

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

![45](https://github.com/user-attachments/assets/787b56a3-f849-4513-a704-237e72aa2ac6)


#Using tr command

cat file23 | tr [:lower:] [:upper:]
 ## OUTPUT

![46](https://github.com/user-attachments/assets/2381e510-0bf0-4450-bc39-de38ea034bb9)

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

![48](https://github.com/user-attachments/assets/098afbcc-076c-4f85-b9d6-c51cf0fb0d46)

 
cat urllist.txt | tr -d ' ' | tr -s '.'
## OUTPUT

![49](https://github.com/user-attachments/assets/62e2fa63-7f75-481d-b9b0-cbd070534217)


#Backup commands
tar -cvf backup.tar *
## OUTPUT

![50](https://github.com/user-attachments/assets/c28c08b3-4839-4fa5-af49-da520d25b9f4)
mkdir backupdir
 
mv backup.tar backupdir
 
tar -tvf backup.tar
## OUTPUT

![51](https://github.com/user-attachments/assets/95ee4d5e-81f5-46aa-b221-9d84cf353090)

tar -xvf backup.tar
## OUTPUT

![52](https://github.com/user-attachments/assets/a3ea4426-447a-423d-b238-37cfd64a32c2)


gzip backup.tar

ls .gz
## OUTPUT

 ![53](https://github.com/user-attachments/assets/0f4f0e96-53c3-4e67-ae22-3ff83d31cdad)

gunzip backup.tar.gz
## OUTPUT

 ![54](https://github.com/user-attachments/assets/1545a8ab-15b6-4fea-b67c-d6778656d289)

# Shell Script
```
echo '#!/bin/sh' > my-script.sh
echo 'echo Hello World‘; exit 0 >> my-script.sh
```
chmod 755 my-script.sh
./my-script.sh
## OUTPUT

![55](https://github.com/user-attachments/assets/2cb093bc-b1c0-4927-9f44-8648e99bdee7)


cat << stop > herecheck.txt
```
hello in this world
i cant stop
for this non stop movement
stop
```

cat herecheck.txt
## OUTPUT

![56](https://github.com/user-attachments/assets/6503d8ea-f020-4a33-bc54-d80d3bc44a30)

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

 ![57](https://github.com/user-attachments/assets/5eb11545-912f-44d6-bff7-fbc0cfbe09fe)

ls file1
## OUTPUT

![58](https://github.com/user-attachments/assets/8e0c0b06-7fa2-404f-8f27-57da942b2b3f)

echo $?
## OUTPUT 
./one
bash: ./one: Permission denied

 ![59](https://github.com/user-attachments/assets/fa3cc91f-4dc8-4c9c-b285-58fe15eead88)

abcd
 
echo $?
 ## OUTPUT

![60](https://github.com/user-attachments/assets/f01acb5d-8c5e-4542-8978-82bfef0a3ea5)

 
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

![61](https://github.com/user-attachments/assets/6b566efb-6d31-498e-9c54-72874711055e)

chmod 755 strcomp.sh
 
./strcomp.sh 
## OUTPUT

![62](https://github.com/user-attachments/assets/83070a40-be1d-4d2a-9c54-3ef580be930a)

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

![63](https://github.com/user-attachments/assets/9b815b7d-899c-4084-be1a-1a71b889e898)

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

![64](https://github.com/user-attachments/assets/3d1162a1-7204-4f55-97b5-b77317da78f6)


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
## OUTPUT

![65](https://github.com/user-attachments/assets/d16f07c4-9edf-45f7-9286-86dd9ac47242)

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

$ chmod 755 ifnested.sh
 
$ ./ifnested.sh 
## OUTPUT

![66](https://github.com/user-attachments/assets/df476fb2-bedd-4247-a5bf-b6e4ee9cbc67)

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

![67](https://github.com/user-attachments/assets/fb6e93b7-597a-4a0d-ac44-6ae3c8006f04)

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

![68](https://github.com/user-attachments/assets/2ab8d86f-3071-40f3-a001-a61e19bd85ba)

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

 ![69](https://github.com/user-attachments/assets/f6846a1c-12ee-40bf-9922-0115741fd0c1)

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
 
![70](https://github.com/user-attachments/assets/e42d36e7-94c0-4d9a-bfab-6dce811876f2)

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
 
 ![71](https://github.com/user-attachments/assets/9cc518d6-6d3d-40b3-96ce-e07af2ba7387)

 
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
 
 ![72](https://github.com/user-attachments/assets/10a7b7fc-bc85-41ec-9d29-c49e824c0d45)

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

 ![73](https://github.com/user-attachments/assets/243b7eef-0e93-4b51-a93c-3af8a9284148)

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

 ![74](https://github.com/user-attachments/assets/c514697f-d795-4272-94cc-1e3b8945d19f)

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
$ ./forctype.sh 
## OUTPUT

![75](https://github.com/user-attachments/assets/7f28d4a7-d821-4e95-8f38-e8223113babc)

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

![76](https://github.com/user-attachments/assets/b26f7b95-3af3-4d24-a1ae-2a51477a4d19)

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

 ![77](https://github.com/user-attachments/assets/352b921d-9e6f-491c-a625-08f4181bad6d)

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
```
## OUTPUT

![78](https://github.com/user-attachments/assets/c103e0a5-3476-4c84-8cbd-f17b9bae9e2d)

$ chmod 755 forbreak.sh
 
$ ./forbreak.sh 
 
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

 ![79](https://github.com/user-attachments/assets/cf727495-c935-4877-b8c3-27a2f53f51c9)

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

![80](https://github.com/user-attachments/assets/2abd07e2-1944-4c70-a029-cd41d7f60800)

 cat exread1.sh
```bash
#!/bin/bash
# testing the read command
read -p "Enter your name: " name
echo "Hello $name, welcome to my program. “
``` 
$ chmod 755 exread1.sh 

## OUTPUT

![81](https://github.com/user-attachments/assets/fad684d9-006c-4bd7-bab5-50c8169f716b)


$ ./exread1.sh 
 
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

 
 ./funcex.sh 1 2

 
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

 ![82](https://github.com/user-attachments/assets/aae1f16d-9ff5-4d5b-8768-27f634a70e1f)

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

 ![83](https://github.com/user-attachments/assets/01d807d9-9604-47db-80e4-04d90919cbe0)

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

![84](https://github.com/user-attachments/assets/ee6e9199-b040-49fd-90ee-f769859de031)

# RESULT:
The Commands are executed successfully.

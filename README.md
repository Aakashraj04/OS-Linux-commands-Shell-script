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

### Name : Aakashraj M
### Register Number : 212222100002

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

![image](https://github.com/Lathika2006/OS-Linux-commands-Shell-script/assets/148959215/645747f6-840a-4fb5-9bb8-3d37985808e1)


cat < file2
## OUTPUT

![image](https://github.com/Lathika2006/OS-Linux-commands-Shell-script/assets/148959215/4680c410-0f1a-417d-9f0d-05e417dff105)


# Comparing Files
cmp file1 file2
## OUTPUT

 ![image](https://github.com/Lathika2006/OS-Linux-commands-Shell-script/assets/148959215/b72ea53a-f252-420f-b008-c1db50733c87)

comm file1 file2
 ## OUTPUT

![image](https://github.com/Lathika2006/OS-Linux-commands-Shell-script/assets/148959215/9d8206de-18fe-42e7-98c7-f58a03d1e027)

 
diff file1 file2
## OUTPUT

![image](https://github.com/Lathika2006/OS-Linux-commands-Shell-script/assets/148959215/9db3fd92-ee1d-45f1-81b7-2421566f2f4a)


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

![image](https://github.com/Lathika2006/OS-Linux-commands-Shell-script/assets/148959215/b05fb00f-680e-478f-bf30-40e73ed3f8fc)





cut -d "|" -f 1 file22
## OUTPUT

![image](https://github.com/Lathika2006/OS-Linux-commands-Shell-script/assets/148959215/9b1db5ba-2294-4c27-93e3-04529c484132)


cut -d "|" -f 2 file22
## OUTPUT

![image](https://github.com/Lathika2006/OS-Linux-commands-Shell-script/assets/148959215/ac5c3093-ce26-4a44-8342-2861d83fe00c)


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

![image](https://github.com/Lathika2006/OS-Linux-commands-Shell-script/assets/148959215/c9dcc002-ec57-4d2a-ac12-b2118670b418)


grep hello newfile 
## OUTPUT

![image](https://github.com/Lathika2006/OS-Linux-commands-Shell-script/assets/148959215/1ba59f65-d89a-443c-b63e-658844690510)



grep -v hello newfile 
## OUTPUT

![image](https://github.com/Lathika2006/OS-Linux-commands-Shell-script/assets/148959215/7898aa37-f171-4dd3-b9bf-4821a7c66366)


cat newfile | grep -i "hello"
## OUTPUT


![image](https://github.com/Lathika2006/OS-Linux-commands-Shell-script/assets/148959215/b34be529-da32-4875-ada4-5403c4b2b219)


cat newfile | grep -i -c "hello"
## OUTPUT

![image](https://github.com/Lathika2006/OS-Linux-commands-Shell-script/assets/148959215/b68bbe48-76d8-4261-aea9-5b3525862b73)


grep -R ubuntu /etc
## OUTPUT

![image](https://github.com/Lathika2006/OS-Linux-commands-Shell-script/assets/148959215/c7641628-681a-431e-a85d-f9606f4a5cf5)


grep -w -n world newfile   
## OUTPUT

![image](https://github.com/Lathika2006/OS-Linux-commands-Shell-script/assets/148959215/ab89cc80-61df-49c7-b155-4a5e5172bb58)


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

![image](https://github.com/Lathika2006/OS-Linux-commands-Shell-script/assets/148959215/3fb6eac9-fb4a-4396-9418-c277da0ac7af)


egrep -w '(H|h)ello' newfile 
## OUTPUT

![image](https://github.com/Lathika2006/OS-Linux-commands-Shell-script/assets/148959215/15faa397-b760-4e38-88c5-46df8d1bdb60)


egrep -w '(H|h)ell[a-z]' newfile 
## OUTPUT

![image](https://github.com/Lathika2006/OS-Linux-commands-Shell-script/assets/148959215/cb5df577-6ca4-4fb2-a5b2-a1bbfc9342ff)



egrep '(^hello)' newfile 
## OUTPUT

![image](https://github.com/Lathika2006/OS-Linux-commands-Shell-script/assets/148959215/84e6db99-923d-4dcb-9d2f-f759f1d23029)


egrep '(world$)' newfile 
## OUTPUT

![image](https://github.com/Lathika2006/OS-Linux-commands-Shell-script/assets/148959215/3e4a7354-30a8-4a78-9ba7-ef3d7b9205cc)


egrep '(World$)' newfile 
## OUTPUT

![image](https://github.com/Lathika2006/OS-Linux-commands-Shell-script/assets/148959215/73eb50dd-a4e7-4231-93fd-3043957f5bb6)


egrep '((W|w)orld$)' newfile 
## OUTPUT

![image](https://github.com/Lathika2006/OS-Linux-commands-Shell-script/assets/148959215/10d9f5b0-41c6-4871-8acb-7c1bbfbefaaa)


egrep '[1-9]' newfile 
## OUTPUT

![image](https://github.com/Lathika2006/OS-Linux-commands-Shell-script/assets/148959215/56fd1f75-45fe-46f6-8ed2-f25c8c712aec)



egrep 'Linux.*world' newfile 
## OUTPUT

![image](https://github.com/Lathika2006/OS-Linux-commands-Shell-script/assets/148959215/7d6419cf-634f-4106-9a64-86fb2f8098c3)


egrep 'Linux.*World' newfile 
## OUTPUT

![image](https://github.com/Lathika2006/OS-Linux-commands-Shell-script/assets/148959215/1128e562-d671-4878-a83c-49a308d4f983)


egrep l{2} newfile
## OUTPUT

![image](https://github.com/Lathika2006/OS-Linux-commands-Shell-script/assets/148959215/da8d070f-5f44-421c-b63e-b08b08021b2d)


egrep 's{1,2}' newfile
## OUTPUT 

![image](https://github.com/Lathika2006/OS-Linux-commands-Shell-script/assets/148959215/c79a5769-68c8-4842-87e9-d9799398d1dc)


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

![image](https://github.com/Lathika2006/OS-Linux-commands-Shell-script/assets/148959215/d023edb3-6837-4065-98e9-08bb8b5d4360)


sed -n -e '$p' file23
## OUTPUT

![image](https://github.com/Lathika2006/OS-Linux-commands-Shell-script/assets/148959215/4c0977d9-7438-4ace-a89a-e0536e3c96b0)


sed  -e 's/Ram/Sita/' file23
## OUTPUT

![image](https://github.com/Lathika2006/OS-Linux-commands-Shell-script/assets/148959215/03ea1332-8ae5-4e5b-9f27-5f150319a13b)


sed  -e '2s/Ram/Sita/' file23
## OUTPUT

![image](https://github.com/Lathika2006/OS-Linux-commands-Shell-script/assets/148959215/54e0938a-b87e-4a52-a6d8-1d33b644ef58)


sed  '/tom/s/5000/6000/' file23
## OUTPUT

![image](https://github.com/Lathika2006/OS-Linux-commands-Shell-script/assets/148959215/f4539868-4ccb-480e-a828-de27371cc413)


sed -n -e '1,5p' file23
## OUTPUT

![image](https://github.com/Lathika2006/OS-Linux-commands-Shell-script/assets/148959215/61c2937f-7b06-4bae-828a-7e00818b5287)

sed -n -e '2,/Joe/p' file23
## OUTPUT


![image](https://github.com/Lathika2006/OS-Linux-commands-Shell-script/assets/148959215/07aa75ef-5b1e-4d5b-bfe5-7d36cb65c8d7)



sed -n -e '/tom/,/Joe/p' file23
## OUTPUT

![image](https://github.com/Lathika2006/OS-Linux-commands-Shell-script/assets/148959215/b3664d94-dc31-448c-88b1-e74cd741c96b)


seq 10 
## OUTPUT

![image](https://github.com/Lathika2006/OS-Linux-commands-Shell-script/assets/148959215/b51046e0-51df-4a04-97a3-9aff3b3929fd)


seq 10 | sed -n '4,6p'
## OUTPUT

![image](https://github.com/Lathika2006/OS-Linux-commands-Shell-script/assets/148959215/4ed9f3b2-3d9a-4859-a477-9c4d47247f26)


seq 10 | sed -n '2,~4p'
## OUTPUT

![image](https://github.com/Lathika2006/OS-Linux-commands-Shell-script/assets/148959215/a910466b-be1c-4335-8842-201a475247b6)


seq 3 | sed '2a hello'
## OUTPUT

![image](https://github.com/Lathika2006/OS-Linux-commands-Shell-script/assets/148959215/40491877-b232-4596-96a2-c3d9955510e8)



seq 2 | sed '2i hello'
## OUTPUT

![image](https://github.com/Lathika2006/OS-Linux-commands-Shell-script/assets/148959215/c0cd675e-bff0-4f16-a406-081556b997ad)


seq 10 | sed '2,9c hello'
## OUTPUT

![image](https://github.com/Lathika2006/OS-Linux-commands-Shell-script/assets/148959215/0867c436-fe08-4955-b19f-d73264f8008b)


sed -n '2,4{s/^/$/;p}' file23
## OUTPUT

![image](https://github.com/Lathika2006/OS-Linux-commands-Shell-script/assets/148959215/97a3d875-4b77-48e6-bba7-a65eedd77df3)


sed -n '2,4{s/$/*/;p}' file23


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

![image](https://github.com/Lathika2006/OS-Linux-commands-Shell-script/assets/148959215/ef7e2f21-aca3-4acd-818a-4f55a6cc180b)


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

![image](https://github.com/Lathika2006/OS-Linux-commands-Shell-script/assets/148959215/1f2963c8-35ed-4d50-9053-02ce2a88be06)


#Using tr command

cat file23 | tr [:lower:] [:upper:]
 ## OUTPUT

![image](https://github.com/Lathika2006/OS-Linux-commands-Shell-script/assets/148959215/dbf6ba03-73d0-4af8-8dc3-0d50d2d6afb4)


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

![image](https://github.com/Lathika2006/OS-Linux-commands-Shell-script/assets/148959215/0729a6c7-8b70-4a6e-93dd-369f6a699821)

 
cat urllist.txt | tr -d ' ' | tr -s '.'
## OUTPUT

![image](https://github.com/Lathika2006/OS-Linux-commands-Shell-script/assets/148959215/36ecee6f-5496-4b22-909a-5fe77534e6dc)


#Backup commands
tar -cvf backup.tar *
## OUTPUT

![image](https://github.com/Lathika2006/OS-Linux-commands-Shell-script/assets/148959215/81b64612-f73a-4d36-8b08-a1615ab5e326)


mkdir backupdir
 
mv backup.tar backupdir
 
tar -tvf backup.tar
## OUTPUT

![image](https://github.com/Lathika2006/OS-Linux-commands-Shell-script/assets/148959215/eb10b39d-0ce2-4e71-ab67-37fc7cc9d18b)


tar -xvf backup.tar
## OUTPUT

![image](https://github.com/Lathika2006/OS-Linux-commands-Shell-script/assets/148959215/1b4ddf40-3c5d-45e7-ae2b-914819b4c2ec)


gzip backup.tar

ls .gz
## OUTPUT

![image](https://github.com/Lathika2006/OS-Linux-commands-Shell-script/assets/148959215/f9334fa8-a252-415c-b056-c1f9b5d80b38)

 
gunzip backup.tar.gz
## OUTPUT

![image](https://github.com/Lathika2006/OS-Linux-commands-Shell-script/assets/148959215/5f0b0094-2c2c-40f3-884f-0c0dcecc24f1)

 
# Shell Script
```
echo '#!/bin/sh' > my-script.sh
echo 'echo Hello World‘; exit 0 >> my-script.sh
```
chmod 755 my-script.sh
./my-script.sh
## OUTPUT

![image](https://github.com/Lathika2006/OS-Linux-commands-Shell-script/assets/148959215/c7f6eac0-d1a0-4703-9a07-2d631edd84d7)
 
cat << stop > herecheck.txt
```
hello in this world
i cant stop
for this non stop movement
stop
```

cat herecheck.txt
## OUTPUT

![image](https://github.com/Lathika2006/OS-Linux-commands-Shell-script/assets/148959215/18cbf086-541c-4bb1-92ab-c814bdf8c142)

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

![image](https://github.com/Lathika2006/OS-Linux-commands-Shell-script/assets/148959215/888cca6e-adb3-4897-99a7-fd743ee6f1bd)

 
ls file1
## OUTPUT

![image](https://github.com/Lathika2006/OS-Linux-commands-Shell-script/assets/148959215/8aa7a308-1319-4bfe-b9c2-7929272e63cc)

echo $?
## OUTPUT 

![image](https://github.com/Lathika2006/OS-Linux-commands-Shell-script/assets/148959215/f0d7cbbc-d1eb-42b7-830b-91c7bc5797f4)

./one
bash: ./one: Permission denied
 
echo $?
## OUTPUT 
 
abcd
 
echo $?
 ## OUTPUT


 
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

![image](https://github.com/Lathika2006/OS-Linux-commands-Shell-script/assets/148959215/35a3a9c0-5224-4e0f-bae9-6c603032ec8e)


chmod 755 strcomp.sh
 
./strcomp.sh 
## OUTPUT

![image](https://github.com/Lathika2006/OS-Linux-commands-Shell-script/assets/148959215/a22b99b0-1191-4cd0-a055-a3206264951b)


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

![image](https://github.com/Lathika2006/OS-Linux-commands-Shell-script/assets/148959215/f984545d-33bc-4b82-833f-e994e20beb27)


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

![image](https://github.com/Lathika2006/OS-Linux-commands-Shell-script/assets/148959215/d95b622a-155f-4e82-a895-818b862dbca1)


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

![image](https://github.com/Lathika2006/OS-Linux-commands-Shell-script/assets/148959215/031d4ce7-6bf5-4cf0-9ef6-3c6fad1b8752)


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
##OUTPUT

![image](https://github.com/Lathika2006/OS-Linux-commands-Shell-script/assets/148959215/b67da7ca-c91d-4a9f-8d63-c24b01a28434)


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

![image](https://github.com/Lathika2006/OS-Linux-commands-Shell-script/assets/148959215/a955d321-158d-46a5-a932-dbe21449c991)

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

![image](https://github.com/Lathika2006/OS-Linux-commands-Shell-script/assets/148959215/24882ffa-4666-48a8-80b0-92c170da5e60)


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

## OUTPUT

![image](https://github.com/Lathika2006/OS-Linux-commands-Shell-script/assets/148959215/fd8b7441-e413-4c34-b35e-72d6b8e953bd)

 
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
 ## OUTPUT

 ![image](https://github.com/Lathika2006/OS-Linux-commands-Shell-script/assets/148959215/e4f9b365-56ff-4898-b0fd-44843212470a)

 
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
$ ./untiltest.sh

##OUTPUT

![image](https://github.com/Lathika2006/OS-Linux-commands-Shell-script/assets/148959215/22431f68-6b65-49ec-9287-eeb6d31792a4)

 
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
$ ./forin1.sh

##OUTPUT

![image](https://github.com/Lathika2006/OS-Linux-commands-Shell-script/assets/148959215/8766aba0-572e-4a9b-bd39-03c7e64820b1)

 
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
## OUTPUT

![image](https://github.com/Lathika2006/OS-Linux-commands-Shell-script/assets/148959215/169751ae-053b-424e-b0ab-63ef3308d633)

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
 
cat forin3.sh 
```bash
\#!/bin/bash
\# another example of how not to use the for command
for test in I don\'t know if "this'll" work
do
echo "word:$test"
done
```
$ chmod 755 forin3.sh
$ ./forin3.sh 
##OUTPUT

![image](https://github.com/Lathika2006/OS-Linux-commands-Shell-script/assets/148959215/20318e60-4a59-472f-ac43-2f3fb6dcd9b9)

 
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

![image](https://github.com/Lathika2006/OS-Linux-commands-Shell-script/assets/148959215/1ee1082b-0af5-42d2-8088-78ba28ca6c20)

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

![image](https://github.com/Lathika2006/OS-Linux-commands-Shell-script/assets/148959215/18486ab6-4411-45e3-8f9f-fa86c28172a5)


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

![image](https://github.com/Lathika2006/OS-Linux-commands-Shell-script/assets/148959215/841f1a13-e515-4529-b171-cd063a871600)


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

![image](https://github.com/Lathika2006/OS-Linux-commands-Shell-script/assets/148959215/1bdc895e-f05e-4992-9c84-b482adc312d0)

 
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

![image](https://github.com/Lathika2006/OS-Linux-commands-Shell-script/assets/148959215/b8396871-2ea9-4236-8a0b-f7ca315c2d98)


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

![image](https://github.com/Lathika2006/OS-Linux-commands-Shell-script/assets/148959215/2f5a8645-be73-45eb-840b-8a9d23274fb6)

 
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

![image](https://github.com/Lathika2006/OS-Linux-commands-Shell-script/assets/148959215/b459d5c6-e132-4bc5-845d-ed2316ca8f75)


 cat exread1.sh
```bash
#!/bin/bash
# testing the read command
read -p "Enter your name: " name
echo "Hello $name, welcome to my program. “
``` 
$ chmod 755 exread1.sh 


## OUTPUT

![image](https://github.com/Lathika2006/OS-Linux-commands-Shell-script/assets/148959215/f8502838-935e-4fda-9fe1-502e60e42c68)


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
$ chmod 755 funcex.sh

$ ./funcex.sh

$ ./funcex.sh 1 2

## OUTPUT
 
![image](https://github.com/Lathika2006/OS-Linux-commands-Shell-script/assets/148959215/62cd062e-c179-4e5a-9ab8-9a83f6b78032)

 
cat argshift.sh
```bash
#!/bin/bash 
 while (( "$#" )); do 
  echo $1 
  shift 
done
```
$ chmod 777 argshift.sh

$ ./argshift.sh

./argshift.sh 1 2 3

## OUTPUT

![image](https://github.com/Lathika2006/OS-Linux-commands-Shell-script/assets/148959215/e82552ac-1446-4b63-91a2-fe9947fa3ca3)

 
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
$ ./argshift.sh 1 2 3

## OUTPUT

![image](https://github.com/Lathika2006/OS-Linux-commands-Shell-script/assets/148959215/c104a58c-d3d6-4d6b-930b-d7779001e0ea)
 
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
chmod 777 argshift2.sh
 ./argshift.sh 1 2 3
 
## OUTPUT
 
 ![image](https://github.com/Lathika2006/OS-Linux-commands-Shell-script/assets/148959215/be6b3831-7903-4684-a5ad-4969e49f766a)

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

 ![image](https://github.com/Lathika2006/OS-Linux-commands-Shell-script/assets/148959215/6cc7231e-1fe4-4a75-8d76-712cf7246e4a)

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

![image](https://github.com/Lathika2006/OS-Linux-commands-Shell-script/assets/148959215/9d97b191-3f17-43eb-8883-e773907c2eea)

# RESULT:
The Commands are executed successfully.

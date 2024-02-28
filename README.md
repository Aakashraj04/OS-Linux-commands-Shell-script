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
```
chanchal singhvi
c.k. shukla
s.n. dasgupta
sumit chakrobarty
```
cat < file2
## OUTPUT
```
anil aggarwal
barun sengupta
c.k. shukla
lalit chowdury
s.n. dasgupta
# Comparing Files
cmp file1 file2
```
# Comparing Files
cmp file1 file2
## OUTPUT
 ```
 file1 file2 differ: char1,line1
 comm file1 file2
```
comm file1 file2
 ## OUTPUT
```
anil aggarwal
barun sengupta
c.k. shukla
chanchal singhvi
c.k. shukla
lalit chowdury
s.n. dasgupta
```
 
diff file1 file2
## OUTPUT
```
---file1
+++ file2
@@ -1,4 +1,5 @@
-chanchal singhvi
+anil aggarwal
+barun sengupta
 c.k. shukla
+lalit chowdury
 s.n. dasgupta
-sumit chakrobarty

```

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
![image](https://github.com/Aakashraj04/OS-Linux-commands-Shell-script/assets/121117266/d78957f3-d9bd-49e7-a683-0ca946e94547)




cut -d "|" -f 1 file22
## OUTPUT
![image](https://github.com/Aakashraj04/OS-Linux-commands-Shell-script/assets/121117266/f74ffbcd-9f0f-46ce-b868-31fe8acddc98)



cut -d "|" -f 2 file22
## OUTPUT
![image](https://github.com/Aakashraj04/OS-Linux-commands-Shell-script/assets/121117266/e5f91d42-d22e-4b14-a785-e8a5587fcfb3)


cat < newfile 
```
Hello world
hello world
^d
````
cat > newfile 
Hello world
hello world
 
grep hello newfile 
## OUTPUT
![image](https://github.com/Aakashraj04/OS-Linux-commands-Shell-script/assets/121117266/eb3e78f8-41ff-4588-863d-bfcd1123c503)

grep Hello newfile 
## OUTPUT
![image](https://github.com/Aakashraj04/OS-Linux-commands-Shell-script/assets/121117266/acd62aa0-2542-40f7-85c0-9f712b785baf)

grep -v hello newfile 
## OUTPUT
![image](https://github.com/Aakashraj04/OS-Linux-commands-Shell-script/assets/121117266/3ea4822b-4dec-454c-a77d-54d2c5bbb8ee)

cat newfile | grep -i "hello"
## OUTPUT

![image](https://github.com/Aakashraj04/OS-Linux-commands-Shell-script/assets/121117266/3a5649a9-605b-42fd-a592-20be7ea87b59)



cat newfile | grep -i -c "hello"
## OUTPUT

![image](https://github.com/Aakashraj04/OS-Linux-commands-Shell-script/assets/121117266/04dbd06e-2134-429d-9f75-c4b94525199d)



grep -R ubuntu /etc
## OUTPUT



grep -w -n world newfile   
## OUTPUT
![image](https://github.com/Aakashraj04/OS-Linux-commands-Shell-script/assets/121117266/0245faf8-ac63-4004-adb5-a3e1e546fb6b)


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
![image](https://github.com/Aakashraj04/OS-Linux-commands-Shell-script/assets/121117266/c54d29c2-fc3b-4fd9-8fe0-367257a3898d)



egrep -w '(H|h)ello' newfile 
## OUTPUT
![image](https://github.com/Aakashraj04/OS-Linux-commands-Shell-script/assets/121117266/e0b3281c-0d10-4593-97f7-1688dc28bb54)



egrep -w '(H|h)ell[a-z]' newfile 
## OUTPUT
![image](https://github.com/Aakashraj04/OS-Linux-commands-Shell-script/assets/121117266/80f67836-9823-4e93-a68d-34850d813857)




egrep '(^hello)' newfile 
## OUTPUT

![image](https://github.com/Aakashraj04/OS-Linux-commands-Shell-script/assets/121117266/04c28c42-8f25-493d-971b-d9fd10518fb9)


egrep '(world$)' newfile 
## OUTPUT
![image](https://github.com/Aakashraj04/OS-Linux-commands-Shell-script/assets/121117266/5141cd04-cd79-417e-9960-b899b92f07f1)



egrep '(World$)' newfile 
## OUTPUT
![image](https://github.com/Aakashraj04/OS-Linux-commands-Shell-script/assets/121117266/9021ac40-cddf-41ca-89a5-fe421de8fae9)


egrep '((W|w)orld$)' newfile 
## OUTPUT
![image](https://github.com/Aakashraj04/OS-Linux-commands-Shell-script/assets/121117266/5de01f53-f5b0-4776-a376-bc3a10204d88)



egrep '[1-9]' newfile 
## OUTPUT
![image](https://github.com/Aakashraj04/OS-Linux-commands-Shell-script/assets/121117266/b02593f6-059b-4dba-89e6-60cf7b93253d)



egrep 'Linux.*world' newfile 
## OUTPUT
![image](https://github.com/Aakashraj04/OS-Linux-commands-Shell-script/assets/121117266/d32d3bca-97fc-4991-97c4-aaba8b534f9f)


egrep 'Linux.*World' newfile 
## OUTPUT
![image](https://github.com/Aakashraj04/OS-Linux-commands-Shell-script/assets/121117266/99a88fc6-426c-4da4-a6fc-3de44fc85e79)

egrep l{2} newfile
## OUTPUT
![image](https://github.com/Aakashraj04/OS-Linux-commands-Shell-script/assets/121117266/097eadd9-4ef4-4b84-b456-758efdc9d4b7)



egrep 's{1,2}' newfile
## OUTPUT 
![image](https://github.com/Aakashraj04/OS-Linux-commands-Shell-script/assets/121117266/dd06128c-1446-4805-b31d-4cf14e267be7)


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
![image](https://github.com/Aakashraj04/OS-Linux-commands-Shell-script/assets/121117266/36e57ad6-122e-47c2-b940-22ad8d22123b)



sed -n -e '$p' file23
## OUTPUT

![image](https://github.com/Aakashraj04/OS-Linux-commands-Shell-script/assets/121117266/c8e46caf-8c59-42a5-bf51-09491409c09c)


sed  -e 's/Ram/Sita/' file23
## OUTPUT
![image](https://github.com/Aakashraj04/OS-Linux-commands-Shell-script/assets/121117266/d65508e0-334e-409e-9e75-6719432c64e0)



sed  -e '2s/Ram/Sita/' file23
## OUTPUT

![image](https://github.com/Aakashraj04/OS-Linux-commands-Shell-script/assets/121117266/3c90832e-332b-4638-877e-7d57f964c2e0)


sed  '/tom/s/5000/6000/' file23
## OUTPUT
![image](https://github.com/Aakashraj04/OS-Linux-commands-Shell-script/assets/121117266/5f254ef4-f713-456a-8c39-d883e402a997)



sed -n -e '1,5p' file23
## OUTPUT

![image](https://github.com/Aakashraj04/OS-Linux-commands-Shell-script/assets/121117266/42ec110a-ad05-428b-8aa1-3427f8931154)


sed -n -e '2,/Joe/p' file23
## OUTPUT

![image](https://github.com/Aakashraj04/OS-Linux-commands-Shell-script/assets/121117266/91e2d86f-be2f-4cff-bc5b-46651d9eaec1)



sed -n -e '/tom/,/Joe/p' file23
## OUTPUT
![image](https://github.com/Aakashraj04/OS-Linux-commands-Shell-script/assets/121117266/05529eb6-ea51-4023-8e3f-17f32d05dc83)


seq 10 
## OUTPUT
![image](https://github.com/Aakashraj04/OS-Linux-commands-Shell-script/assets/121117266/1912b991-788d-4941-96fc-34f9c119639d)



seq 10 | sed -n '4,6p'
## OUTPUT
![image](https://github.com/Aakashraj04/OS-Linux-commands-Shell-script/assets/121117266/150b54e8-9b28-4d15-8874-650b9594e58d)


seq 10 | sed -n '2,~4p'
## OUTPUT

![image](https://github.com/Aakashraj04/OS-Linux-commands-Shell-script/assets/121117266/183d08ae-4459-4c07-8995-ad4a95561bc2)


seq 3 | sed '2a hello'
## OUTPUT
![image](https://github.com/Aakashraj04/OS-Linux-commands-Shell-script/assets/121117266/089282ba-f462-4a12-94fa-c603e5fbb693)



seq 2 | sed '2i hello'
## OUTPUT
![image](https://github.com/Aakashraj04/OS-Linux-commands-Shell-script/assets/121117266/c44a28f6-a87e-4890-a02f-38f1db990793)


seq 10 | sed '2,9c hello'
## OUTPUT
![image](https://github.com/Aakashraj04/OS-Linux-commands-Shell-script/assets/121117266/e9f09a5e-2377-4d24-99bc-d4137d865d75)

sed -n '2,4{s/^/$/;p}' file23
## OUTPUT
![image](https://github.com/Aakashraj04/OS-Linux-commands-Shell-script/assets/121117266/e6ad7a2e-3e7c-4611-86db-e921ffa88393)



sed -n '2,4{s/$/*/;p}' file23
![image](https://github.com/Aakashraj04/OS-Linux-commands-Shell-script/assets/121117266/be07359b-8bdd-482a-8788-4324d9ad7f47)


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
![image](https://github.com/Aakashraj04/OS-Linux-commands-Shell-script/assets/121117266/7ae4b4ac-67ba-469b-9577-08c766fac86b)


#Using tr command

cat file23 | tr [:lower:] [:upper:]
 ## OUTPUT
![image](https://github.com/Aakashraj04/OS-Linux-commands-Shell-script/assets/121117266/5ed4838c-3b49-4dda-acec-0b6f999883c5)

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

![image](https://github.com/Aakashraj04/OS-Linux-commands-Shell-script/assets/121117266/549e6acc-4620-4e35-a3e1-342d1d42ec3d)

 
cat urllist.txt | tr -d ' ' | tr -s '.'
## OUTPUT



#Backup commands
tar -cvf backup.tar *
## OUTPUT


mkdir backupdir
 
mv backup.tar backupdir
 
tar -tvf backup.tar
## OUTPUT


tar -xvf backup.tar
## OUTPUT

gzip backup.tar

ls .gz
## OUTPUT
 
gunzip backup.tar.gz
## OUTPUT

 
# Shell Script
```
echo '#!/bin/sh' > my-script.sh
echo 'echo Hello World‘; exit 0 >> my-script.sh
```
chmod 755 my-script.sh
./my-script.sh
## OUTPUT

 
cat << stop > herecheck.txt
```
hello in this world
i cant stop
for this non stop movement
stop
```

cat herecheck.txt
## OUTPUT


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

 
ls file1
## OUTPUT

echo $?
## OUTPUT 
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



chmod 755 strcomp.sh
 
./strcomp.sh 
## OUTPUT


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


 cat exread1.sh
```bash
#!/bin/bash
# testing the read command
read -p "Enter your name: " name
echo "Hello $name, welcome to my program. “
``` 
$ chmod 755 exread1.sh 

## OUTPUT



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


# RESULT:
The Commands are executed successfully.

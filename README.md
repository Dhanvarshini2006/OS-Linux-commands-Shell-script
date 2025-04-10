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
![image](https://github.com/user-attachments/assets/634ac1f1-6ac3-4e97-89a2-2f8316043852)



cat < file2
## OUTPUT
![image](https://github.com/user-attachments/assets/09da1afb-c491-4517-ab04-c440a4308999)



# Comparing Files
cmp file1 file2
## OUTPUT
![image](https://github.com/user-attachments/assets/e7eae80d-e1b7-4120-90ea-ce87e77bab83)


 
comm file1 file2
 ## OUTPUT
![image](https://github.com/user-attachments/assets/5bd9c348-a715-44ef-ab97-250f0075d3fa)

diff file1 file2
## OUTPUT
![image](https://github.com/user-attachments/assets/78a3d482-e43e-4b28-9977-219691b4c9a0)


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
![image](https://github.com/user-attachments/assets/d2743532-c51e-4f8b-9035-9bd13036ee6e)



cut -d "|" -f 1 file22
## OUTPUT
![image](https://github.com/user-attachments/assets/0fb3d096-b3b9-4d0d-9d2a-c72cceed2a53)



cut -d "|" -f 2 file22
## OUTPUT
![image](https://github.com/user-attachments/assets/837cc36b-dcd5-4657-8475-607f01334ef9)


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
![image](https://github.com/user-attachments/assets/d5882c4c-4885-472b-9bf7-818945a4067f)




grep hello newfile 
## OUTPUT
![image](https://github.com/user-attachments/assets/d251c3af-589d-4333-b799-30feb2825b7d)




grep -v hello newfile 
## OUTPUT
![image](https://github.com/user-attachments/assets/606b8c2b-f067-42e2-91f2-f502c642ef77)


cat newfile | grep -i "hello"
## OUTPUT
![image](https://github.com/user-attachments/assets/3c11c53d-0515-4307-9a44-f7460966a607)




cat newfile | grep -i -c "hello"
## OUTPUT
![image](https://github.com/user-attachments/assets/24e8eab7-4ee2-4163-8aff-61d9590535ae)



grep -R ubuntu /etc
## OUTPUT
![image](https://github.com/user-attachments/assets/66cc7a34-d99a-437e-acfb-aa19c9e7ea00)



grep -w -n world newfile   
## OUTPUT
![image](https://github.com/user-attachments/assets/c0dc0e06-91c3-4672-8a81-431a63859636)


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
![image](https://github.com/user-attachments/assets/b79e7af2-f62c-4a73-a43b-3d95b064ef77)



egrep -w '(H|h)ello' newfile 
## OUTPUT
![image](https://github.com/user-attachments/assets/ef98c7ca-e834-4825-b7b7-2b3fc675e236)


egrep -w '(H|h)ell[a-z]' newfile 
## OUTPUT
![image](https://github.com/user-attachments/assets/93dc995a-90e9-4890-b510-c02463551d5e)




egrep '(^hello)' newfile 
## OUTPUT
![image](https://github.com/user-attachments/assets/7a232b62-d540-41be-91be-64a5fb03367f)



egrep '(world$)' newfile 
## OUTPUT
![image](https://github.com/user-attachments/assets/e98b3db3-0453-4c81-8ad9-3685155567d3)




egrep '(World$)' newfile 
## OUTPUT
![image](https://github.com/user-attachments/assets/e6b2e608-ad39-40e1-852d-6e9a9730f7da)


egrep '((W|w)orld$)' newfile 
## OUTPUT
![image](https://github.com/user-attachments/assets/52d8b20a-f90f-4773-8397-04fed1241a24)



egrep '[1-9]' newfile 
## OUTPUT
![image](https://github.com/user-attachments/assets/ca59d576-b6fe-4cad-b993-4e97327a294a)


egrep 'Linux.*world' newfile 
## OUTPUT
![image](https://github.com/user-attachments/assets/9e5261e4-b0a2-43a6-a331-8c8bef7e82d7)



egrep 'Linux.*World' newfile 
## OUTPUT
![image](https://github.com/user-attachments/assets/3b6b3408-eece-4ee8-8531-647bfbe94b6f)

egrep l{2} newfile
## OUTPUT
![image](https://github.com/user-attachments/assets/b7b5fce7-9118-4719-90e7-62bd6159728d)



egrep 's{1,2}' newfile
## OUTPUT 
![image](https://github.com/user-attachments/assets/69d97a55-718f-49f5-878a-27fb13f50b3a)


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
![image](https://github.com/user-attachments/assets/c996a628-c124-4632-a2eb-401127c6c63c)



sed -n -e '5p' file23
## OUTPUT
![image](https://github.com/user-attachments/assets/662279ee-0235-4096-b991-17515caf4ef1)




sed  -e 's/Ram/Sita/' file23
## OUTPUT
![image](https://github.com/user-attachments/assets/e9abf882-4497-4602-a70f-6160e5f62239)



sed  -e '2s/Ram/Sita/' file23
## OUTPUT
![image](https://github.com/user-attachments/assets/eec8f808-a947-4f04-a6a8-118a4c84da5c)



sed  '/tom/s/5000/6000/' file23
## OUTPUT
![image](https://github.com/user-attachments/assets/94a89200-32ed-4ded-942e-003b2069ec47)



sed -n -e '1,5p' file23
## OUTPUT
![image](https://github.com/user-attachments/assets/3d6fed4b-b35e-4532-a4bb-5fa83967e8f7)


sed -n -e '2,/Joe/p' file23
## OUTPUT

![image](https://github.com/user-attachments/assets/40bcbcff-174b-4473-ab1a-d0e145a9a3a2)



sed -n -e '/tom/,/Joe/p' file23
## OUTPUT
![image](https://github.com/user-attachments/assets/f1456cad-4bbc-4f3d-9b81-3261ac8fa86d)


seq 10 
## OUTPUT
![image](https://github.com/user-attachments/assets/f6e96870-5d21-49c0-ac01-5eb1780f68fe)



seq 10 | sed -n '4,6p'
## OUTPUT
![image](https://github.com/user-attachments/assets/8553f94b-aeb3-4233-ab84-8c2922b362cd)



seq 10 | sed -n '2,~4p'
## OUTPUT
![image](https://github.com/user-attachments/assets/c5e9c07c-ffa3-4dd1-8ee9-26b19d7c2944)



seq 3 | sed '2a hello'
## OUTPUT
![image](https://github.com/user-attachments/assets/a98f8fbc-e513-4dce-92fa-a86cdb69d57c)



seq 2 | sed '2i hello'
## OUTPUT
![image](https://github.com/user-attachments/assets/75da1a7b-636c-4212-95cc-0daf33439a52)


seq 10 | sed '2,9c hello'
## OUTPUT
![image](https://github.com/user-attachments/assets/8bf23907-8322-4c09-840f-a96954544117)


sed -n '2,4{s/^/$/;p}' file23
## OUTPUT
![image](https://github.com/user-attachments/assets/9cfb3809-34f0-4e4d-8508-8a26852b9e6c)



sed -n '2,4{s/$/*/;p}' file23
## OUTPUT
![image](https://github.com/user-attachments/assets/f50c6cda-368c-4655-a0e2-52e5f3dedea9)


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
![image](https://github.com/user-attachments/assets/f5828a95-dca9-49f6-89fe-0bf335b13fef)


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
![image](https://github.com/user-attachments/assets/7683f17b-6fc3-42b6-85af-9da1bba9eb52)



#Using tr command

cat file23 | tr [:lower:] [:upper:]
 ## OUTPUT
 ![image](https://github.com/user-attachments/assets/a3c52e41-b1dd-4c3b-8090-a67417f0c119)


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
![image](https://github.com/user-attachments/assets/677a6bad-0ee9-4408-b427-adb1e50c4255)


 
cat urllist.txt | tr -d ' ' | tr -s '.'
## OUTPUT
![image](https://github.com/user-attachments/assets/f6b7929b-46ae-420a-a2d4-6c761d7c9da0)


#Backup commands
tar -cvf backup.tar *
## OUTPUT
![image](https://github.com/user-attachments/assets/dedb6214-31ab-4f34-9f5e-e819c99b6490)


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
![image](https://github.com/user-attachments/assets/cc1481c8-c140-406b-9eaa-c3d0f83c0ba1)


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

## OUTPUT
![image](https://github.com/user-attachments/assets/a5617238-2e02-4d3f-82b6-d31dd2f419be)



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
![image](https://github.com/user-attachments/assets/123859e7-4fe4-4a46-8c6a-9c4888c63e1a)


 
ls file1
## OUTPUT

![image](https://github.com/user-attachments/assets/3e9987d7-de29-4d2b-a9cc-54d7b8e4b804)


echo $?
## OUTPUT 

![image](https://github.com/user-attachments/assets/a7afe317-2dde-4d5b-b16a-4c5762879a01)

./one
bash: ./one: Permission denied
 
echo $?

## OUTPUT 
 ![image](https://github.com/user-attachments/assets/bae8910c-ba58-45d1-9656-8e74b351aac2)

abcd
 
echo $?
 ## OUTPUT

![image](https://github.com/user-attachments/assets/238d5443-c3dd-4a73-9313-7b6e6039196e)

 
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

## OUTPUT
![image](https://github.com/user-attachments/assets/e8015eed-e7fe-45d7-a00a-bad25d56d722)



chmod 755 strcomp.sh
 
./strcomp.sh 
## OUTPUT
![image](https://github.com/user-attachments/assets/338cf1ee-f318-40d2-86e0-74beabf55ef3)


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

![image](https://github.com/user-attachments/assets/4e35bc15-e5fe-4029-aeaa-f370d076d717)


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
![image](https://github.com/user-attachments/assets/0f1cab8b-65f6-4be8-9d18-4a01ad44dd03)




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
![image](https://github.com/user-attachments/assets/fe8cf2f6-9b3b-4788-bde3-749636be1051)

 



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
![Screenshot from 2025-04-10 20-52-03](https://github.com/user-attachments/assets/4ce33835-8af1-4dd8-bf7f-17804e7ac7b7)

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
![image](https://github.com/user-attachments/assets/6c863a35-a7dc-4ae9-aed9-8d291116ce35)


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

![Screenshot from 2025-04-10 21-21-50](https://github.com/user-attachments/assets/34e47fc6-38ae-43ee-9ba3-6a565567d852)

 
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

![Screenshot from 2025-04-10 21-30-15](https://github.com/user-attachments/assets/17b26096-57af-4ad8-847f-4079eb3d3d15)

 
 
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
![Screenshot from 2025-04-10 21-28-55](https://github.com/user-attachments/assets/c58f6ccd-1775-4d0e-b4be-a0b3633a3d23)

 
 
 
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
![Screenshot from 2025-04-10 21-30-15](https://github.com/user-attachments/assets/65550d7f-e15f-4bc1-b5d3-e61ccd335832)
 
 
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
![image](https://github.com/user-attachments/assets/696b3e5d-8efa-475f-8583-170548696457)


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
 ![image](https://github.com/user-attachments/assets/0cf8eb87-b148-4286-bc72-dbf80bc2ac01)



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
![image](https://github.com/user-attachments/assets/81ab1494-f0f9-4bd6-80b4-67f9d2b26868)


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

![image](https://github.com/user-attachments/assets/3c3a45ba-0f02-4178-8ec6-9803b48c20ef)

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
## OUTPUT
![image](https://github.com/user-attachments/assets/196661b3-69e6-463e-87d8-de289c535efd)

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
## OUTPUT
![image](https://github.com/user-attachments/assets/b6c400d4-be9a-48cd-af9a-0353007cbe0e)

awk -f nc.awk data.dat
## OUTPUT 
![image](https://github.com/user-attachments/assets/e6056a1b-886c-4138-acab-44ca082732a2)

 
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
![image](https://github.com/user-attachments/assets/be35ce0e-1cb0-46e0-bcd8-13ce0634317e)



# RESULT:
The Commands are executed successfully.

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
cat < file2
## OUTPUT
![image](https://github.com/user-attachments/assets/c3893933-d2a3-4aab-8b2b-2517c295ffb3)

# Comparing Files
cmp file1 file2
## OUTPUT
 ![image](https://github.com/user-attachments/assets/9fbb375c-419d-4068-a34f-0024c0e7956c)

comm file1 file2
 ## OUTPUT
![image](https://github.com/user-attachments/assets/fe9d242f-d054-4b5a-9a13-e89455f888bf)

 
diff file1 file2
## OUTPUT
![image](https://github.com/user-attachments/assets/238b4bf7-0115-4d1b-8498-8d16cfe0599c)


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

![image](https://github.com/user-attachments/assets/80785423-5146-496a-9a92-699ca6236a65)



cut -d "|" -f 1 file22
## OUTPUT

![image](https://github.com/user-attachments/assets/c21af105-8a3d-4458-9f16-f546ea318a68)


cut -d "|" -f 2 file22
## OUTPUT
![image](https://github.com/user-attachments/assets/78f81a13-5a45-43d5-954c-51b806e7dd40)


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
![image](https://github.com/user-attachments/assets/a2c6df57-2b30-4c9d-a950-fa272d3e3f8d)



grep hello newfile 
## OUTPUT

![image](https://github.com/user-attachments/assets/f10af965-a490-411d-81d3-37e9881c9acd)



grep -v hello newfile 
## OUTPUT
![image](https://github.com/user-attachments/assets/31d5ca07-c954-4030-bde4-b1f6161ddb1d)



cat newfile | grep -i "hello"
## OUTPUT

![image](https://github.com/user-attachments/assets/11dba4fe-e79f-4a96-afde-49ea6a2fc5e8)



cat newfile | grep -i -c "hello"
## OUTPUT

![image](https://github.com/user-attachments/assets/1bd95a16-732c-4014-a438-78eaa84b744e)



grep -R ubuntu /etc
## OUTPUT
![image](https://github.com/user-attachments/assets/bd54ed38-5b8b-4cf3-a103-b785970a1314)



grep -w -n world newfile   
## OUTPUT
![image](https://github.com/user-attachments/assets/318abe50-f2f9-407a-af3d-4710e1f67ab6)


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
![image](https://github.com/user-attachments/assets/7b3f2189-4034-43fc-9c03-4957559f29f8)



egrep -w '(H|h)ello' newfile 
## OUTPUT
![image](https://github.com/user-attachments/assets/2ff41474-f7d0-42fd-af32-48b48e65d087)



egrep -w '(H|h)ell[a-z]' newfile 
## OUTPUT

![image](https://github.com/user-attachments/assets/cefda79e-bc48-4610-b225-4a2dc001f5bd)



egrep '(^hello)' newfile 
## OUTPUT
![image](https://github.com/user-attachments/assets/0606cd79-3a31-427b-867d-7cf1409c549a)



egrep '(world$)' newfile 
## OUTPUT
![image](https://github.com/user-attachments/assets/b1f6ca6e-3e58-4e14-bc19-59b1a3509b10)



egrep '(World$)' newfile 
## OUTPUT

![image](https://github.com/user-attachments/assets/b1f6ca6e-3e58-4e14-bc19-59b1a3509b10)

egrep '((W|w)orld$)' newfile 
## OUTPUT

![image](https://github.com/user-attachments/assets/fafcb4a6-848c-4bf6-a586-352fdc5cfa3f)


egrep '[1-9]' newfile 
## OUTPUT
![image](https://github.com/user-attachments/assets/6a01d6aa-2373-4a1f-b4e9-a75fce5d41de)



egrep 'Linux.*world' newfile 
## OUTPUT
![image](https://github.com/user-attachments/assets/5383dd37-381c-414a-a55e-bcb284a79e2b)


egrep 'Linux.*World' newfile 
## OUTPUT
![image](https://github.com/user-attachments/assets/5c5879f2-d5f7-4ab2-9cc3-f9f9a731d87c)


egrep l{2} newfile
## OUTPUT

![image](https://github.com/user-attachments/assets/142c6933-37a3-4d9a-ae26-b74435fc06c2)


egrep 's{1,2}' newfile
## OUTPUT 

![image](https://github.com/user-attachments/assets/0cfdf08c-66d3-4f44-a9e3-daae0f0a1418)

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
![image](https://github.com/user-attachments/assets/74a5eb4f-3221-4a10-98f6-4ddc8001d7b8)



sed -n -e '$p' file23
## OUTPUT
![image](https://github.com/user-attachments/assets/9d506d4b-a876-42a0-9aff-79834c050dfb)



sed  -e 's/Ram/Sita/' file23
## OUTPUT

![image](https://github.com/user-attachments/assets/87ef47de-12a7-40dd-82a9-66d0018e9181)


sed  -e '2s/Ram/Sita/' file23
## OUTPUT

![image](https://github.com/user-attachments/assets/9446f60c-7224-48e0-a3a9-0d4715c205b1)


sed  '/tom/s/5000/6000/' file23
## OUTPUT

![image](https://github.com/user-attachments/assets/c599a0cf-5789-4b02-b624-3736d0c57ece)


sed -n -e '1,5p' file23
## OUTPUT
![image](https://github.com/user-attachments/assets/f348986a-fe11-40d8-b891-0e237f5b03b2)



sed -n -e '2,/Joe/p' file23
## OUTPUT
![image](https://github.com/user-attachments/assets/ccad8677-353e-47a9-a944-cce9122c51c4)




sed -n -e '/tom/,/Joe/p' file23
## OUTPUT

![image](https://github.com/user-attachments/assets/2381a79e-9a3b-4593-9b04-32870d2365f4)


seq 10 
## OUTPUT
![image](https://github.com/user-attachments/assets/be4aad14-1ecd-4500-8a79-f527e69b720e)



seq 10 | sed -n '4,6p'
## OUTPUT
![image](https://github.com/user-attachments/assets/57db29c8-3d0a-49e2-8f69-34c6788e5a7e)



seq 10 | sed -n '2,~4p'
## OUTPUT
![image](https://github.com/user-attachments/assets/c37c3a2c-a6c4-4ab0-9739-d1613a33a53e)



seq 3 | sed '2a hello'
## OUTPUT

![image](https://github.com/user-attachments/assets/defa997a-a88c-4778-9749-cfbf8b6e8cd2)


seq 2 | sed '2i hello'
## OUTPUT
![image](https://github.com/user-attachments/assets/93e91158-be16-4426-b5ee-1ae995afe700)


seq 10 | sed '2,9c hello'
## OUTPUT
![image](https://github.com/user-attachments/assets/42a58831-9246-4acf-ac67-bfb542eeb51b)


sed -n '2,4{s/^/$/;p}' file23
## OUTPUT

![image](https://github.com/user-attachments/assets/afeaab9e-c688-40f4-a688-00e684ab7f33)


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
![image](https://github.com/user-attachments/assets/baeed806-266c-4155-96f0-04e87854b221)



#Using tr command

cat file23 | tr [:lower:] [:upper:]
 ## OUTPUT
![image](https://github.com/user-attachments/assets/688ced8e-6077-4d2c-aa58-87546ff58102)

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
![image](https://github.com/user-attachments/assets/48e6ccd7-09ee-4a90-8d0e-243516f8c8c8)


 
cat urllist.txt | tr -d ' ' | tr -s '.'
## OUTPUT
![image](https://github.com/user-attachments/assets/2152b522-8f76-4282-b0c8-5506b77b019e)



#Backup commands
tar -cvf backup.tar *
## OUTPUT
bench.py file1 file11 file2 file21 file22 file23 hello.c hello.js                                      newfile readme.txt urllist.txt

mkdir backupdir
 
mv backup.tar backupdir
 
tar -tvf backup.tar
## OUTPUT
-rw-r--r-- user/group 0 2024-02-25 14:30:00 file1.txt drwxr-xr-x user/group 0 2024-02-25 14:30:00 directory1/ -rw-r--r-- user/group 1024 2024-02-25 14:30:00 directory1/file2.txt -rw-r--r-- user/group 2048 2024-02-25 14:30:00 directory1/file3.txt tar -xvf backup.tar      
tar -xvf backup.tar
## OUTPUT
x file1.txt x directory1/ x directory1/file2.txt x directory1/file3.txt
gzip backup.tar

ls .gz
## OUTPUT
backup.tar.gz gunzip backup.tar.gz
## OUTPUT
backup.tar
 
# Shell Script
```
echo '#!/bin/sh' > my-script.sh
echo 'echo Hello World‘; exit 0 >> my-script.sh
```
chmod 755 my-script.sh
./my-script.sh
## OUTPUT
![image](https://github.com/user-attachments/assets/cb31a8d4-63ec-4cef-959b-b934859a4780)

 
cat << stop > herecheck.txt
```
hello in this world
i cant stop
for this non stop movement
stop
```

cat herecheck.txt
## OUTPUT
![image](https://github.com/user-attachments/assets/f0c4a6bd-5b3f-4713-bd9b-e9d8ea32b5f5)


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
File name is ./scriptest.sh File name is scriptest.sh First arg. is 1 Second arg. is 2 Third arg. is 3 Fourth arg. is The @ i s 1 2 3 T h e
 
ls file1
## OUTPUT
![image](https://github.com/user-attachments/assets/6ee50aef-4e6b-4908-a249-b8188d4d3d9b)

echo $?
## OUTPUT 
![image](https://github.com/user-attachments/assets/90670edc-48cb-498f-a66d-fd754ea975fe)

./one
bash: ./one: Permission denied
 
echo $?
## OUTPUT 
 
abcd
 
echo $?
 ## OUTPUT
1
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
![image](https://github.com/user-attachments/assets/d82f4924-bf2b-4175-8e83-c36cec603396)

chmod 755 strcomp.sh
 
./strcomp.sh 
## OUTPUT
baseball is less than hockey

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
You are the owner of the /etc/passwd file
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
![image](https://github.com/user-attachments/assets/95e4c995-1698-455e-9457-dc47b5a6aef2)



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
![image](https://github.com/user-attachments/assets/6da5feca-ec5b-416a-b547-f735f2a3aa5f)

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
![image](https://github.com/user-attachments/assets/638ee850-7fbb-4735-8fcf-654d898fa478)


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
![image](https://github.com/user-attachments/assets/ba3cc137-1894-4f81-877e-fc9b3fa7fca2)

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
![image](https://github.com/user-attachments/assets/b008d022-f4fd-4051-814c-391a983cb663)

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
## OUTPUt
![image](https://github.com/user-attachments/assets/15dc1e1f-aa35-469d-b7f2-6284400b1124)

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
![image](https://github.com/user-attachments/assets/854fc7fd-3952-49c4-977b-ccbb4ffa6409)

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
 ![image](https://github.com/user-attachments/assets/50a9e2af-ff53-4347-8d1d-822568f3542b)

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
![image](https://github.com/user-attachments/assets/37da2fef-2e1a-4403-aba1-d2dca7e70c55)

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
![image](https://github.com/user-attachments/assets/7ed05ce8-486b-47d7-a3f3-44f97e27c284)

cat exread.sh 
```
#!/bin/bash
# testing the read command
echo -n "Enter your name: "
read name
echo "Hello $name, welcome to my program. "
 ```
 
$ chmod 755 exread.sh 
 
$ ./exread.sh 
## OUTPUT:
![image](https://github.com/user-attachments/assets/245fb0a5-6c00-4b38-94bd-84ce35268b34)

cat funcex.sh

```
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
![image](https://github.com/user-attachments/assets/b233261a-47c7-400e-b283-77d208d24331)

./funcex.sh 1 2

## OUTPUT
 ![image](https://github.com/user-attachments/assets/65ed5ac9-8a58-41f5-971a-e789c7b0ea96)

cat argshift.sh
```
#!/bin/bash 
 while (( "$#" )); do 
  echo $1 
  shift 
done
```
$ chmod 777 argshift.sh

## OUTPUT
![image](https://github.com/user-attachments/assets/23e3730d-9c19-4239-b68f-af7fad60bdc7)

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
![image](https://github.com/user-attachments/assets/e1e4b0ab-f0a1-4414-b856-1886e2fd7b64)

$ ./argshift.sh 1 2 3
 
cat argshift.sh
```
#!/bin/bash 
set -x 
while (( "$#" )); do 
  echo $1 
  shift 
done
set +x
```
./argshift.sh 1 2 3

## OUTPUT
![image](https://github.com/user-attachments/assets/35dc02e8-b51c-4cc8-b0ee-b2cb26326fab)

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
 ![image](https://github.com/user-attachments/assets/7fa999a1-40f3-434c-b5dc-93282812cb40)

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
![image](https://github.com/user-attachments/assets/f5fa90ad-dfb1-453d-9724-38b6f5eec17c)

# RESULT:
The Commands are executed successfully.

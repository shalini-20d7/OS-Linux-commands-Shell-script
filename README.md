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
<img width="270" height="167" alt="image" src="https://github.com/user-attachments/assets/03525429-99df-4ac1-b960-5a6a2e753296" />



cat < file2
## OUTPUT

<img width="257" height="172" alt="image" src="https://github.com/user-attachments/assets/e25713e4-156c-4d2d-bb64-1d828887b086" />

# Comparing Files
cmp file1 file2
## OUTPUT
 <img width="373" height="82" alt="image" src="https://github.com/user-attachments/assets/fb05ae2b-ba62-4a5b-8bb9-98d073d4d3b8" />

comm file1 file2
 ## OUTPUT

 <img width="327" height="282" alt="image" src="https://github.com/user-attachments/assets/b4204ab9-daee-47bb-8406-7058f50debe3" />

diff file1 file2
## OUTPUT
<img width="317" height="317" alt="image" src="https://github.com/user-attachments/assets/7b3ea7f9-4fa1-48bd-a414-40da330526bf" />


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

<img width="323" height="143" alt="image" src="https://github.com/user-attachments/assets/36b2a645-1f4d-4049-ab56-9ea14177f862" />



cut -d "|" -f 1 file22
## OUTPUT

<img width="392" height="155" alt="image" src="https://github.com/user-attachments/assets/8e74bc2b-6cbc-450d-ab0e-a5a8cc0b8b81" />


cut -d "|" -f 2 file22
## OUTPUT
<img width="400" height="140" alt="image" src="https://github.com/user-attachments/assets/d0c809bf-f165-426b-bbc2-c51c71100757" />


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

<img width="345" height="92" alt="image" src="https://github.com/user-attachments/assets/1535de76-fc0a-499e-a107-827b7491d96f" />


grep hello newfile 
## OUTPUT
<img width="352" height="68" alt="image" src="https://github.com/user-attachments/assets/4f46fdf4-a5cb-4d4b-a7a3-45f55c969d9e" />




grep -v hello newfile 
## OUTPUT

<img width="377" height="97" alt="image" src="https://github.com/user-attachments/assets/36b564ff-cde8-45f9-9f0c-bb0a599fb4db" />


cat newfile | grep -i "hello"
## OUTPUT

<img width="456" height="96" alt="image" src="https://github.com/user-attachments/assets/81942284-990b-49f2-8d40-21c62260f381" />



cat newfile | grep -i -c "hello"
## OUTPUT

<img width="498" height="77" alt="image" src="https://github.com/user-attachments/assets/84a51c22-e65f-4e3f-b619-758c2c9dbff6" />





grep -w -n world newfile   
## OUTPUT

<img width="402" height="105" alt="image" src="https://github.com/user-attachments/assets/178de305-bd5f-41a7-8136-b44765fb70b1" />

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
<img width="461" height="98" alt="image" src="https://github.com/user-attachments/assets/0f70be72-d2c4-4d47-b7d5-8a3bf12d4b2e" />



egrep -w '(H|h)ello' newfile 
## OUTPUT

<img width="450" height="90" alt="image" src="https://github.com/user-attachments/assets/e14ef92a-4e3c-45e7-b098-b92eb58bb1f7" />


egrep -w '(H|h)ell[a-z]' newfile 
## OUTPUT
<img width="498" height="95" alt="image" src="https://github.com/user-attachments/assets/4dc660ee-b659-4f64-8cea-de17e54ec33f" />




egrep '(^hello)' newfile 
## OUTPUT

<img width="425" height="76" alt="image" src="https://github.com/user-attachments/assets/3b13b859-ca53-4bab-a7c2-c52ca7402bb6" />



egrep '(world$)' newfile 
## OUTPUT
<img width="397" height="90" alt="image" src="https://github.com/user-attachments/assets/3c829b76-0b1f-417d-89bd-c6ed38ea8e26" />


egrep '(World$)' newfile
## OUTPUT

<img width="408" height="68" alt="image" src="https://github.com/user-attachments/assets/438f3632-caec-4afa-99ba-ae0f5b23e177" />


egrep '((W|w)orld$)' newfile 
## OUTPUT

<img width="442" height="117" alt="image" src="https://github.com/user-attachments/assets/acf6bb83-1592-46ad-93ef-ad0c3fd7caf9" />


egrep '[1-9]' newfile 
## OUTPUT
<img width="368" height="67" alt="image" src="https://github.com/user-attachments/assets/7a15d636-ea50-4c6f-969e-72be0b8ed134" />



egrep 'Linux.*world' newfile 
## OUTPUT
<img width="450" height="77" alt="image" src="https://github.com/user-attachments/assets/9084b33a-8213-4356-bbaa-6dd9a8673692" />


egrep 'Linux.*World' newfile 
## OUTPUT
<img width="437" height="75" alt="image" src="https://github.com/user-attachments/assets/cc8db248-d6e5-4093-82a5-f2dfaf470559" />


egrep l{2} newfile
## OUTPUT
<img width="353" height="92" alt="image" src="https://github.com/user-attachments/assets/5a066fb7-d88b-4f0f-a6de-a6a6737f6dca" />



egrep 's{1,2}' newfile
## OUTPUT 
<img width="396" height="120" alt="image" src="https://github.com/user-attachments/assets/0fda0bb9-aec9-438c-8a91-dfba214adaf1" />


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

<img width="367" height="72" alt="image" src="https://github.com/user-attachments/assets/d709ebb9-fe61-48f6-a164-8199a5ef4fd3" />


sed -n -e '$p' file23
## OUTPUT
<img width="382" height="82" alt="image" src="https://github.com/user-attachments/assets/38e9f2b5-30d5-4189-a9e5-b8f4c697d2e5" />



sed  -e 's/Ram/Sita/' file23
## OUTPUT

<img width="465" height="251" alt="image" src="https://github.com/user-attachments/assets/0f9c8be4-b818-444d-83d5-f47e65c571b9" />


sed  -e '2s/Ram/Sita/' file23
## OUTPUT

<img width="461" height="243" alt="image" src="https://github.com/user-attachments/assets/5bbef138-423f-44de-8260-3675425d4b5a" />


sed  '/tom/s/5000/6000/' file23
## OUTPUT
<img width="477" height="250" alt="image" src="https://github.com/user-attachments/assets/86a4d232-1f1e-49b9-90f0-ed1730cb94c3" />



sed -n -e '1,5p' file23
## OUTPUT

<img width="410" height="163" alt="image" src="https://github.com/user-attachments/assets/cedb46fc-6547-4b34-b6b3-3735cb49ea98" />


sed -n -e '2,/Joe/p' file23
## OUTPUT
<img width="428" height="120" alt="image" src="https://github.com/user-attachments/assets/ee73ac4a-7ece-4135-bf29-0274f88ef30b" />




sed -n -e '/tom/,/Joe/p' file23
## OUTPUT

<img width="486" height="95" alt="image" src="https://github.com/user-attachments/assets/ca97c575-6c5c-4e02-98fb-6b61d7e7c29b" />


seq 10 
## OUTPUT
<img width="297" height="265" alt="image" src="https://github.com/user-attachments/assets/921179c0-f377-4e03-9ee3-da04a1dea3bd" />



seq 10 | sed -n '4,6p'
## OUTPUT

<img width="376" height="113" alt="image" src="https://github.com/user-attachments/assets/fd167fe0-f1d6-42d2-8ac4-edd003828474" />


seq 10 | sed -n '2,~4p'
## OUTPUT

<img width="402" height="115" alt="image" src="https://github.com/user-attachments/assets/c7692964-1841-4675-b265-ee72da061841" />


seq 3 | sed '2a hello'
## OUTPUT

<img width="400" height="148" alt="image" src="https://github.com/user-attachments/assets/83565e95-c41e-4aac-8be5-49bef8ea32e9" />


seq 2 | sed '2i hello'
## OUTPUT
<img width="410" height="117" alt="image" src="https://github.com/user-attachments/assets/33590c72-0993-4086-8cf1-6b9f2f892533" />


seq 10 | sed '2,9c hello'
## OUTPUT
<img width="407" height="125" alt="image" src="https://github.com/user-attachments/assets/b9086426-0521-44e1-8e1e-c5b50a5aafcd" />


sed -n '2,4{s/^/$/;p}' file23
## OUTPUT

<img width="462" height="117" alt="image" src="https://github.com/user-attachments/assets/e029c83a-34e8-4420-9abd-fc3f87a67284" />


sed -n '2,4{s/$/*/;p}' file23

<img width="462" height="112" alt="image" src="https://github.com/user-attachments/assets/0eb170b1-8936-4271-a68b-ab60213b89f8" />


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


<img width="327" height="177" alt="image" src="https://github.com/user-attachments/assets/808237f9-5072-499f-9986-d1fec3b431b7" />

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


<img width="423" height="150" alt="image" src="https://github.com/user-attachments/assets/07b7af15-0cb3-4553-953d-f188b25d9e3d" />


#Using tr command

cat file23 | tr [:lower:] [:upper:]
 ## OUTPUT

<img width="532" height="242" alt="image" src="https://github.com/user-attachments/assets/d1e77e55-53b3-43d5-8ec7-1c224c254a8e" />

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


<img width="555" height="147" alt="image" src="https://github.com/user-attachments/assets/9dcb08d4-d9a0-478b-a1e2-e5409e1497e7" />

 
cat urllist.txt | tr -d ' ' | tr -s '.'
## OUTPUT

<img width="555" height="147" alt="image" src="https://github.com/user-attachments/assets/4922f0ea-27ef-4dd1-a33c-095871c0b4e2" />



#Backup commands
tar -cvf backup.tar *
## OUTPUT

<img width="371" height="251" alt="image" src="https://github.com/user-attachments/assets/a7b59a24-c245-46dc-b061-abf5547618cc" />


mkdir backupdir
 
mv backup.tar backupdir

cd backupdir
 
tar -tvf backup.tar
## OUTPUT

<img width="645" height="305" alt="image" src="https://github.com/user-attachments/assets/477d8436-294a-48ba-80f4-1a42e10f6a8e" />


tar -xvf backup.tar
## OUTPUT

<img width="438" height="245" alt="image" src="https://github.com/user-attachments/assets/8ebbb6fc-a783-4d70-96b9-6009ab6ab576" />


 
cat << stop > herecheck.txt
```
hello in this world
i cant stop
for this non stop movement
stop
```

cat herecheck.txt
## OUTPUT


<img width="337" height="136" alt="image" src="https://github.com/user-attachments/assets/049c1b2f-e3ff-49cc-919e-6acbcbf45d2f" />

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

<img width="503" height="865" alt="image" src="https://github.com/user-attachments/assets/cb491234-9bf5-4676-8d45-83e74be8f56f" />

 
ls file1
## OUTPUT

<img width="247" height="85" alt="image" src="https://github.com/user-attachments/assets/c92c20e7-4dc1-4da5-be55-22102f0b596b" />

echo $?
## OUTPUT 
./one
bash: ./one: Permission denied

 <img width="220" height="67" alt="image" src="https://github.com/user-attachments/assets/bc0d5a9e-5ed1-400c-8d0b-bd099c2b7322" />

echo $?
## OUTPUT 

 <img width="252" height="73" alt="image" src="https://github.com/user-attachments/assets/1f3eccad-df2b-478f-99a3-ab10ed84aacd" />

abcd
 
echo $?
 ## OUTPUT


<img width="302" height="87" alt="image" src="https://github.com/user-attachments/assets/35cade2f-3ec6-462e-95e3-3f95af9147ec" />

 
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


<img width="411" height="200" alt="image" src="https://github.com/user-attachments/assets/7fee8300-9e9d-400e-b329-6615dcdf669c" />


chmod 755 strcomp.sh
 
./strcomp.sh 
## OUTPUT

<img width="362" height="111" alt="image" src="https://github.com/user-attachments/assets/ed322010-f501-46d5-a4d5-4c98de82d60b" />


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

<img width="388" height="80" alt="image" src="https://github.com/user-attachments/assets/ea248da3-faf8-493a-a7e4-2c2c1c6e6d6f" />

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


<img width="428" height="90" alt="image" src="https://github.com/user-attachments/assets/37f5cc18-f9f5-495e-8cce-670510c716a1" />


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

<img width="393" height="127" alt="image" src="https://github.com/user-attachments/assets/20b582e9-e93b-4338-9d21-3e2d159fd9d0" />

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

<img width="422" height="133" alt="image" src="https://github.com/user-attachments/assets/ad11760d-a78c-4d14-a256-ff833e038350" />

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

<img width="430" height="182" alt="image" src="https://github.com/user-attachments/assets/794d726d-6546-4137-bf0a-d6616a52a2d2" />


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

<img width="438" height="110" alt="image" src="https://github.com/user-attachments/assets/1a82c3ff-f7aa-4053-b671-3377f165358e" />

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

<img width="631" height="256" alt="image" src="https://github.com/user-attachments/assets/7c7bfa0d-eacb-4e9c-ac1f-2dc0af02cd8b" />

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

<img width="377" height="305" alt="image" src="https://github.com/user-attachments/assets/93b52029-86a1-421e-a8dc-3284d955dd94" />
 
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
## OUTPUT

<img width="435" height="160" alt="image" src="https://github.com/user-attachments/assets/bec7e33f-9eca-42ee-827e-2c30dff1380b" />
 
 
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
## OUTPUT

 <img width="390" height="210" alt="image" src="https://github.com/user-attachments/assets/01a92484-00e2-4b28-86fe-1a52778ab503" />

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
 ## OUTPUT
<img width="377" height="151" alt="image" src="https://github.com/user-attachments/assets/e9883a7c-851b-464b-8a6c-591db010ab27" />




 


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

<img width="377" height="151" alt="image" src="https://github.com/user-attachments/assets/f204d221-b08f-413f-b251-13738e7c8efd" />
 

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
## OUTPUT

<img width="405" height="218" alt="image" src="https://github.com/user-attachments/assets/18fc9345-9881-4265-95d7-7b77639def18" />


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

<img width="385" height="210" alt="image" src="https://github.com/user-attachments/assets/5618769c-c6fd-4f84-bc22-447cea38df63" />


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


<img width="298" height="71" alt="image" src="https://github.com/user-attachments/assets/2386380f-4366-4113-b927-e638fad4cda2" />


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




<img width="393" height="200" alt="image" src="https://github.com/user-attachments/assets/4e88139a-a2ab-4ead-8bf8-742b6e04980a" />



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


<img width="392" height="191" alt="image" src="https://github.com/user-attachments/assets/e7c40194-1c91-4f58-97d5-4cfa78c590f0" />





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
<img width="437" height="335" alt="image" src="https://github.com/user-attachments/assets/1fa4ae2a-b82f-4f2d-ad67-2d4b1655391d" />

 
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
<img width="393" height="142" alt="image" src="https://github.com/user-attachments/assets/9e44259e-4fa2-4f7c-b73c-f5283d801cdb" />

 
$ chmod 755 forcontinue.sh
 
$ ./forcontinue.sh 
## OUTPUT
 <img width="412" height="182" alt="image" src="https://github.com/user-attachments/assets/2d93e86c-dc4e-45dd-814e-d935b43bb1b5" />

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
<img width="485" height="77" alt="image" src="https://github.com/user-attachments/assets/4c5efa1e-7a56-4661-8faa-f920db0f2013" />



 cat exread1.sh
```bash
#!/bin/bash
# testing the read command
read -p "Enter your name: " name
echo "Hello $name, welcome to my program. “
``` 
$ chmod 755 exread1.sh 

## OUTPUT
<img width="488" height="107" alt="image" src="https://github.com/user-attachments/assets/0c107816-15ba-4aad-b3ba-99666d39950a" />



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
<img width="376" height="97" alt="image" src="https://github.com/user-attachments/assets/9f93f7da-8407-4a02-8ac0-fd910aff3a75" />

 
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
 <img width="396" height="143" alt="image" src="https://github.com/user-attachments/assets/63ba2971-1d35-4e59-8551-3dcf8af3cba3" />

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
<img width="405" height="142" alt="image" src="https://github.com/user-attachments/assets/cc88baa6-f88c-4d1a-be34-e8ec4e70cdeb" />


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
 <img width="407" height="350" alt="image" src="https://github.com/user-attachments/assets/c51a16c1-e6ba-46c2-a078-90ad371f60dd" />

 
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
 <img width="376" height="65" alt="image" src="https://github.com/user-attachments/assets/f781f77a-e08f-461b-a4b2-c1b323d6ffd0" />

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
<img width="407" height="138" alt="image" src="https://github.com/user-attachments/assets/20a84508-4dab-4a8c-88b5-fcfd9a186147" />


# RESULT:
The Commands are executed successfully.

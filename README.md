<img width="1876" height="131" alt="image" src="https://github.com/user-attachments/assets/676e37a1-059c-49b2-a0dc-fb4ea0ec5ab9" /># OS-Linux-commands-Shell-scripting
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
<img width="1920" height="974" alt="output1" src="https://github.com/user-attachments/assets/8c4bb112-1d5b-4e9e-a99f-a60eb3d5d93e" />



cat < file2
## OUTPUT

<img width="1920" height="974" alt="output1" src="https://github.com/user-attachments/assets/7b94afb3-e477-4869-ab6f-b6d830b39f96" />

# Comparing Files
cmp file1 file2
## OUTPUT

 <img width="1798" height="227" alt="output2" src="https://github.com/user-attachments/assets/42f50606-ed6a-48a3-8c0b-9e281db8c12f" />

comm file1 file2
 ## OUTPUT
<img width="1810" height="299" alt="output3" src="https://github.com/user-attachments/assets/f3a5fe26-408a-4bb9-b8f6-cb87e969fca3" />

 
diff file1 file2
## OUTPUT

<img width="1810" height="299" alt="output4" src="https://github.com/user-attachments/assets/9e76c914-6bb8-4b9c-99b5-2a9bb3d306f1" />

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
<img width="1808" height="246" alt="output5" src="https://github.com/user-attachments/assets/25b22f3a-2da5-4c3e-bd52-68d52a71bd72" />




cut -d "|" -f 1 file22
## OUTPUT

<img width="1808" height="246" alt="output6" src="https://github.com/user-attachments/assets/10061146-b11c-468e-a6fc-697d32bf12f1" />


cut -d "|" -f 2 file22
## OUTPUT

<img width="1808" height="246" alt="output7" src="https://github.com/user-attachments/assets/fb82b7bc-4ab6-4191-a465-2ed70b0bcb1b" />

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
<img width="1808" height="246" alt="output8" src="https://github.com/user-attachments/assets/b708986d-2719-4a2b-b550-afcbb7443a18" />



grep hello newfile 
## OUTPUT

<img width="1687" height="261" alt="output9" src="https://github.com/user-attachments/assets/b90c7512-5a4a-4893-b410-328fa0f7a2bf" />



grep -v hello newfile 
## OUTPUT

<img width="1687" height="261" alt="output10" src="https://github.com/user-attachments/assets/249394ba-0859-4fd7-8bf9-44dcdbecae86" />


cat newfile | grep -i "hello"
## OUTPUT

<img width="1544" height="111" alt="output11" src="https://github.com/user-attachments/assets/f34282a5-c834-43d7-8fc7-7c2104ecc76b" />



cat newfile | grep -i -c "hello"
## OUTPUT

<img width="1544" height="60" alt="output12" src="https://github.com/user-attachments/assets/965b157e-d0fa-45dd-b957-7667de4256f0" />



grep -R ubuntu /etc
## OUTPUT

<img width="1920" height="974" alt="output13" src="https://github.com/user-attachments/assets/cf48460f-fc1c-4bf6-aa6e-119f6bf9b839" />


grep -w -n world newfile   
## OUTPUT

<img width="1544" height="174" alt="output14" src="https://github.com/user-attachments/assets/c8a32215-2b26-401b-a1f2-e8ffe7abe3d4" />

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
<img width="1571" height="276" alt="15" src="https://github.com/user-attachments/assets/cc170d35-c0f0-4a96-9372-d2c0ee6d75c0" />



egrep -w '(H|h)ello' newfile 
## OUTPUT
<img width="1474" height="126" alt="16" src="https://github.com/user-attachments/assets/f4ea4db8-e203-40d7-8ac3-c64b7e79a63c" />




egrep -w '(H|h)ell[a-z]' newfile 
## OUTPUT

<img width="1474" height="126" alt="17" src="https://github.com/user-attachments/assets/81b08e99-abac-4d80-9c47-debb01726e06" />



egrep '(^hello)' newfile 
## OUTPUT

<img width="1365" height="105" alt="18" src="https://github.com/user-attachments/assets/c75e137e-712c-4212-abcc-1ac492675efc" />


egrep '(world$)' newfile 
## OUTPUT

<img width="1365" height="105" alt="19" src="https://github.com/user-attachments/assets/4e438aa5-6a03-46ed-a3da-59145036b65f" />


egrep '(World$)' newfile 
## OUTPUT

<img width="1365" height="105" alt="20" src="https://github.com/user-attachments/assets/60d0a37d-9f26-431d-ae43-2cefee6f10cf" />

egrep '((W|w)orld$)' newfile 
## OUTPUT

<img width="1378" height="131" alt="21" src="https://github.com/user-attachments/assets/2a75138c-f7f7-4bb5-9719-32b42f299932" />


egrep '[1-9]' newfile 
## OUTPUT

<img width="1378" height="131" alt="image" src="https://github.com/user-attachments/assets/59fa86be-02c3-4e57-90c9-d536fece9fea" />


egrep 'Linux.*world' newfile 
## OUTPUT

<img width="1378" height="131" alt="image" src="https://github.com/user-attachments/assets/be2ae8a4-2f69-4180-a886-1ff06223ac35" />

egrep 'Linux.*World' newfile 
## OUTPUT
<img width="1920" height="215" alt="image" src="https://github.com/user-attachments/assets/2913a315-fc02-48bf-b4f1-2050189c64b7" />


egrep l{2} newfile
## OUTPUT

<img width="1689" height="210" alt="image" src="https://github.com/user-attachments/assets/b3b2c1fb-4274-4785-a66d-81cb55cfdefb" />


egrep 's{1,2}' newfile
## OUTPUT 

<img width="1689" height="210" alt="image" src="https://github.com/user-attachments/assets/6b894d2d-9061-4ceb-953a-4d29d58c4631" />

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

<img width="1680" height="302" alt="image" src="https://github.com/user-attachments/assets/e252baeb-c9bd-4f8a-9c66-cee5d40045fd" />


sed -n -e '$p' file23
## OUTPUT

<img width="1424" height="97" alt="image" src="https://github.com/user-attachments/assets/a77801d7-5936-4d6a-89a3-22066e38dfe4" />


sed  -e 's/Ram/Sita/' file23
## OUTPUT
<img width="1424" height="251" alt="image" src="https://github.com/user-attachments/assets/eb31c4f2-6189-4cbc-bb88-478a1bb786f2" />



sed  -e '2s/Ram/Sita/' file23
## OUTPUT

<img width="1424" height="251" alt="image" src="https://github.com/user-attachments/assets/cd615fc3-31a5-43cd-bac9-08f17119054b" />


sed  '/tom/s/5000/6000/' file23
## OUTPUT

<img width="1424" height="251" alt="image" src="https://github.com/user-attachments/assets/62ca8e69-b756-482e-b6d0-b8fd946911d8" />


sed -n -e '1,5p' file23
## OUTPUT

<img width="1424" height="251" alt="image" src="https://github.com/user-attachments/assets/e9442200-874d-47b7-8b55-3500632b4d35" />


sed -n -e '2,/Joe/p' file23
## OUTPUT

<img width="1288" height="145" alt="image" src="https://github.com/user-attachments/assets/e363126c-7526-42d2-9d19-16522d151eb5" />



sed -n -e '/tom/,/Joe/p' file23
## OUTPUT

<img width="1288" height="145" alt="image" src="https://github.com/user-attachments/assets/9313882c-61b2-4805-86e8-c9167d4e9d0a" />


seq 10 
## OUTPUT
<img width="1258" height="286" alt="image" src="https://github.com/user-attachments/assets/fd27f9c9-0708-433d-9c52-abc5036460ea" />



seq 10 | sed -n '4,6p'
## OUTPUT

<img width="1042" height="142" alt="image" src="https://github.com/user-attachments/assets/54451ca1-010c-45fb-a1fb-1767a0fa0c35" />


seq 10 | sed -n '2,~4p'
## OUTPUT

<img width="1042" height="142" alt="image" src="https://github.com/user-attachments/assets/e5ce5927-a8e5-4088-8529-a45298439482" />


seq 3 | sed '2a hello'
## OUTPUT

<img width="1042" height="218" alt="image" src="https://github.com/user-attachments/assets/9d1a2080-8044-4fe0-b9bf-ec3de5aa3464" />


seq 2 | sed '2i hello'
## OUTPUT

<img width="954" height="173" alt="image" src="https://github.com/user-attachments/assets/9779ab48-b9a5-4ff8-a113-f2313cbbb6a2" />

seq 10 | sed '2,9c hello'
## OUTPUT

<img width="954" height="173" alt="image" src="https://github.com/user-attachments/assets/5624e2e7-548e-44fe-a671-531524eaae93" />

sed -n '2,4{s/^/$/;p}' file23
## OUTPUT

<img width="954" height="173" alt="image" src="https://github.com/user-attachments/assets/1dc6658e-8eec-46bd-a445-62918ed226b4" />


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

<img width="602" height="157" alt="image" src="https://github.com/user-attachments/assets/2d0e4625-1d62-4599-a17f-d6cc20ac7a68" />


#Using tr command

cat file23 | tr [:lower:] [:upper:]
 ## OUTPUT
<img width="848" height="281" alt="image" src="https://github.com/user-attachments/assets/d7130ce2-5af0-4f65-ab8b-d837cb0f7016" />

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

<img width="1876" height="282" alt="image" src="https://github.com/user-attachments/assets/0d3fb15a-ca08-44c7-8a46-2cde86162579" />

 
cat urllist.txt | tr -d ' ' | tr -s '.'
## OUTPUT

<img width="1876" height="141" alt="image" src="https://github.com/user-attachments/assets/048fc5af-07b7-40e3-9c5c-882f0a686fcd" />


#Backup commands
tar -cvf backup.tar *
## OUTPUT

<img width="1876" height="688" alt="image" src="https://github.com/user-attachments/assets/2481ee19-1009-4850-9ebe-609bc555e469" />

mkdir backupdir
 
mv backup.tar backupdir

cd backupdir
 
tar -tvf backup.tar
## OUTPUT
<img width="1876" height="688" alt="image" src="https://github.com/user-attachments/assets/5a0f8ea1-55b4-4f91-b67b-2318c295571c" />


tar -xvf backup.tar
## OUTPUT
<img width="1876" height="774" alt="image" src="https://github.com/user-attachments/assets/374c174c-894b-4f30-93a8-a35a699a903e" />

gzip backup.tar

ls .gz
## OUTPUT
 <img width="1920" height="974" alt="image" src="https://github.com/user-attachments/assets/e742612c-851a-4f39-8cb4-150cf1b65e12" />

gunzip backup.tar.gz
## OUTPUT

 <img width="1920" height="974" alt="image" src="https://github.com/user-attachments/assets/53323c42-d230-415c-aff3-e925f8968d88" />

# Shell Script
```
echo '#!/bin/sh' > my-script.sh
echo 'echo Hello World‘; exit 0 >> my-script.sh
```
chmod 755 my-script.sh
./my-script.sh
## OUTPUT
<img width="1876" height="215" alt="image" src="https://github.com/user-attachments/assets/12040070-1d35-490c-91b0-cf3746992c63" />

 
cat << stop > herecheck.txt
```
hello in this world
i cant stop
for this non stop movement
stop
```

cat herecheck.txt
## OUTPUT
<img width="1876" height="249" alt="image" src="https://github.com/user-attachments/assets/fe292440-42f3-4386-b791-f8a443adcb73" />


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
<img width="1876" height="464" alt="image" src="https://github.com/user-attachments/assets/1d98ddff-c208-437c-b6a6-4c2d5365d13f" />

 
ls file1
## OUTPUT
<img width="1876" height="92" alt="image" src="https://github.com/user-attachments/assets/597ea858-f3ab-4dbf-91b0-de9ce7a58cfd" />

echo $?
## OUTPUT 
<img width="1876" height="66" alt="image" src="https://github.com/user-attachments/assets/73a993a7-b6c7-4e78-a9f5-1a3ac475d5ed" />

./one
bash: ./one: Permission denied
 
echo $?
## OUTPUT 
 <img width="1876" height="131" alt="image" src="https://github.com/user-attachments/assets/330db04a-2993-428f-949d-95d67fffb8bc" />

abcd
 
echo $?
 ## OUTPUT

<img width="1864" height="245" alt="image" src="https://github.com/user-attachments/assets/204d289b-2b23-4c3b-b844-866194cd65c0" />


 
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

<img width="1864" height="245" alt="image" src="https://github.com/user-attachments/assets/e289a3ca-2c72-4898-b068-79de8a6de242" />


chmod 755 strcomp.sh
 
./strcomp.sh 
## OUTPUT
<img width="1864" height="101" alt="image" src="https://github.com/user-attachments/assets/dd7bb412-1163-4ac9-994e-e60002e89a5d" />


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
<img width="1864" height="101" alt="image" src="https://github.com/user-attachments/assets/508c574d-0ee9-41f8-a391-841417fe7d77" />

# check if with file location
cat>ifnested.sh 
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

<img width="1878" height="116" alt="image" src="https://github.com/user-attachments/assets/dc5665e9-f7b0-4b6e-b92c-a90642eb6269" />


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
<img width="1878" height="116" alt="image" src="https://github.com/user-attachments/assets/f4fdd5a6-4a52-440e-af61-a09316fdfa21" />

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
<img width="1878" height="156" alt="image" src="https://github.com/user-attachments/assets/780d2430-b59d-4d8e-a356-5ba9ff230b2a" />

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
<img width="1878" height="156" alt="image" src="https://github.com/user-attachments/assets/c05ecaa7-8d41-4afc-bda4-e144beb7cdb9" />


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
<img width="1878" height="76" alt="image" src="https://github.com/user-attachments/assets/f39c2a33-36bd-45ea-8391-2e7f955cf918" />

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
<img width="1920" height="974" alt="image" src="https://github.com/user-attachments/assets/3489f9b3-5105-411c-b18d-edb0efd53315" />

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
<img width="1878" height="213" alt="image" src="https://github.com/user-attachments/assets/e7d13463-efac-4219-a4a7-b8d81d0b40cf" />


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
<img width="1878" height="235" alt="image" src="https://github.com/user-attachments/assets/494e5f1f-f07c-41f2-9e44-ce5db0ba9ae9" />

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

<img width="1878" height="235" alt="image" src="https://github.com/user-attachments/assets/2aaece3f-7726-41a9-a2ac-df832107a682" />
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

 <img width="1876" height="362" alt="image" src="https://github.com/user-attachments/assets/06b230ac-7a0d-4532-8eb0-a31b2df9143f" />

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
 <img width="1876" height="119" alt="image" src="https://github.com/user-attachments/assets/a782c18d-241c-4737-b760-96d9f2a228a7" />
<img width="1876" height="160" alt="image" src="https://github.com/user-attachments/assets/ec61339c-dd29-40f8-af30-cc76ae06cbf6" />

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

<img width="1876" height="116" alt="image" src="https://github.com/user-attachments/assets/dcf8121a-11f5-4af5-9b14-20906c073178" />


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
<img width="1876" height="72" alt="image" src="https://github.com/user-attachments/assets/bab75403-c31d-46d8-a1d2-f9c9926ac310" />

 
 ./funcex.sh 1 2

 <img width="1876" height="72" alt="image" src="https://github.com/user-attachments/assets/e93d24f3-fe83-4f49-a0e6-f932be68526c" />

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
 <img width="1876" height="155" alt="image" src="https://github.com/user-attachments/assets/9f8a5919-e47d-4a21-a34a-7cc89ee29b81" />

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
<img width="1876" height="241" alt="image" src="https://github.com/user-attachments/assets/a0a23517-ec14-4de4-a2d0-59545915b6d6" />


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
 <img width="1876" height="365" alt="image" src="https://github.com/user-attachments/assets/3f56e316-4a49-41eb-b715-2b9a72817a15" />

 
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
 <img width="1876" height="365" alt="image" src="https://github.com/user-attachments/assets/bc31f399-809b-47ec-9ae7-ab56e5570a93" />

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

<img width="1876" height="286" alt="image" src="https://github.com/user-attachments/assets/a7502f8a-a616-402d-b5da-626d04e36c10" />

# RESULT:
The Commands are executed successfully.

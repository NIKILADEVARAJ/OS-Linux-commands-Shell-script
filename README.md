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

![WhatsApp Image 2025-09-28 at 10 55 05_28884e70](https://github.com/user-attachments/assets/d94a0040-751e-4d94-9c62-560196cbafad)



cat < file2
## OUTPUT
![WhatsApp Image 2025-09-28 at 10 52 23_ea385d49](https://github.com/user-attachments/assets/34adce73-4900-44f9-a077-25e91f3d9b76)

# Comparing Files
cmp file1 file2
## OUTPUT
 ![WhatsApp Image 2025-09-28 at 10 56 22_11d1556b](https://github.com/user-attachments/assets/3fc04ad2-f8db-47f0-8c38-9dc25e8ba2d0)
comm file1 file2
 ## OUTPUT
![WhatsApp Image 2025-09-28 at 10 57 56_248a36fb](https://github.com/user-attachments/assets/9cecea81-c952-48d5-ae1d-848aceb571ae)
 
diff file1 file2
## OUTPUT

![WhatsApp Image 2025-09-28 at 10 59 15_9ec5bb29](https://github.com/user-attachments/assets/15a261d6-4502-4388-b31d-cd90765f8d6e)



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
![WhatsApp Image 2025-09-28 at 11 00 33_714138b9](https://github.com/user-attachments/assets/b88cf8a3-48ca-41a5-aa5f-40ac9ee629f2)




cut -d "|" -f 1 file22
## OUTPUT
![WhatsApp Image 2025-09-28 at 11 01 18_26fa5ec4](https://github.com/user-attachments/assets/e4d0bbb6-3e84-43af-992d-517b25b9deaf)



cut -d "|" -f 2 file22
## OUTPUT
![WhatsApp Image 2025-09-28 at 11 02 06_427f7904](https://github.com/user-attachments/assets/4675f7e0-292e-4a6d-a463-2d638d1a476f)


cat < newfile 
```
Hello world
hello world
^d
````
cat > newfile 
Hello world
hello world
 ## OUTPUT 
 ![WhatsApp Image 2025-09-28 at 11 03 29_a1fc5459](https://github.com/user-attachments/assets/4d5d0e3c-8d97-47d7-8bf0-705d5a6d09c6)

grep Hello newfile 
## OUTPUT

![WhatsApp Image 2025-09-28 at 11 05 10_1b16b51e](https://github.com/user-attachments/assets/62d7c96a-da27-4470-a68e-0ace148909ad)


grep hello newfile 
## OUTPUT

![WhatsApp Image 2025-09-28 at 11 05 23_649c0e80](https://github.com/user-attachments/assets/8817911c-6cdd-4c18-ac7f-29e8998fccd3)



grep -v hello newfile 
## OUTPUT

![WhatsApp Image 2025-09-28 at 11 06 23_6a071847](https://github.com/user-attachments/assets/0412eef1-0f97-448c-99b1-62cd4734fce7)


cat newfile | grep -i "hello"
## OUTPUT
![WhatsApp Image 2025-09-28 at 11 07 39_e287eb64](https://github.com/user-attachments/assets/9567e8ee-ab73-4662-990f-6150e14b4920)




cat newfile | grep -i -c "hello"
## OUTPUT
![WhatsApp Image 2025-09-28 at 11 07 28_50658503](https://github.com/user-attachments/assets/fab08513-911d-4310-be2e-9662fd09bf27)




grep -R parrot /etc
## OUTPUT
<img width="1920" height="937" alt="image" src="https://github.com/user-attachments/assets/e9b107b7-3b0e-40e6-a967-3a1829db6c7e" />



grep -w -n world newfile   
## OUTPUT
![WhatsApp Image 2025-09-28 at 12 42 18_893ffaa3](https://github.com/user-attachments/assets/0a26b6d0-788f-4473-af03-a0d01535f4f0)


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
![WhatsApp Image 2025-09-28 at 12 44 28_8cab69e4](https://github.com/user-attachments/assets/e54370d0-525a-427d-9ee2-592c64bc2b10)



egrep -w '(H|h)ello' newfile 
## OUTPUT
![WhatsApp Image 2025-09-28 at 12 45 01_a9b6ce99](https://github.com/user-attachments/assets/d975618a-0ffd-4548-84a2-63700bf3cc71)



egrep -w '(H|h)ell[a-z]' newfile 
## OUTPUT


![WhatsApp Image 2025-09-28 at 12 45 26_43bd2544](https://github.com/user-attachments/assets/1cb7ee6c-3195-488b-a3df-635fd58abcf6)


egrep '(^hello)' newfile 
## OUTPUT
![WhatsApp Image 2025-09-28 at 12 45 57_2ad78dbd](https://github.com/user-attachments/assets/0a379399-470a-49f2-b57d-493fef898636)



egrep '(world$)' newfile 
## OUTPUT
![WhatsApp Image 2025-09-28 at 12 46 25_1117dda5](https://github.com/user-attachments/assets/43ff4926-c212-4e77-800e-00edd9d3578e)



egrep '(World$)' newfile 
## OUTPUT
![WhatsApp Image 2025-09-28 at 12 46 54_33ac2936](https://github.com/user-attachments/assets/f72e9a7b-3955-4ece-a521-024a40236f13)


egrep '((W|w)orld$)' newfile 
## OUTPUT

![WhatsApp Image 2025-09-28 at 12 47 32_0e8c06ba](https://github.com/user-attachments/assets/480e9756-3d81-425f-9acc-bc33b7b7cb6b)


egrep '[1-9]' newfile 
## OUTPUT


![WhatsApp Image 2025-09-28 at 12 48 01_e73b6c06](https://github.com/user-attachments/assets/14982eea-163a-4aa6-93c5-716ff2e62621)

egrep 'Linux.*world' newfile 
## OUTPUT
![WhatsApp Image 2025-09-28 at 12 48 29_d8d0c27b](https://github.com/user-attachments/assets/7fb4c98e-61e9-444e-87d1-c3c84bbd57f5)


egrep 'Linux.*World' newfile 
## OUTPUT

![WhatsApp Image 2025-09-28 at 12 48 51_cd13d069](https://github.com/user-attachments/assets/076e0135-2727-4ba4-867f-84e4d10ee3b5)

egrep l{2} newfile
## OUTPUT

![WhatsApp Image 2025-09-28 at 12 49 38_df4ad6d8](https://github.com/user-attachments/assets/8a9daa42-6fea-45ce-a440-48073796b0e0)


egrep 's{1,2}' newfile
## OUTPUT 
![WhatsApp Image 2025-09-28 at 12 50 25_3406bf72](https://github.com/user-attachments/assets/88d5c3aa-442d-4fe5-a5ee-ae6ad7c1645a)


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
![WhatsApp Image 2025-09-28 at 12 52 01_d69b32db](https://github.com/user-attachments/assets/19ce316e-49e5-4594-8bb6-942c86c75b3c)



sed -n -e '$p' file23
## OUTPUT

![WhatsApp Image 2025-09-28 at 12 52 50_8ca398b5](https://github.com/user-attachments/assets/79de7c3b-0736-4665-9d4a-38dcc438a609)


sed  -e 's/Ram/Sita/' file23
## OUTPUT

![WhatsApp Image 2025-09-28 at 12 53 47_90e525d9](https://github.com/user-attachments/assets/bcba9c8a-1d81-42e4-8124-941a30226fd3)


sed  -e '2s/Ram/Sita/' file23
## OUTPUT
![WhatsApp Image 2025-09-28 at 12 54 41_e42e68a4](https://github.com/user-attachments/assets/e63e6abb-a50d-4bd7-a669-c366455b8c6b)



sed  '/tom/s/5000/6000/' file23
## OUTPUT

![WhatsApp Image 2025-09-28 at 12 55 24_11ecd4a4](https://github.com/user-attachments/assets/24ba4a19-dec8-44bf-9e6e-1cc8af601352)


sed -n -e '1,5p' file23
## OUTPUT
![WhatsApp Image 2025-09-28 at 12 57 07_a5a5ab73](https://github.com/user-attachments/assets/8eec82c2-f421-48bf-8d3a-dfdbfe91bd53)



sed -n -e '2,/Joe/p' file23
## OUTPUT

![WhatsApp Image 2025-09-28 at 12 58 18_c05e9eb5](https://github.com/user-attachments/assets/ebb1428b-7076-489a-a123-26ff8fcbe766)



sed -n -e '/tom/,/Joe/p' file23
## OUTPUT
![WhatsApp Image 2025-09-28 at 12 58 58_316331d4](https://github.com/user-attachments/assets/25ccde55-a75b-4397-99ee-59e94b1117e7)



seq 10 
## OUTPUT

![WhatsApp Image 2025-09-28 at 12 59 52_fa136b2c](https://github.com/user-attachments/assets/5e447f1e-aedd-4ee5-82fd-ad8a9112130a)


seq 10 | sed -n '4,6p'
## OUTPUT
![WhatsApp Image 2025-09-28 at 13 01 00_02a05d4a](https://github.com/user-attachments/assets/064d4d60-ac83-4bb6-8227-021eef06b141)



seq 10 | sed -n '2,~4p'
## OUTPUT

![WhatsApp Image 2025-09-28 at 13 01 35_e8cb905a](https://github.com/user-attachments/assets/5189f972-5db8-46de-8df1-9150c6b57571)


seq 3 | sed '2a hello'
## OUTPUT

![WhatsApp Image 2025-09-28 at 13 05 34_55ef1967](https://github.com/user-attachments/assets/0f66640c-ddb5-4366-b3e3-2f2bcd20e147)


seq 2 | sed '2i hello'
## OUTPUT
![WhatsApp Image 2025-09-28 at 13 06 02_beecef1b](https://github.com/user-attachments/assets/a287c3d3-44e7-48f6-bb83-0c46703c1e4d)



seq 10 | sed '2,9c hello'
## OUTPUT
![WhatsApp Image 2025-09-28 at 13 08 14_b52c1493](https://github.com/user-attachments/assets/957f8fc3-beb3-4690-b150-18d5d4da05ad)


sed -n '2,4{s/^/$/;p}' file23
## OUTPUT
![WhatsApp Image 2025-09-28 at 13 08 35_322a7035](https://github.com/user-attachments/assets/218fa587-e13a-4268-b916-385f13fd6141)



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
![WhatsApp Image 2025-09-28 at 13 10 57_3c232e4f](https://github.com/user-attachments/assets/f913e903-8a2e-496b-b424-f4840e93de2a)


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

![WhatsApp Image 2025-09-28 at 13 13 04_748558fe](https://github.com/user-attachments/assets/6abf11d6-535e-4265-9a2f-4502b7cf0f44)


#Using tr command

cat file23 | tr [:lower:] [:upper:]
 ## OUTPUT
cat![WhatsApp Image 2025-09-28 at 13 15 06_2d18bddc](https://github.com/user-attachments/assets/7b726329-1ec3-4c63-903f-bdc7e17e069d)

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
![WhatsApp Image 2025-09-28 at 13 17 50_b6e74eda](https://github.com/user-attachments/assets/56664014-e327-411e-9ab3-2eb95c3aff0c)


 
cat urllist.txt | tr -d ' ' | tr -s '.'
## OUTPUT

![WhatsApp Image 2025-09-28 at 13 18 04_222180e1](https://github.com/user-attachments/assets/969e9a33-2247-46ce-8ae5-a061bb9ea421)


#Backup commands
tar -cvf backup.tar *
## OUTPUT
![WhatsApp Image 2025-09-28 at 13 21 42_fe299f63](https://github.com/user-attachments/assets/e263ca83-a238-4127-abaa-5f4722471415)



mkdir backupdir
 
mv backup.tar backupdir

cd backupdir
 
tar -tvf backup.tar
## OUTPUT
<img width="1280" height="461" alt="image" src="https://github.com/user-attachments/assets/cec2ee51-1a05-43d5-a6c0-3d8c64904c20" />

tar -xvf backup.tar
## OUTPUT
![WhatsApp Image 2025-09-28 at 13 23 43_ef60f9f0](https://github.com/user-attachments/assets/0e085c72-d3c4-4844-9303-d49a05da1e00)

gzip backup.tar

ls .gz
## OUTPUT
 ![WhatsApp Image 2025-09-28 at 13 24 47_26f6137e](https://github.com/user-attachments/assets/608b31d2-824f-41c4-ac45-81f74ef162b7)

gunzip backup.tar.gz
## OUTPUT
![WhatsApp Image 2025-09-28 at 13 26 59_fb4b47e7](https://github.com/user-attachments/assets/93336490-1a35-4bee-b6b7-65e00a9eabe6)

 
# Shell Script
```
echo '#!/bin/sh' > my-script.sh
echo 'echo Hello World‘; exit 0 >> my-script.sh
```
chmod 755 my-script.sh
./my-script.sh
## OUTPUT
![WhatsApp Image 2025-09-28 at 13 27 35_d7dd032b](https://github.com/user-attachments/assets/7873be6b-53b1-45e2-9978-0498d708e13b)

 
cat << stop > herecheck.txt
```
hello in this world
i cant stop
for this non stop movement
stop
```

cat herecheck.txt
## OUTPUT

![WhatsApp Image 2025-09-28 at 13 30 02_5e9a28fa](https://github.com/user-attachments/assets/cee9a611-0230-482b-8c9f-afa61e11dd16)

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

 ![WhatsApp Image 2025-09-28 at 13 48 17_78326827](https://github.com/user-attachments/assets/1f6031a0-b514-40a6-9967-492c1301a039)

ls file1
## OUTPUT
![WhatsApp Image 2025-09-28 at 13 48 38_0387690b](https://github.com/user-attachments/assets/ce9bf8fb-a863-450f-87dd-e43964df38b8)

echo $?
## OUTPUT 
./one
bash: ./one: Permission denied
 <img width="258" height="49" alt="image" src="https://github.com/user-attachments/assets/a6dbc9ce-0567-427d-b845-919fa8b77825" />

echo $?
## OUTPUT 
 ![WhatsApp Image 2025-09-28 at 13 49 03_3215c1e8](https://github.com/user-attachments/assets/fa607474-5092-4d06-af13-18a29bb590db)

abcd
 
echo $?
 ## OUTPUT
![WhatsApp Image 2025-09-28 at 13 49 27_5ca2bd11](https://github.com/user-attachments/assets/1cd93d8f-94ef-4052-ad0d-5f87a61aeaa2)


 
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
![WhatsApp Image 2025-09-28 at 13 52 57_991a7ccb](https://github.com/user-attachments/assets/7f6bd65e-f215-424d-b610-5077048421a0)



chmod 755 strcomp.sh
 
./strcomp.sh 
## OUTPUT
![WhatsApp Image 2025-09-28 at 13 51 28_613067e2](https://github.com/user-attachments/assets/aade5658-094d-4ff7-a0af-1b31c7d4cfc9)


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
##OUTPUT 
![WhatsApp Image 2025-09-28 at 13 54 48_0e9be609](https://github.com/user-attachments/assets/a5a197e9-414d-4019-8623-b2e41ba4f863)
./psswdperm.sh
## OUTPUT

![WhatsApp Image 2025-09-28 at 13 55 00_cc4827bc](https://github.com/user-attachments/assets/b6e51b5f-a850-4d30-be7b-b5624d909400)


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
![WhatsApp Image 2025-09-28 at 13 57 51_239da918](https://github.com/user-attachments/assets/1d7d6d48-fc65-4995-8d7e-57ec3bd9d0c2)



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
![WhatsApp Image 2025-09-28 at 13 59 32_d68e4b49](https://github.com/user-attachments/assets/68023b7c-bb2f-4ea5-9b82-bc896c8bea56)

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
![WhatsApp Image 2025-09-28 at 14 03 30_9e32c766](https://github.com/user-attachments/assets/697b6239-8b43-4feb-8658-8ab76a624976)

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
![WhatsApp Image 2025-09-28 at 14 01 49_1539b12f](https://github.com/user-attachments/assets/4c309615-3d15-41c0-8d83-59d5e8f53ad4)


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
![WhatsApp Image 2025-09-28 at 14 05 10_e0d4506f](https://github.com/user-attachments/assets/226d63f5-c644-479b-a933-62ceb956ad6f)

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
![WhatsApp Image 2025-09-28 at 14 06 07_0bc42c00](https://github.com/user-attachments/assets/0020cb81-b473-4921-9484-c59a68ef8a7b)
 
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
 ![WhatsApp Image 2025-09-28 at 14 07 14_be0675e1](https://github.com/user-attachments/assets/8f0c1315-babd-4de8-9c68-a6f1e58b6abe)

 
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
 
![WhatsApp Image 2025-09-28 at 14 08 00_feeef4b1](https://github.com/user-attachments/assets/baee3b1a-5cd3-43a1-b7f5-88fae1e8da43)
 
 
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
 
![WhatsApp Image 2025-09-28 at 14 09 13_995ad4c1](https://github.com/user-attachments/assets/f4a0a14f-bc9d-4a80-9fbd-52384f1bf8e4)
 
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
![WhatsApp Image 2025-09-28 at 14 09 34_f401ae7a](https://github.com/user-attachments/assets/51456761-5fd6-408e-bb73-09303fe23f96)

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
![WhatsApp Image 2025-09-28 at 14 11 29_fa6914a0](https://github.com/user-attachments/assets/6f8e6b4e-e2e3-420b-8102-3e2fd6245747)

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
![WhatsApp Image 2025-09-28 at 14 12 31_5b47c856](https://github.com/user-attachments/assets/5dc29a1d-97ce-471a-94b7-9e7d397d1875)

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
![WhatsApp Image 2025-09-28 at 14 16 11_4a549af9](https://github.com/user-attachments/assets/8521450b-eeea-4f6d-a6c4-0668cbf79059)

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
![WhatsApp Image 2025-09-28 at 14 15 52_cb5dacab](https://github.com/user-attachments/assets/e2282acf-0075-4e53-be9e-4ab2b98ed4c9)


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

![WhatsApp Image 2025-09-28 at 14 19 19_55d5476e](https://github.com/user-attachments/assets/84053e63-2851-40bf-a169-240672ed7c7e)

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
![WhatsApp Image 2025-09-28 at 14 17 32_22a1895b](https://github.com/user-attachments/assets/229db691-0fed-44df-95d0-249193e6021d)
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
![WhatsApp Image 2025-09-28 at 14 20 03_b9da08b9](https://github.com/user-attachments/assets/445e45cd-6c03-4349-8aa8-7a59da65189e)

 
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
![WhatsApp Image 2025-09-28 at 14 20 45_ac151c27](https://github.com/user-attachments/assets/9e33fd42-4c42-4039-badd-e15dca939f5e)

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
 ![WhatsApp Image 2025-09-28 at 14 21 36_9adcdc0c](https://github.com/user-attachments/assets/0d07f2b4-f5a8-4233-8693-72f069a68b4b)

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
![WhatsApp Image 2025-09-28 at 14 22 19_243b31dd](https://github.com/user-attachments/assets/312781e9-c696-4ae8-826c-7e4bf3f71dbd)


 cat exread1.sh
```bash
#!/bin/bash
# testing the read command
read -p "Enter your name: " name
echo "Hello $name, welcome to my program. “
``` 
$ chmod 755 exread1.sh 

## OUTPUT

![WhatsApp Image 2025-09-28 at 14 23 07_c883219a](https://github.com/user-attachments/assets/3625541f-4a3e-4bc4-b23b-fe3510d64f76)


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

 ![WhatsApp Image 2025-09-28 at 14 24 12_bd573391](https://github.com/user-attachments/assets/29d2fdc7-3d28-400e-ac82-7fa89c7e08d3)

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
![WhatsApp Image 2025-09-28 at 14 26 30_63728ee1](https://github.com/user-attachments/assets/5189dc69-edf6-4f5f-bf16-97193674383f)
 
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
 ![WhatsApp Image 2025-09-28 at 14 26 30_63728ee1](https://github.com/user-attachments/assets/26fb6a65-9154-4770-847a-473fe2989506)

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
 ![WhatsApp Image 2025-09-28 at 14 27 44_c9bec06d](https://github.com/user-attachments/assets/47911c3c-5f1b-40db-a370-b176809591ef)

 
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
 ![WhatsApp Image 2025-09-28 at 14 28 35_ac007caf](https://github.com/user-attachments/assets/7dcdff5c-fdeb-4c43-ad2f-9e31cbaa72d5)

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

![WhatsApp Image 2025-09-28 at 14 29 17_93596289](https://github.com/user-attachments/assets/0d2320b7-888b-4309-a30d-5e0a511aa84b)

# RESULT:
The Commands are executed successfully.

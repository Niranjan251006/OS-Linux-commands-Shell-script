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
![Screenshot from 2025-03-10 18-31-31](https://github.com/user-attachments/assets/245a539a-cdd3-447e-931f-14d16637f12f)



cat < file2
## OUTPUT
![Screenshot from 2025-03-10 18-32-03](https://github.com/user-attachments/assets/2b2e889d-2ff8-4f7d-9086-0f3774851e0d)


# Comparing Files
cmp file1 file2
## OUTPUT
 ![Screenshot from 2025-03-10 18-32-52](https://github.com/user-attachments/assets/3ecc4a84-a1eb-4d0a-91ae-472592e0f8a3)

comm file1 file2
 ## OUTPUT

 ![Screenshot from 2025-03-10 18-33-50](https://github.com/user-attachments/assets/c25dfa52-e780-41cf-b252-5340bbbe7f25)

diff file1 file2
## OUTPUT
![Screenshot from 2025-03-10 18-34-21](https://github.com/user-attachments/assets/32e6211e-6291-4809-965c-5719db6b4254)


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

![Screenshot from 2025-03-10 18-39-10](https://github.com/user-attachments/assets/0d15bf56-ed02-4e6c-a83e-69ec8920c248)



cut -d "|" -f 1 file22
## OUTPUT
![Screenshot from 2025-03-10 18-40-29](https://github.com/user-attachments/assets/bbda8e3f-87ac-41a7-9fe2-9fe671495276)



cut -d "|" -f 2 file22
## OUTPUT

![Screenshot from 2025-03-10 18-40-45](https://github.com/user-attachments/assets/150f7065-92d0-43bc-8acd-1cc7bd0e2e77)

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
![Screenshot from 2025-03-10 18-44-09](https://github.com/user-attachments/assets/9e51ed4e-a09a-42fd-b145-3060f6afc272)




grep hello newfile 
## OUTPUT
![Screenshot from 2025-03-10 18-44-09](https://github.com/user-attachments/assets/337fff1c-63a1-48c0-b240-106fbfc33183)




grep -v hello newfile 
## OUTPUT
![Screenshot from 2025-03-10 18-45-16](https://github.com/user-attachments/assets/72a3634d-ff1f-48c7-ac3b-7110b675e761)



cat newfile | grep -i "hello"
## OUTPUT
![Screenshot from 2025-03-10 18-46-40](https://github.com/user-attachments/assets/30cab330-5879-4265-ab73-8dba439d66a9)




cat newfile | grep -i -c "hello"
## OUTPUT

![Screenshot from 2025-03-10 18-49-16](https://github.com/user-attachments/assets/bd864fb9-6d58-4ae1-98e8-18fcf4602c0e)



grep -R ubuntu /etc
## OUTPUT

![309630290-22fdcf81-932f-4b8d-8525-a64e0ec2f425](https://github.com/user-attachments/assets/21cde40b-aff0-417b-96fe-9a7379dbba2b)


grep -w -n world newfile   
## OUTPUT

![305804614-3e1bda9a-6ea0-4db2-a568-fbc718c37a19](https://github.com/user-attachments/assets/f5202c32-62d0-4c4e-b660-b4a7eb40d205)

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


![305808474-25d0fec3-0f33-4029-bb7a-8b6dc3d9f165](https://github.com/user-attachments/assets/9047d812-4872-4fae-8a81-31d7bb608536)

egrep -w '(H|h)ello' newfile 
## OUTPUT

![305809631-949add15-11a4-4fe7-84e8-440126aaa9a4](https://github.com/user-attachments/assets/e706c6d4-cadb-47b5-b7e2-155bb7d7d0c0)


egrep -w '(H|h)ell[a-z]' newfile 
## OUTPUT

![305810476-30add5da-a3a2-4363-a53a-130b58db8320](https://github.com/user-attachments/assets/aed4eb51-c223-4486-af40-88ffbddf43c8)



egrep '(^hello)' newfile 
## OUTPUT
![305811443-55b62521-ae26-4c21-a7ef-76af4069aca8](https://github.com/user-attachments/assets/2a02bbce-af1d-4c01-8a2e-0f15b0f639b5)



egrep '(world$)' newfile 
## OUTPUT
![305812168-6231c0d4-c8b0-4331-80ab-b50c2c750dfa](https://github.com/user-attachments/assets/58bc3c4b-f195-4bf4-8d69-9f3d8d418c01)



egrep '(World$)' newfile 
## OUTPUT
![309630312-54bd99ae-8395-4423-a4d5-33985e59bf47](https://github.com/user-attachments/assets/dddc7d50-c230-4123-afe6-f91e6784c3f3)


egrep '((W|w)orld$)' newfile 
## OUTPUT
![305814671-f34d417b-508e-4569-8d0e-e8a3ad4d6b45](https://github.com/user-attachments/assets/2442782c-7363-4a1c-928b-a2ad5b8f1f08)



egrep '[1-9]' newfile 
## OUTPUT
![306316795-d39364c0-71da-42bc-844d-be536727a70f](https://github.com/user-attachments/assets/1d67c7b9-f7c6-4d9b-92df-27b7215cca53)



egrep 'Linux.*world' newfile 
## OUTPUT
![306317421-7149b0f0-5880-435e-8c34-0114f0fa3f94](https://github.com/user-attachments/assets/cb0fa5ef-68ef-44c7-8adc-ac280ac0cf48)


egrep 'Linux.*World' newfile 
## OUTPUT
![309630686-a1558cfd-123d-4d04-a072-edf7f8e194de](https://github.com/user-attachments/assets/1dc9b6ef-a039-44ab-bd45-558a377c62d0)


egrep l{2} newfile
## OUTPUT
![306318648-919d40e4-c1ea-42e1-9645-de17925281f8](https://github.com/user-attachments/assets/386c7e85-7a33-4fa9-a8af-3801db5ad757)



egrep 's{1,2}' newfile
## OUTPUT 
![306319020-cea59baf-267b-419f-aee4-2673da56d2d5](https://github.com/user-attachments/assets/59bf594c-2d97-48ba-b06a-e4d43aaaeaf7)



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

![306320295-98b8fafa-04d2-41ed-ad0a-f1230817d95a](https://github.com/user-attachments/assets/3de55afc-3e5e-4d7e-ae7c-540305e40fd5)


sed -n -e '$p' file23
## OUTPUT
![306320509-b660c572-1734-40ce-be88-9252a60d9aa3](https://github.com/user-attachments/assets/5ba5cbd3-6c4e-400d-8ad8-ddb8d1368da2)



sed  -e 's/Ram/Sita/' file23
## OUTPUT
![306320967-dbb7abdd-1f69-4e0f-8433-2953261eb789](https://github.com/user-attachments/assets/74663235-1aa7-4e53-8a30-e240d1baff68)



sed  -e '2s/Ram/Sita/' file23
## OUTPUT
![306322946-6aa29cfd-6b07-4d27-b36e-1b14d1cb2e7e](https://github.com/user-attachments/assets/51a8bc60-ef58-4ac9-8b6d-c6a5f68a7816)



sed  '/tom/s/5000/6000/' file23
## OUTPUT

![309630812-30f5c5a9-9c75-43f0-8ad1-38df5d8c8177](https://github.com/user-attachments/assets/cc13e867-419d-41c7-a568-eb656e902528)


sed -n -e '1,5p' file23
## OUTPUT
![306323531-0257c450-9623-4f9c-a9fa-376e59ea41eb](https://github.com/user-attachments/assets/41c280a1-934b-49f7-9941-f063b04c3e99)



sed -n -e '2,/Joe/p' file23
## OUTPUT
![306324580-13bd70de-b1df-4d66-91f4-400ca29f4092](https://github.com/user-attachments/assets/e8c86349-a6cf-47d8-930d-dc92f28f9020)




sed -n -e '/tom/,/Joe/p' file23
## OUTPUT

![306324859-f4130ac3-9533-4d96-8f07-cabd48ddeb4b](https://github.com/user-attachments/assets/7a0f9182-d67f-4e59-8e6a-861439cf2348)


seq 10 
## OUTPUT
![306325086-6878d8f6-6916-4079-9662-041241ba0fb7](https://github.com/user-attachments/assets/eb5f8b77-c33e-427a-8008-ca7326decad4)



seq 10 | sed -n '4,6p'
## OUTPUT

![306325371-81bde4e8-4de7-46ae-a6ab-91a67224ad05](https://github.com/user-attachments/assets/977a95ee-d8ce-4247-adc1-8235457d24dc)


seq 10 | sed -n '2,~4p'
## OUTPUT

![306325717-fd8471e6-bc9a-43b1-aa5d-573add27fa89](https://github.com/user-attachments/assets/9d876174-daaf-43fd-9c8a-36539769f1c0)


seq 3 | sed '2a hello'
## OUTPUT
![306327286-444759b0-3989-40f1-add9-59938cbb27f1](https://github.com/user-attachments/assets/236efd80-a815-4a92-b333-61153dbd1985)



seq 2 | sed '2i hello'
## OUTPUT
![306327545-f725afb5-e8b8-4694-b49c-b8a0c813a692](https://github.com/user-attachments/assets/ace0cafa-cc0f-4c5b-a0f7-ff331348d681)


seq 10 | sed '2,9c hello'
## OUTPUT
![306327729-a00f2a8c-4b7d-4822-99cf-83263a691c6a](https://github.com/user-attachments/assets/cbd0512b-009b-46ab-8756-11470f3c1a0d)


sed -n '2,4{s/^/$/;p}' file23
## OUTPUT
![306328394-d04ee7c2-46ee-43ac-93b2-0ea156edc231](https://github.com/user-attachments/assets/0cb90cf9-db9e-4714-b94e-5c51a2c2b82f)




sed -n '2,4{s/$/*/;p}' file23
![306328394-d04ee7c2-46ee-43ac-93b2-0ea156edc231](https://github.com/user-attachments/assets/6123adf8-982d-4b61-92c3-73d52ae950e9)


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
![306330202-0fa515bd-81b8-4cb3-8d49-4e050065141e](https://github.com/user-attachments/assets/59a06be6-f976-4a61-b4aa-9dd07d58d3ad)


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
![306330904-47a9031a-70e8-4290-ab78-aee3b3336700](https://github.com/user-attachments/assets/1af8e4e2-c201-4ac2-a304-37d4459bff53)



#Using tr command

cat file23 | tr [:lower:] [:upper:]
 ## OUTPUT
![306331301-3a8b94a3-b62c-4e2d-ba61-6b952493ee12](https://github.com/user-attachments/assets/c17b689d-41be-46d1-a5f5-bf01538a4ec6)

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
![306538649-bfeb1938-f6da-4d70-a305-87724b6f9b66](https://github.com/user-attachments/assets/78e12d60-ddd6-475d-8574-24da16ab7028)


 
cat urllist.txt | tr -d ' ' | tr -s '.'
## OUTPUT

![306538982-a0a2671d-6f19-4682-bd0d-36e82d2a7048](https://github.com/user-attachments/assets/dbf167c7-83e3-4b6d-8948-dc64b67c02f0)


#Backup commands
tar -cvf backup.tar *
## OUTPUT
![309631309-4c9a04e6-dfe5-4928-af8f-b4f35f38d37c](https://github.com/user-attachments/assets/f21f2971-ce76-494e-b85b-ff97f4fc175e)


mkdir backupdir
 
mv backup.tar backupdir
 
tar -tvf backup.tar
## OUTPUT

![309631412-ccbc4154-17d8-4dc5-bbaf-0896a668b8a5](https://github.com/user-attachments/assets/19ca977e-8332-4f29-a17f-8d3b9d1173ed)

tar -xvf backup.tar
## OUTPUT
![309631509-0d5efaa0-863c-4b17-9ed8-3e9dd6f09955](https://github.com/user-attachments/assets/36834bfc-2236-4616-9d8a-aeba6e47d341)


gzip backup.tar
## OUTPUT
![309631509-0d5efaa0-863c-4b17-9ed8-3e9dd6f09955](https://github.com/user-attachments/assets/bf843114-f8a3-4afa-b227-07027101e783)

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
![309631646-8b571dc0-2f93-4ab2-a314-0055d7559ee3](https://github.com/user-attachments/assets/f234a4ba-330c-4562-b35a-8fc20be028da)

 
cat << stop > herecheck.txt
```
hello in this world
i cant stop
for this non stop movement
stop
```

cat herecheck.txt
## OUTPUT
![306541597-f05197ce-9a61-4432-8677-06f9a3f2074d](https://github.com/user-attachments/assets/1d34842b-70be-459b-9f72-3b3fb6624be6)


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
![309631701-66ce463b-a769-4ce7-9701-472a735ec84e](https://github.com/user-attachments/assets/79d68f20-9436-4190-8ff6-3126c5c9c73a)

 
ls file1
## OUTPUT
![306542056-6d43e64c-5b38-4b4c-953d-15306e4f0962](https://github.com/user-attachments/assets/a6291725-7fdd-43a2-986f-0cc4186a31dc)

echo $?
## OUTPUT 
./one
bash: ./one: Permission denied
 
echo $?
## OUTPUT 
 ![306542294-e207d92e-1b49-4f24-bf5e-6b509e151ca3](https://github.com/user-attachments/assets/2bbecf6f-5808-433a-a1c6-db91bdfe5ec2)

abcd
 
echo $?
 ## OUTPUT
![306542294-e207d92e-1b49-4f24-bf5e-6b509e151ca3](https://github.com/user-attachments/assets/ce8ec05e-5d06-403d-9c1b-47d242480969)


 
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
![307678773-f5691f96-7fb8-405b-aca8-99b245694866](https://github.com/user-attachments/assets/1c46d91a-6ff0-4922-80fa-3ec0abbbffaa)


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
![307679532-9e14508f-e06b-48bd-8335-24ab45869507](https://github.com/user-attachments/assets/3883645c-bdd6-4235-a66c-49f23002157a)

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

![307680054-a3bbfe31-a584-41fa-bb8e-34f6a8c71c2d](https://github.com/user-attachments/assets/870f1883-ae1d-49cf-a64e-99bc73b0605b)


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
![307680530-f0324dc3-e174-4c13-9e62-2b8e12f0ece8](https://github.com/user-attachments/assets/53af98ec-204e-465b-b0f0-9a517e80e864)

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
![307681129-4d51cbe0-75a7-4c8b-9897-31d80e242b23](https://github.com/user-attachments/assets/4f482401-4406-403f-a157-9902c3092533)


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

![307682021-b23da05d-9057-4155-a3b3-e0d5e1658424](https://github.com/user-attachments/assets/c482de8e-7fad-4114-8617-d1bcc0881e1c)

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
![307682427-dd2856b3-6746-4001-9bb5-64248d70cbf2](https://github.com/user-attachments/assets/b176610d-854a-49e5-8e0b-f1020480bacd)

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
 ![307682893-2089b93c-f8f4-4aa2-9a14-7ad18c022649](https://github.com/user-attachments/assets/47fe6098-bc95-462f-8315-0340c6f3743d)

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

 ![309632182-01d121de-472d-4dbd-b7b9-3b02b5273151](https://github.com/user-attachments/assets/88630df5-5981-44b6-9c92-076be5633441)

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
 ## OUTPUT:
 
 ![309632243-37852111-38c2-4d5b-b02e-db081bb55911](https://github.com/user-attachments/assets/5beeab18-1729-48e6-b045-5b696590dae0)

 
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
 ## OUTPUT:
 ![308472685-5db0aa23-2b65-47be-845b-d27e71d1cf0e](https://github.com/user-attachments/assets/08afa233-3b7d-4b49-a194-b7ea38ace531)
 
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
 
$ ./forin2.s
![308473693-e871a57b-eba5-4f24-beaa-b50a1cc05f9d](https://github.com/user-attachments/assets/c554c961-0343-40a2-9cf7-f5d8fc150f26)
h 
 
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
![308474292-3e502c00-aa25-42d7-94f4-c1cf42abbeb0](https://github.com/user-attachments/assets/111fccf0-4eca-467d-9d39-ccfbf482efb1)

 
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
![308474845-57eb9b7e-55ed-4f8a-b04f-299ca7312d54](https://github.com/user-attachments/assets/6a2a8ba1-bc06-4e4d-a4b8-e70ecd54f768)

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

![308475810-23e57dee-3012-407b-a599-187a55addb7b](https://github.com/user-attachments/assets/a24ce304-0157-45fc-a5f0-87c1ec7cb7d0)

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
![308478403-2811cf5c-8f23-497a-8175-1e53557b62ab](https://github.com/user-attachments/assets/338088d1-1bdc-4271-b350-e2a315c7a6db)

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
![309632774-25c8eba9-2ae6-4b0d-aee8-0f5bdc40756f](https://github.com/user-attachments/assets/80c58987-e477-47a1-858b-775bd859a775)


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
![309632814-7ff92879-790a-4e10-b53d-b3f846385518](https://github.com/user-attachments/assets/c9608779-1aa6-4aff-b8d0-315819cc8a3f)

 
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
![308486165-605c7e2c-66cc-4915-b199-f4a7fe1f3dc7](https://github.com/user-attachments/assets/fe2f2372-3b9e-4c88-bcb2-c009a2fef6bf)

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

 ![316738281-0765d54a-32b7-4dab-aee7-73ba559f2404](https://github.com/user-attachments/assets/4f831b63-e146-4189-ad55-50f684151700)

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

![316740804-7ee0fda7-4aee-48b9-b66c-db62420186d5](https://github.com/user-attachments/assets/797dc51e-2151-4fe1-9dfc-11a9343a1c59)


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
![316740804-7ee0fda7-4aee-48b9-b66c-db62420186d5](https://github.com/user-attachments/assets/a8050b22-74eb-49f4-b711-cb04a5919f19)

 
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
 ![316738750-fbf0ccbc-30fd-4ba9-8017-efa27261d721](https://github.com/user-attachments/assets/1feb8e77-ea7b-4ea9-83e6-6fceef9ab738)

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
![316738765-b564ab36-5649-4d4f-b1e4-a269609ab7d7](https://github.com/user-attachments/assets/ea2c0b82-aeea-43da-8f47-0506db30ef4a) 
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
 ![316738796-d0fd2ccc-8439-46b4-b072-8a78cd3503db](https://github.com/user-attachments/assets/27db8e4a-0958-47c0-8f0e-eb572067df58)


cat > pal
in
drome.sh
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
![316739033-1daf5b3a-3394-47b0-ac6f-32a86e8c83f0](https://github.com/user-attachments/assets/95eeecb4-7536-4cd2-a146-a50edc857ecb)


# RESULT:
The Commands are executed successfully.

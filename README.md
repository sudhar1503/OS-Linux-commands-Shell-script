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
## OUTPUT
![alt text](1.png)

cat > file2
```
anil aggarwal
barun sengupta
c.k. shukla
lalit chowdury
s.n. dasgupta
^d
```
## OUTPUT
![alt text](2.png)

### Display the content of the files
cat < file1
## OUTPUT
![alt text](3.png)

cat < file2
## OUTPUT
![alt text](4.png)

# Comparing Files
cmp file1 file2

## OUTPUT
 ![alt text](5.png)

comm file1 file2
 ## OUTPUT
![alt text](6.png)
 
diff file1 file2
## OUTPUT
![alt text](7.png)

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
![alt text](8.png)

cut -d "|" -f 1 file22
## OUTPUT
![alt text](9.png)

cut -d "|" -f 2 file22
## OUTPUT
![alt text](10.png)

cat < newfile 
```
Hello world
hello world
^d
```
cat > newfile 
Hello world
hello world
 
grep Hello newfile 
## OUTPUT
![alt text](11.png)


grep hello newfile 
## OUTPUT
![alt text](12.png)


grep -v hello newfile 
## OUTPUT
![alt text](13.png)


cat newfile | grep -i "hello"
## OUTPUT
![alt text](14.png)




cat newfile | grep -i -c "hello"
## OUTPUT
![alt text](15.png)



grep -R "kalilinux" /etc
## OUTPUT
![alt text](16.png)


grep -w -n world newfile   
## OUTPUT
![alt text](17.png)

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
![Screenshot From 2025-04-29 14-27-19](https://github.com/user-attachments/assets/04f0f1ee-3466-42d2-92a4-3bd7ff3a1787)



egrep -w '(H|h)ello' newfile 
## OUTPUT
![Screenshot From 2025-04-29 14-27-33](https://github.com/user-attachments/assets/9de7ec66-2c6e-47cf-947b-b14ef79cddb5)


egrep -w '(H|h)ell[a-z]' newfile 
## OUTPUT

![Screenshot From 2025-04-29 14-37-14](https://github.com/user-attachments/assets/4815d2e7-a51f-41d1-b065-f6f9a4dd9069)



egrep '(^hello)' newfile 
## OUTPUT
![Screenshot From 2025-04-29 14-37-27](https://github.com/user-attachments/assets/cc9378d6-a8c0-4279-8105-84eed894cdbf)



egrep '(world$)' newfile 
## OUTPUT
![Screenshot From 2025-04-29 14-37-32](https://github.com/user-attachments/assets/c91d7b20-7fa1-4923-b2dc-a39a723e02be)



egrep '(World$)' newfile 
## OUTPUT
![Screenshot From 2025-04-29 14-37-38](https://github.com/user-attachments/assets/11715f37-1da2-4757-a486-3ba308b47361)


egrep '((W|w)orld$)' newfile 
## OUTPUT
![Screenshot From 2025-04-29 14-37-47](https://github.com/user-attachments/assets/b4c79bd3-423e-409d-9498-5659470f50e2)



egrep '[1-9]' newfile 
## OUTPUT

![Screenshot From 2025-04-29 14-39-11](https://github.com/user-attachments/assets/7c81292c-7222-4680-95d5-71abd929b789)




egrep 'Linux.*world' newfile 
## OUTPUT
![Screenshot From 2025-04-29 14-39-21](https://github.com/user-attachments/assets/63266161-66a1-4462-bf1c-43625e886f5c)


egrep 'Linux.*World' newfile 
## OUTPUT
![Screenshot From 2025-04-29 14-39-30](https://github.com/user-attachments/assets/8946d8c3-5079-44c1-8e62-6a267b409803)


egrep l{2} newfile
## OUTPUT
![Screenshot From 2025-04-29 14-39-48](https://github.com/user-attachments/assets/cc1c76d6-e46b-4b3a-a96c-a80d338258fc)



egrep 's{1,2}' newfile
## OUTPUT 
![Screenshot From 2025-04-29 14-40-01](https://github.com/user-attachments/assets/27ea2439-7498-47c2-8d63-872ac07ed63c)


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

![Screenshot From 2025-04-29 14-40-14](https://github.com/user-attachments/assets/c9f2eab8-219b-4aef-a834-d183c6e20185)

sed -n -e '$p' file23
## OUTPUT

![Screenshot From 2025-04-29 14-40-39](https://github.com/user-attachments/assets/40300fbd-5b31-4ad2-b214-f912f389f641)


sed  -e 's/Ram/Sita/' file23
## OUTPUT
![Screenshot From 2025-04-29 14-40-51](https://github.com/user-attachments/assets/ded05a21-a771-4b50-91cd-3eab379db66e)



sed  -e '2s/Ram/Sita/' file23
## OUTPUT
![Screenshot From 2025-04-29 14-41-08](https://github.com/user-attachments/assets/4cc053b0-4baf-45f9-a80c-f9e816c765ad)



sed  '/tom/s/5000/6000/' file23
## OUTPUT
![Screenshot From 2025-04-29 14-41-17](https://github.com/user-attachments/assets/2476d247-f98e-4349-a52a-f6703201afb4)



sed -n -e '1,5p' file23
## OUTPUT
![Screenshot From 2025-04-29 14-41-34](https://github.com/user-attachments/assets/d949de84-631c-4f48-8625-e248df652fb4)



sed -n -e '2,/Joe/p' file23
## OUTPUT
![Screenshot From 2025-04-29 14-42-11](https://github.com/user-attachments/assets/e7cf3566-e1ce-4bfb-81b2-8d72c4fb2d24)




sed -n -e '/tom/,/Joe/p' file23
## OUTPUT
![Screenshot From 2025-04-29 14-42-42](https://github.com/user-attachments/assets/aa9c4447-cb35-4b83-b509-61764c54d472)



seq 10 
## OUTPUT
![Screenshot From 2025-04-29 14-43-07](https://github.com/user-attachments/assets/c507c9f7-3f60-4bc1-bbbd-3f27e39b8f39)



seq 10 | sed -n '4,6p'
## OUTPUT
![Screenshot From 2025-04-29 14-43-34](https://github.com/user-attachments/assets/71668284-9c74-4ad8-9d54-894396614c76)



seq 10 | sed -n '2,~4p'
## OUTPUT
![Screenshot From 2025-04-29 14-43-43](https://github.com/user-attachments/assets/5a2f1385-042f-4004-923f-c069f5a02038)



seq 3 | sed '2a hello'
## OUTPUT
![Screenshot From 2025-04-29 14-43-55](https://github.com/user-attachments/assets/b8f21266-22db-4900-a57f-3f9f6b43b3fe)



seq 2 | sed '2i hello'
##OUTPUT
![Screenshot From 2025-04-29 14-44-06](https://github.com/user-attachments/assets/d87bdb11-1434-41b8-b8d3-e8a1010ab026)

seq 10 | sed '2,9c hello'
## OUTPUT
![Screenshot From 2025-04-29 14-44-12](https://github.com/user-attachments/assets/ff675226-8245-4561-8ac5-ae8773f16b0a)


sed -n '2,4{s/^/$/;p}' file23
## OUTPUT
![Screenshot From 2025-04-29 14-44-25](https://github.com/user-attachments/assets/7e30920d-72d0-47fd-bc3b-8d7d763ba1d4)



sed -n '2,4{s/$/*/;p}' file23
## OUTPUT
![Screenshot From 2025-04-29 14-44-34](https://github.com/user-attachments/assets/503dea72-4aa1-4cef-b4d1-06b4d07f4c7f)


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
![Screenshot From 2025-05-05 14-47-57](https://github.com/user-attachments/assets/bc6a505f-e7df-4ebb-b933-08b460135601)


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
![Screenshot From 2025-04-29 14-44-53](https://github.com/user-attachments/assets/98476f15-e939-4952-9a3c-fe679e5bb175)



## Using tr command

cat file23 | tr [:lower:] [:upper:]
## OUTPUT
 ![Screenshot From 2025-04-29 14-45-11](https://github.com/user-attachments/assets/e807e0f5-3b4f-4435-9a88-e46e06f5a0db)

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
![Screenshot From 2025-05-05 14-48-40](https://github.com/user-attachments/assets/bc6cae1b-68bd-4c77-8129-4fab806b1068)


 
cat urllist.txt | tr -d ' ' | tr -s '.'
## OUTPUT

![Screenshot From 2025-05-05 14-49-13](https://github.com/user-attachments/assets/8d9b664f-9b19-4a4e-b93f-e77beb096105)


## Backup commands
tar -cvf backup.tar *
## OUTPUT
![Screenshot From 2025-05-05 14-49-57](https://github.com/user-attachments/assets/b5a79259-1e04-4ee0-9cdb-444ff4ca4822)


mkdir backupdir
## OUTPUT
 ![Screenshot From 2025-05-05 14-56-39](https://github.com/user-attachments/assets/0a98825a-dd30-4ec9-b4e1-9156c0e6f2b1)

mv backup.tar backupdir
## OUTPUT
 ![Screenshot From 2025-05-05 14-56-51](https://github.com/user-attachments/assets/ad2fa69e-0f24-4007-9a59-9f3a5881cc92)

tar -tvf backup.tar
## OUTPUT
![Screenshot From 2025-05-05 14-53-36](https://github.com/user-attachments/assets/399ffb8f-7362-4981-b988-a53d0173642c)


tar -xvf backup.tar
## OUTPUT

![Screenshot From 2025-05-05 15-09-13](https://github.com/user-attachments/assets/7af35c3e-d49b-473b-86d9-984a0473cc06)


gzip backup.tar
ls *.gz

## OUTPUT
![Screenshot From 2025-05-05 15-09-30](https://github.com/user-attachments/assets/45fcc918-f449-40ab-8130-b504a1f38a2e)

 
gunzip backup.tar.gz
## OUTPUT
![Screenshot From 2025-05-05 15-09-46](https://github.com/user-attachments/assets/3ce75910-279c-4db1-b9db-179831b3072d)

 
# Shell Script
```
echo '#!/bin/sh' > my-script.sh
echo 'echo Hello World‘; exit 0 >> my-script.sh
```
chmod 755 my-script.sh
./my-script.sh
## OUTPUT
![Screenshot From 2025-05-05 16-31-36](https://github.com/user-attachments/assets/b5025ff2-b669-4cb7-846f-b03b6e6d86d1)

 
cat << stop > herecheck.txt
```
hello in this world
i cant stop
for this non stop movement
stop
```

cat herecheck.txt
## OUTPUT
![Screenshot From 2025-05-05 16-32-16](https://github.com/user-attachments/assets/2b69223a-37a6-48d1-8c2b-cb651915bdd2)


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
![Screenshot From 2025-05-05 16-32-58](https://github.com/user-attachments/assets/b814cf25-804c-4f22-a21a-008d1162e9e6)

 
ls file1
## OUTPUT
![Screenshot From 2025-05-05 16-33-14](https://github.com/user-attachments/assets/01ce4931-f05f-4c5a-9684-09da47654c31)

echo $?
## OUTPUT 
![Screenshot From 2025-05-05 16-33-24](https://github.com/user-attachments/assets/d560da30-b7f3-4e52-82af-7e808b53344b)

./one
bash: ./one: Permission denied
 
echo $?
# OUTPUT 
#![Screenshot From 2025-05-05 16-33-34](https://github.com/user-attachments/assets/e3456778-f340-4c4c-9d98-be58ba8ec821)
 
abcd
 
echo $?
 ## OUTPUT
![Screenshot From 2025-05-05 16-33-51](https://github.com/user-attachments/assets/51376a37-9b7e-44d6-8da9-edf03a150217)


 
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

chmod 755 strcomp.sh
 
./strcomp.sh 

## OUTPUT
![Screenshot From 2025-05-05 16-34-04](https://github.com/user-attachments/assets/d11d1220-fdc1-4385-8dd6-c6cb627ae9a6)


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
chmod 755 psswdperm.sh

./psswdperm.sh

## OUTPUT
![Screenshot From 2025-05-05 16-34-37](https://github.com/user-attachments/assets/c83579f4-10d1-4c34-8bbe-18402eab44fd)

# check if with file location
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

$ chmod 755 ifnested.sh

./ifnested.sh 

## OUTPUT

![Screenshot From 2025-05-05 16-34-56](https://github.com/user-attachments/assets/c4dd8bfb-16b9-49a7-b8d7-6adaf3c3ce40)


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
![Screenshot From 2025-05-05 16-35-07](https://github.com/user-attachments/assets/21cf103d-a323-42e8-9a84-8a0aa05f0e9b)

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
![Screenshot From 2025-05-05 16-34-56](https://github.com/user-attachments/assets/664d35e0-251c-4c0f-8753-16e7ed810b36)


# looking for a possible value using elif
cat > elifcheck.sh 
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

![Screenshot From 2025-05-05 16-35-29](https://github.com/user-attachments/assets/37242c7a-968d-4342-bdd2-5c3397e513ed)



# testing compound comparisons
cat > ifcompound.sh 
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

![Screenshot From 2025-05-05 16-35-44](https://github.com/user-attachments/assets/36fe5686-f941-4fab-9977-c7cc7370e622)

# using the case command
cat > casecheck.sh 
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
![Screenshot From 2025-05-05 16-36-01](https://github.com/user-attachments/assets/a904a24c-92bd-40d1-af7c-8b3b2e7dc86a)

 
cat > whiletest.sh
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
 
 ![Screenshot From 2025-05-05 16-36-20](https://github.com/user-attachments/assets/bfe5359f-f0ec-4e07-94e1-5eca53c29200)

 
cat >  untiltest.sh 
```bash
\#using the until command
#!/bin/bash
var1=100
until [ $var1 -eq 0 ]
do
echo $var1
var1=$[ $var1 - 25 ]
done
``` 
$ chmod 755 untiltest.sh

$ ./untiltest.sh
 
## OUTPUT
 ![Screenshot From 2025-05-05 16-37-04](https://github.com/user-attachments/assets/47d08c65-cdf1-402f-ba2b-3ca452d068f4)

 
cat > forin1.sh 
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

## OUTPUT
 ![Screenshot From 2025-05-05 16-37-16](https://github.com/user-attachments/assets/10a40709-a84f-48e9-967f-a1bbe5e63e70)

 
cat > forin2.sh 
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
 ![Screenshot From 2025-05-05 16-37-31](https://github.com/user-attachments/assets/e4c2a463-3d8d-4450-bafd-627273375c7b)


cat > forin3.sh 
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

## OUTPUT
![Screenshot From 2025-05-05 16-38-18](https://github.com/user-attachments/assets/938c6c3a-052d-4def-8e2b-66c4ca8674f6)


$ cat > cities
```
Hyderabad
Alampur
Basara
Warangal
Adilabad
Bhadrachalam
Khammam
```
cat > forinfile.sh 
```bash
#!/bin/bash
# reading values from a file
file="cities"

for state in $(cat "$file")
do
  echo "Visit beautiful $state"
done
```
$ chmod 777 forinfile.sh

$ ./forinfile.sh

## OUTPUT

![Screenshot From 2025-05-05 16-38-35](https://github.com/user-attachments/assets/7be9eb97-cdbd-4dba-ad3e-addc24e1b318)


cat > forctype.sh 
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
![Screenshot From 2025-05-05 16-38-48](https://github.com/user-attachments/assets/d7e49c60-00d4-4f37-8d47-05512bb5bc72)

cat > forctype1.sh 
```bash
#!/bin/bash
# multiple variables
for (( a=1, b=5; a <= 5; a++, b-- ))
do
echo "$a - $b"
done
```
$ chmod 755 forctype1.sh

$ ./forctype1.sh 

## OUTPUT
![Screenshot From 2025-05-05 16-38-56](https://github.com/user-attachments/assets/2072194f-1449-407d-bea7-d2cdb707abfc)

cat > fornested1.sh 
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
![Screenshot From 2025-05-05 16-39-07](https://github.com/user-attachments/assets/d2700b10-31fd-4ba6-b38b-f112cfeb90dd)

 
cat > forbreak.sh 
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
$ chmod 755 forbreak.sh

$ ./forbreak.sh 

## OUTPUT
![Screenshot From 2025-05-05 16-39-20](https://github.com/user-attachments/assets/ac390cdf-8049-43f2-a2ad-350cefb7641b)

 
 
cat > forcontinue.sh 
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

 ![Screenshot From 2025-05-05 16-39-34](https://github.com/user-attachments/assets/088e5bb3-63ed-4a11-a6eb-42ae081d5945)

cat > exread.sh 
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
![Screenshot From 2025-05-05 16-39-49](https://github.com/user-attachments/assets/7ca466d7-be40-4598-9b3f-a15c907dfa70)


 cat > exread1.sh
```bash
#!/bin/bash
# testing the read command
read -p "Enter your name: " name
echo "Hello $name, welcome to my program."

``` 
$ chmod 755 exread1.sh 

$ ./exread1.sh 

## OUTPUT

![Screenshot From 2025-05-05 16-40-11](https://github.com/user-attachments/assets/16e8fb66-4738-4ef1-824b-0e9307dba901)

 
cat > funcex.sh
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

$ ./funcex.sh 1 2

## OUTPUT

 ![Screenshot From 2025-05-05 16-40-25](https://github.com/user-attachments/assets/828a7532-6258-4dc5-8ad5-36b5f30e3b93)


 
cat > argshift.sh
```bash
#!/bin/bash 
 while (( "$#" )); do 
  echo $1 
  shift 
done
```
$ chmod 777 argshift.sh

$ ./argshift.sh 1 2 3

## OUTPUT
 ![Screenshot From 2025-05-05 16-40-41](https://github.com/user-attachments/assets/66a9294b-f226-4304-bb8b-02f2fa6cc41d)

 cat > argshift1.sh
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
$ chmod 777 argshift1.sh

$ ./argshift1.sh 1 2 3

## OUTPUT

 ![Screenshot From 2025-05-05 16-41-25](https://github.com/user-attachments/assets/309d6b40-42d6-494c-9b87-6c6c864b9076)

cat > argshift2.sh
```bash
#!/bin/bash 
set -x 
while (( "$#" )); do 
  echo $1 
  shift 
done
set +x
```
$ chmod 777 argshift2.sh
$
./argshift2.sh 1 2 3

## OUTPUT
 ![Screenshot From 2025-05-05 16-41-43](https://github.com/user-attachments/assets/1f37e4f9-43d9-4b1d-838b-45787da5032f)

 
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
cat > data.dat
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
$ awk -f nc.awk data.dat

## OUTPUT 
![Screenshot From 2025-05-05 16-42-19](https://github.com/user-attachments/assets/2ad354f1-de44-4ef1-93ca-5bbbd8b88e7a)
 
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
$ chmod 777 palindrome.sh

$ ./palindrome.sh 1 2 3

## OUTPUT 

![Screenshot From 2025-05-05 16-42-42](https://github.com/user-attachments/assets/db2c7b8a-9342-4c12-a091-1f142da56816)


# RESULT:
The Commands are executed successfully.

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

<img width="626" height="182" alt="image" src="https://github.com/user-attachments/assets/91ae81f4-c082-4078-aedf-5544c12f47a3" />




cat < file2
## OUTPUT
<img width="655" height="206" alt="image" src="https://github.com/user-attachments/assets/3a49e9ac-04ac-42e9-b97e-0dc127dc47b1" />



# Comparing Files
cmp file1 file2
## OUTPUT
<img width="575" height="79" alt="image" src="https://github.com/user-attachments/assets/1981146b-bc29-4587-b47b-01761b3ee899" />

 
comm file1 file2
 ## OUTPUT
 <img width="579" height="204" alt="image" src="https://github.com/user-attachments/assets/febd505c-dafc-4505-8779-e7cd12d71edb" />


 
diff file1 file2
## OUTPUT

<img width="680" height="314" alt="image" src="https://github.com/user-attachments/assets/90297aff-ad18-43f6-b109-cf0476860af8" />

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
<img width="626" height="112" alt="image" src="https://github.com/user-attachments/assets/d865e337-b17a-4909-81c7-e271ad0b2142" />





cut -d "|" -f 1 file22
## OUTPUT
<img width="655" height="129" alt="image" src="https://github.com/user-attachments/assets/984f291d-106d-4c2c-bc65-0d63060cd79a" />



cut -d "|" -f 2 file22
## OUTPUT
<img width="633" height="123" alt="image" src="https://github.com/user-attachments/assets/757ce4b8-4bbf-40a8-a0bd-0b13470b543c" />



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
<img width="566" height="74" alt="image" src="https://github.com/user-attachments/assets/278a8a0e-bb30-4b9f-bc8d-65f6965e5909" />




grep hello newfile 
## OUTPUT
<img width="566" height="74" alt="image" src="https://github.com/user-attachments/assets/c6c23a37-a837-444c-aa49-9b42cf922b7b" />





grep -v hello newfile 
## OUTPUT
<img width="588" height="70" alt="image" src="https://github.com/user-attachments/assets/7d71c6ed-9992-47bf-992e-838ec811af45" />




cat newfile | grep -i "hello"
## OUTPUT
<img width="588" height="70" alt="image" src="https://github.com/user-attachments/assets/7d71c6ed-9992-47bf-992e-838ec811af45" />




cat newfile | grep -i -c "hello"
## OUTPUT
<img width="573" height="74" alt="image" src="https://github.com/user-attachments/assets/6acc6a82-bccb-4997-b6bd-8c0af6862007" />





grep -R ubuntu /etc
## OUTPUT

<img width="804" height="590" alt="image" src="https://github.com/user-attachments/assets/fec37585-beb6-4f91-8f5b-895137f7b52a" />



grep -w -n world newfile   
## OUTPUT
<img width="565" height="96" alt="image" src="https://github.com/user-attachments/assets/614dbf53-c937-493f-9b71-6e87f6ca86dc" />



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
<img width="534" height="96" alt="image" src="https://github.com/user-attachments/assets/b48bbd9e-3ef6-443b-9e32-07901ec7ffa6" />



egrep -w '(H|h)ello' newfile 
## OUTPUT
<img width="542" height="87" alt="image" src="https://github.com/user-attachments/assets/d43e2c78-7c86-4c76-b8b5-60ac69ccb37c" />




egrep -w '(H|h)ell[a-z]' newfile 
## OUTPUT

<img width="570" height="101" alt="image" src="https://github.com/user-attachments/assets/25470d12-9291-4afc-9007-9d3e636fac66" />



egrep '(^hello)' newfile 
## OUTPUT
<img width="553" height="68" alt="image" src="https://github.com/user-attachments/assets/a1fcb258-d8f9-4fc9-877c-10a4a6e70256" />




egrep '(world$)' newfile 
## OUTPUT
<img width="541" height="92" alt="image" src="https://github.com/user-attachments/assets/77b8dbd1-92d2-490f-b1d6-1961582ac0cd" />



egrep '(World$)' newfile 
## OUTPUT
<img width="556" height="85" alt="image" src="https://github.com/user-attachments/assets/ba3f446d-030e-4dd8-ac1b-810046800ed0" />



egrep '((W|w)orld$)' newfile 
## OUTPUT
<img width="614" height="127" alt="image" src="https://github.com/user-attachments/assets/84c0604f-804c-4ef2-9967-8f860afa07e0" />





egrep '[1-9]' newfile 
## OUTPUT

<img width="568" height="80" alt="image" src="https://github.com/user-attachments/assets/10e295d8-0f90-4b69-997a-5006aa55c22b" />


egrep 'Linux.*world' newfile 
## OUTPUT
<img width="513" height="66" alt="image" src="https://github.com/user-attachments/assets/cb276a22-1bd2-4699-80f5-7a332cb3ea7f" />


egrep 'Linux.*World' newfile 
## OUTPUT
<img width="540" height="76" alt="image" src="https://github.com/user-attachments/assets/9c9fc5f9-5d88-4e05-abd8-df24ff6fa0ef" />


egrep l{2} newfile
## OUTPUT
<img width="531" height="110" alt="image" src="https://github.com/user-attachments/assets/126d1c0b-23d7-42b4-97c8-087180d9b299" />



egrep 's{1,2}' newfile
## OUTPUT 
<img width="610" height="126" alt="image" src="https://github.com/user-attachments/assets/03614509-2d69-48b8-ac66-0c7b1a9b7ca0" />



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
<img width="573" height="73" alt="image" src="https://github.com/user-attachments/assets/5f3df474-4f35-4b2b-b5bf-9c9e79eee20e" />



sed -n -e '$p' file23
## OUTPUT

<img width="535" height="73" alt="image" src="https://github.com/user-attachments/assets/def15c66-38ae-4df8-8e5b-64a4bbf0d83f" />


sed  -e 's/Ram/Sita/' file23
## OUTPUT
<img width="542" height="268" alt="image" src="https://github.com/user-attachments/assets/d6286fbb-b5e1-4cea-9848-1b802c18ae5a" />



sed  -e '2s/Ram/Sita/' file23
## OUTPUT
<img width="550" height="272" alt="image" src="https://github.com/user-attachments/assets/a07aa8b8-139c-48c5-a5bd-c88a56f5b01a" />



sed  '/tom/s/5000/6000/' file23
## OUTPUT
<img width="541" height="283" alt="image" src="https://github.com/user-attachments/assets/16428be5-4dc1-409c-a8b1-ea502b588933" />



sed -n -e '1,5p' file23
## OUTPUT
<img width="543" height="177" alt="image" src="https://github.com/user-attachments/assets/9005135d-d1de-4ad8-b229-6c349515e41d" />



sed -n -e '2,/Joe/p' file23
## OUTPUT
<img width="537" height="125" alt="image" src="https://github.com/user-attachments/assets/19ace75e-7d4b-4c8e-a5c2-aec5a94e6dcc" />




sed -n -e '/tom/,/Joe/p' file23
## OUTPUT
<img width="527" height="103" alt="image" src="https://github.com/user-attachments/assets/ffb06054-f1aa-4458-994a-d9d9b4d8371f" />



seq 10 
## OUTPUT
<img width="533" height="295" alt="image" src="https://github.com/user-attachments/assets/f50b8ffc-9d08-47b3-8f14-126e2e42bee3" />



seq 10 | sed -n '4,6p'
## OUTPUT
<img width="552" height="111" alt="image" src="https://github.com/user-attachments/assets/6764fe90-705b-4596-83cc-6a2e9653d2b5" />



seq 10 | sed -n '2,~4p'
## OUTPUT
<img width="530" height="125" alt="image" src="https://github.com/user-attachments/assets/c571de12-af4c-42de-811b-9f9a78ec2962" />



seq 3 | sed '2a hello'
## OUTPUT
<img width="519" height="154" alt="image" src="https://github.com/user-attachments/assets/c32ca07b-1087-487f-aaac-0ce56aa967f4" />



seq 2 | sed '2i hello'
## OUTPUT
<img width="528" height="124" alt="image" src="https://github.com/user-attachments/assets/ec6aff8f-8987-4cfa-aa3f-37a2136a6274" />


seq 10 | sed '2,9c hello'
## OUTPUT
<img width="587" height="129" alt="image" src="https://github.com/user-attachments/assets/621384ae-6795-4f92-bfba-d9a3fcc6ea60" />


sed -n '2,4{s/^/$/;p}' file23
## OUTPUT
<img width="524" height="125" alt="image" src="https://github.com/user-attachments/assets/eacd5a2e-3c82-4238-921d-e8f5e844b53c" />



sed -n '2,4{s/$/*/;p}' file23
<img width="532" height="132" alt="image" src="https://github.com/user-attachments/assets/00127c98-0ab7-409b-9a32-50a1bbd6f9ce" />


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
<img width="598" height="146" alt="image" src="https://github.com/user-attachments/assets/a5391da5-8013-48b2-8e3c-df1c029bff40" />


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
<img width="572" height="157" alt="image" src="https://github.com/user-attachments/assets/c1b8666a-1f93-49a7-866f-766a5c9fa006" />



#Using tr command

cat file23 | tr [:lower:] [:upper:]
 ## OUTPUT
<img width="555" height="274" alt="image" src="https://github.com/user-attachments/assets/25b679e9-44b7-464a-a45a-d1c2ffbb988d" />

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
<img width="521" height="135" alt="image" src="https://github.com/user-attachments/assets/dc95dd9d-8e9e-47c4-a36e-85a4343b12fb" />


 
cat urllist.txt | tr -d ' ' | tr -s '.'
## OUTPUT
<img width="544" height="121" alt="image" src="https://github.com/user-attachments/assets/f388b4fa-058b-481d-92e6-dd9486e64cf1" />



#Backup commands
tar -cvf backup.tar *
## OUTPUT
<img width="798" height="568" alt="image" src="https://github.com/user-attachments/assets/42b7696e-1b7e-43b1-ab7e-63269a01d0b1" />


mkdir backupdir
 
mv backup.tar backupdir

cd backupdir
 
tar -tvf backup.tar
## OUTPUT
<img width="793" height="605" alt="image" src="https://github.com/user-attachments/assets/1678bb76-6364-4126-955a-e3e019459b46" />


tar -xvf backup.tar
## OUTPUT
<img width="784" height="565" alt="image" src="https://github.com/user-attachments/assets/12200b14-87b6-46f9-9d18-ac6da518efd1" />

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
<img width="419" height="125" alt="image" src="https://github.com/user-attachments/assets/1138a50e-9f80-45ae-91c9-abe2fd673cdb" />


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
<img width="548" height="72" alt="image" src="https://github.com/user-attachments/assets/6704505f-e3b2-41e2-986e-bd6262ca6b6f" />

echo $?
## OUTPUT 
./one
bash: ./one: Permission denied
 
echo $?
## OUTPUT 
 <img width="423" height="76" alt="image" src="https://github.com/user-attachments/assets/d4a53c44-c908-4c55-b9de-fbf5f64f3f38" />

abcd
 
echo $?
 ## OUTPUT
 <img width="423" height="76" alt="image" src="https://github.com/user-attachments/assets/d4a53c44-c908-4c55-b9de-fbf5f64f3f38" />

 
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
<img width="404" height="296" alt="image" src="https://github.com/user-attachments/assets/684c224b-50ad-4bfb-b8c3-71b326068ebf" />



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
<img width="462" height="71" alt="image" src="https://github.com/user-attachments/assets/c9a0fb37-fe87-4587-826f-c06140cb9430" />

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
<img width="539" height="502" alt="image" src="https://github.com/user-attachments/assets/1b3b646a-5cb1-40fb-b67b-c713276c05c0" />



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
<img width="611" height="397" alt="image" src="https://github.com/user-attachments/assets/da6afb47-e77b-45fd-942b-0b41ccb822dd" />


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

<img width="602" height="497" alt="image" src="https://github.com/user-attachments/assets/264de70f-c76a-42dd-ae5b-ec17901a051a" />

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
<img width="485" height="65" alt="Screenshot 2026-01-29 230751" src="https://github.com/user-attachments/assets/c6be5203-16a7-4284-a859-594fa8140825" />


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
<img width="510" height="65" alt="Screenshot 2026-01-29 230821" src="https://github.com/user-attachments/assets/75d8b021-3cdf-4109-9777-894d6b2a4120" />

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
<img width="503" height="72" alt="Screenshot 2026-01-29 231004" src="https://github.com/user-attachments/assets/471db570-923c-41f4-a8c3-7d86d6955b9f" />

 
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

 <img width="494" height="232" alt="Screenshot 2026-01-29 231045" src="https://github.com/user-attachments/assets/639bfd2f-a015-4d79-832c-640a3e2a41e5" />

 
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
 <img width="516" height="133" alt="Screenshot 2026-01-29 231208" src="https://github.com/user-attachments/assets/b03b3e1e-9dd4-47c1-b528-560e2164d6d7" />

 
 
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
 <img width="510" height="179" alt="Screenshot 2026-01-29 231249" src="https://github.com/user-attachments/assets/ca3e3c4b-f685-4a46-ac4d-98bcf16e8248" />

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
 <img width="490" height="121" alt="Screenshot 2026-01-29 231333" src="https://github.com/user-attachments/assets/03ec9560-ebf1-4902-ad52-e12da03ce1cb" />

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
<img width="531" height="161" alt="Screenshot 2026-01-29 231424" src="https://github.com/user-attachments/assets/30e3e452-65de-4c2b-895e-20923ac1ef6e" />

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
<img width="528" height="273" alt="Screenshot 2026-01-29 231501" src="https://github.com/user-attachments/assets/f42fc582-e4b6-4cef-9978-595c994efc2c" />


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
<img width="491" height="141" alt="Screenshot 2026-01-29 231544" src="https://github.com/user-attachments/assets/34f91df6-1bdc-4b02-b271-2d081371317a" />

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
<img width="503" height="132" alt="Screenshot 2026-01-29 231618" src="https://github.com/user-attachments/assets/f397eba5-3d10-40d1-a8fe-e43968a76319" />

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
<img width="536" height="268" alt="Screenshot 2026-01-29 231652" src="https://github.com/user-attachments/assets/0d73791e-a611-495b-a822-1facb51133fb" />

 
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

<img width="475" height="101" alt="Screenshot 2026-01-29 231714" src="https://github.com/user-attachments/assets/7ff31a90-f5e8-4244-b9c1-d523d95c4ed0" />

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

 <img width="491" height="136" alt="Screenshot 2026-01-29 231757" src="https://github.com/user-attachments/assets/e9d4487e-1847-424c-840d-a3b62edf34df" />

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




 cat exread1.sh
```bash
#!/bin/bash
# testing the read command
read -p "Enter your name: " name
echo "Hello $name, welcome to my program. “
``` 
$ chmod 755 exread1.sh



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

<img width="475" height="55" alt="Screenshot 2026-01-29 232315" src="https://github.com/user-attachments/assets/ed9ac30c-a577-44af-8c9a-2d6af037dba2" />

 
 ./funcex.sh 1 2


 <img width="442" height="47" alt="Screenshot 2026-01-29 232253" src="https://github.com/user-attachments/assets/5a9e001a-cf97-4cd2-895c-df870f608534" />

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

 <img width="462" height="99" alt="Screenshot 2026-01-29 232228" src="https://github.com/user-attachments/assets/eb4b5a05-c611-4c40-8cef-e92031b9cd3d" />

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

 <img width="507" height="100" alt="Screenshot 2026-01-29 232202" src="https://github.com/user-attachments/assets/af83ad51-de98-445b-8469-20d800c11ab1" />

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

 <img width="509" height="311" alt="Screenshot 2026-01-29 232129" src="https://github.com/user-attachments/assets/b5cb78fd-38e6-44b7-b2cc-ac4fc00c6b60" />

 
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

 <img width="473" height="275" alt="Screenshot 2026-01-29 232048" src="https://github.com/user-attachments/assets/3bf197fd-57ec-42a1-bd6c-585ddec8314a" />

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

<img width="523" height="290" alt="Screenshot 2026-01-29 232021" src="https://github.com/user-attachments/assets/f6f02550-9740-4e1a-9322-0b525fd3817d" />


# RESULT:

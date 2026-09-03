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
<img width="1411" height="375" alt="Screenshot 2026-09-02 221620" src="https://github.com/user-attachments/assets/aa828365-8054-4f85-b4db-4d7c4dd0c92f" />


cat < file2
## OUTPUT
<img width="1117" height="326" alt="image" src="https://github.com/user-attachments/assets/b78eb843-fcb8-4bef-9ad0-fc55669c2dae" />




# Comparing Files
cmp file1 file2
## OUTPUT
<img width="1612" height="187" alt="image" src="https://github.com/user-attachments/assets/6f63700e-7f40-4cbe-8d2e-f076de9df4d2" />



comm file1 file2
 ## OUTPUT
<img width="1502" height="512" alt="image" src="https://github.com/user-attachments/assets/422c71ee-0c02-4559-9328-a1b3b67aac28" />

 
diff file1 file2
## OUTPUT

<img width="868" height="572" alt="image" src="https://github.com/user-attachments/assets/88160439-c224-435d-8e9f-2f4f67cdaf95" />


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

<img width="1612" height="287" alt="image" src="https://github.com/user-attachments/assets/810ae459-c058-4b10-9d5d-58b32c70c564" />


cut -d "|" -f 1 file22
## OUTPUT

<img width="1568" height="386" alt="image" src="https://github.com/user-attachments/assets/12b8e448-5f79-4438-9c47-6934094034c0" />

cut -d "|" -f 2 file22
## OUTPUT

![Alt text](img/img95.png)
cat < newfile 
```
Hello world
hello world
^d

cat > newfile 
Hello world
hello world
```
grep Hello newfile 


## OUTPUT
![Alt text](img/img111.png)


grep hello newfile 
## OUTPUT
![Alt text](img/img116.png)



grep -v hello newfile 
## OUTPUT
![Alt text](img/im122.png)


cat newfile | grep -i "hello"
## OUTPUT
![Alt text](img/img127.png)



cat newfile | grep -i -c "hello"
## OUTPUT
![Alt text](img/img133.png)



grep -R ubuntu /etc
## OUTPUT
![Alt text](img/img139.png)


grep -w -n world newfile   
## OUTPUT
![Alt text](img/IMG144.png)

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
![Alt text](img/img169.png)


egrep -w '(H|h)ello' newfile 
## OUTPUT
![Alt text](img/img174.png)


egrep -w '(H|h)ell[a-z]' newfile 
## OUTPUT
![Alt text](img/img179.png)



egrep '(^hello)' newfile 
## OUTPUT
![Alt text](img/img185.png)


egrep '(world$)' newfile 
## OUTPUT
![Alt text](img/img190.png)


egrep '(World$)' newfile 
## OUTPUT
![Alt text](img/img195.png)

egrep '((W|w)orld$)' newfile 
## OUTPUT
![Alt text](img/img199.png)



egrep '[1-9]' newfile 
## OUTPUT
![Alt text](img/img204.png)


egrep 'Linux.*world' newfile 
## OUTPUT
![Alt text](img/img209.png)

egrep 'Linux.*World' newfile 
## OUTPUT
![Alt text](img/img213.png)

egrep l{2} newfile
## OUTPUT
![Alt text](img/img217.png)


egrep 's{1,2}' newfile
## OUTPUT 
![Alt text](img/img222.png)

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
![Alt text](img/img241.png)



sed -n -e '$p' file23
## OUTPUT
![Alt text](img/img247.png)


sed  -e 's/Ram/Sita/' file23
## OUTPUT
![Alt text](img/img252.png)


sed  -e '2s/Ram/Sita/' file23
## OUTPUT
![Alt text](img/img257.png)


sed  '/tom/s/5000/6000/' file23
## OUTPUT
![Alt text](img/img262.png)


sed -n -e '1,5p' file23
## OUTPUT
![Alt text](img/img267.png)


sed -n -e '2,/Joe/p' file23
## OUTPUT
![Alt text](img/img272.png)



sed -n -e '/tom/,/Joe/p' file23
## OUTPUT
![Alt text](img/img278.png)


seq 10 
## OUTPUT
![Alt text](img/img283.png)


seq 10 | sed -n '4,6p'
## OUTPUT

![Alt text](img/img288.png)

seq 10 | sed -n '2,~4p'
## OUTPUT
![Alt text](img/img293.png)


seq 3 | sed '2a hello'
## OUTPUT
![Alt text](img/img298.png)


seq 2 | sed '2i hello'
## OUTPUT
![Alt text](img/img303.png)

seq 10 | sed '2,9c hello'
## OUTPUT
![Alt text](img/img307.png)

sed -n '2,4{s/^/$/;p}' file23
## OUTPUT
![Alt text](img/img311.png)


sed -n '2,4{s/$/*/;p}' file23
## OUTPUT
![Alt text](img/img316.png)


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
![Alt text](img/img330.png)

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
![Alt text](img/img343.png)


#Using tr command

cat file23 | tr [:lower:] [:upper:]
 ## OUTPUT
![Alt text](img/img350.png)

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
![Alt text](img/img367.png)

 
cat urllist.txt | tr -d ' ' | tr -s '.'
## OUTPUT
![Alt text](img/img372.png)


#Backup commands
tar -cvf backup.tar *
## OUTPUT
![Alt text](img/img378(1).png)

![Alt text](img/img378(2).png)
mkdir backupdir
 
mv backup.tar backupdir

cd backupdir
 
tar -tvf backup.tar
## OUTPUT
![Alt text](img/img389.png)

tar -xvf backup.tar
## OUTPUT
![Alt text](img/img393-1.png)

![Alt text](img/img393-2.png)
gzip backup.tar

ls .gz
## OUTPUT
 ![Alt text](img/img400.png)

gunzip backup.tar.gz
## OUTPUT
![Alt text](img/img404.png)
 
# Shell Script
```
echo '#!/bin/sh' > my-script.sh
echo 'echo Hello World‘; exit 0 >> my-script.sh
```
chmod 755 my-script.sh
./my-script.sh
## OUTPUT
![Alt text](img/img414.png)
 
cat << stop > herecheck.txt
```
hello in this world
i cant stop
for this non stop movement
stop
```

cat herecheck.txt
## OUTPUT
![Alt text](img/img426.png)

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
![Alt text](img/img463.png)
 
ls file1
## OUTPUT
![Alt text](img/img468.png)

echo $?
## OUTPUT
 ![Alt text](img/img472.png)
./one
bash: ./one: Permission denied
 
echo $?
## OUTPUT 
 ![Alt text](img/img478.png)
abcd
 
echo $?
 ## OUTPUT
![Alt text](img/img483.png)

 
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
![Alt text](img/img504.png)


chmod 755 strcomp.shdd
 
./strcomp.sh 
## OUTPUT
![Alt text](img/img522.png)

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

![Alt text](img/img549.png)
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
![Alt text](img/img595.png)


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

![Alt text](img/img639.png)

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

![Alt text](img/img688.png)

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
![Alt text](img/img724.png)

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
![Alt text](img/img740.png)

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
![Alt text](img/img760.png)

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
 ![Alt text](img/img777.png)
 
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
```
$ chmod 755 untiltest.sh
```

 ## OUTPUT

 ![Alt text](img/img793.png)
 
cat forin1.sh 
```bash
\#!/bin/bash
\#basic for command
for test in Alabama Alaska Arizona Arkansas California Colorado
do
echo The next state is $test
done
 ```
 ## OUTPUT
![Alt text](img/img807.png)
 
$ chmod 755 forin1.sh
 

cat forin2.sh 
```bash
#!/bin/bash
# another example of how not to use the for command
for test in I don't know if this'll work
do
echo "word:$test"
done
```

$ chmod 755 forin2.sh
```
 
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
![Alt text](img/img839.png)
 
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
$ chmod 755 forin3.sh

## OUTPUT
![Alt text](img/img863.png)

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
![Alt text](img/img886.png)

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
![Alt text](img/img902.png)
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
![Alt text](img/img915.png)
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
![Alt text](img/img933.png)
 
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
![Alt text](img/img949.png)
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
![Alt text](img/img976.png) 

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
![Alt text](img/img991.png)

 cat exread1.sh
```bash
#!/bin/bash
# testing the read command
read -p "Enter your name: " name
echo "Hello $name, welcome to my program. “
```
$ chmod 755 exread1.sh 
```
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
## OUTPUT!
[Alt text](img/img1024.png)
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
```
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
![Alt text](img/img1069.png)

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
![Alt text](img/img1104.png)## OUTPUT 
 
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
![Alt text](img/img1130.png)

# RESULT:
The Commands are executed successfully.

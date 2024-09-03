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
![image](https://github.com/user-attachments/assets/b8d3904d-370e-4f89-8635-9ef0f6cc6e92)

cat < file2
## OUTPUT
![image](https://github.com/user-attachments/assets/53f30e35-761f-4f94-ba34-8f4b4672c53e)

# Comparing Files
cmp file1 file2
## OUTPUT
![image](https://github.com/user-attachments/assets/dcfc779c-a72d-4897-9afd-afb17d73a2f4)

comm file1 file2
 ## OUTPUT
![image](https://github.com/user-attachments/assets/c0c13c99-b689-4aaf-86a8-d3f52eb0020a)

 
diff file1 file2
## OUTPUT
![image](https://github.com/user-attachments/assets/14801fb7-23b8-4375-8973-a73158474050)


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

![image](https://github.com/user-attachments/assets/d0d8de83-90a1-487c-b8ed-52c6a16825a4)

cut -d "|" -f 1 file22
## OUTPUT
![image](https://github.com/user-attachments/assets/7238bc7b-9031-4af7-b313-0c65c4ea1088)


cut -d "|" -f 2 file22
## OUTPUT
![image](https://github.com/user-attachments/assets/4e4d59bb-2105-483e-a1a4-c3e18b8f6ceb)


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

![image](https://github.com/user-attachments/assets/cb638c9d-4334-42eb-85eb-edacb7ee86b8)


grep hello newfile 
## OUTPUT


![image](https://github.com/user-attachments/assets/7253ffc9-9448-43fa-8b89-e6442337001a)


grep -v hello newfile 
## OUTPUT
![image](https://github.com/user-attachments/assets/776c4241-6bae-4daa-bcaf-d0dffe633816)



cat newfile | grep -i "hello"
## OUTPUT

![image](https://github.com/user-attachments/assets/1413eec1-482c-4cdc-812f-2b42615a98b7)



cat newfile | grep -i -c "hello"
## OUTPUT

![image](https://github.com/user-attachments/assets/38ccc733-8119-4487-ac53-d5c1eee62695)



grep -R ubuntu /etc
## OUTPUT
![image](https://github.com/user-attachments/assets/b6ce2cff-d36a-4095-982f-3e1a784c687b)



grep -w -n world newfile   
## OUTPUT

![image](https://github.com/user-attachments/assets/82128d60-9674-4de7-a98f-4e105a2926d1)

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

![image](https://github.com/user-attachments/assets/dc4c3b8c-1c45-4db7-a973-8acbfdc31a2f)


egrep -w '(H|h)ello' newfile 
## OUTPUT

![image](https://github.com/user-attachments/assets/d1cbf411-2442-4672-a7b6-c7b7412e6a2b)


egrep -w '(H|h)ell[a-z]' newfile 
## OUTPUT

![image](https://github.com/user-attachments/assets/98cb38a1-a50b-4c07-bbeb-12f7600b3b31)

egrep '(^hello)' newfile 
## OUTPUT
![image](https://github.com/user-attachments/assets/1ef0c757-8edf-4adb-988c-9991e13aeb45)

egrep '(world$)' newfile 
## OUTPUT

![image](https://github.com/user-attachments/assets/23ed3913-f7ce-41ea-b085-a1d08172522c)


egrep '(World$)' newfile 
## OUTPUT
![image](https://github.com/user-attachments/assets/df2a6c1e-223a-4386-af7d-6a24e150045f)


egrep '((W|w)orld$)' newfile 
## OUTPUT
![image](https://github.com/user-attachments/assets/e6ad35d7-13fd-4fdd-b7b2-163b533c8bb6)



egrep '[1-9]' newfile 
## OUTPUT

![image](https://github.com/user-attachments/assets/ac1bc063-f023-4521-a660-fe5863033c15)


egrep 'Linux.*world' newfile 
## OUTPUT
![image](https://github.com/user-attachments/assets/2532f227-0513-4bba-a4a7-2b23e11cebd8)


egrep 'Linux.*World' newfile 
## OUTPUT
![image](https://github.com/user-attachments/assets/a40eeb22-1105-4631-a2cb-dc61bed60169)


egrep l{2} newfile
## OUTPUT
![image](https://github.com/user-attachments/assets/42f9f502-3795-4b3b-8e45-9cecf1aab216)



egrep 's{1,2}' newfile
## OUTPUT 
![image](https://github.com/user-attachments/assets/aa09bce3-febf-4dd8-b16b-43194e222a1f)


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
![image](https://github.com/user-attachments/assets/2b08d3a8-9c28-4984-8519-a8e2cec67460)



sed -n -e '$p' file23
## OUTPUT
![image](https://github.com/user-attachments/assets/c394c85f-1df7-433e-93fb-a08ac574dea1)



sed  -e 's/Ram/Sita/' file23
## OUTPUT

![image](https://github.com/user-attachments/assets/b01ede05-1bc7-4d5e-abef-2b8fe9d8912d)


sed  -e '2s/Ram/Sita/' file23
## OUTPUT

![image](https://github.com/user-attachments/assets/e427e82a-912f-4460-87e4-8c676d63dbea)


sed  '/tom/s/5000/6000/' file23
## OUTPUT

![image](https://github.com/user-attachments/assets/bd01101e-07d5-4669-9209-e0e433f3186b)


sed -n -e '1,5p' file23
## OUTPUT

![image](https://github.com/user-attachments/assets/31e92d1e-a13f-4b91-bf58-2cbb042611ab)


sed -n -e '2,/Joe/p' file23
## OUTPUT
![image](https://github.com/user-attachments/assets/c421352f-df2e-4ea2-b80e-6901f336d8ad)




sed -n -e '/tom/,/Joe/p' file23
## OUTPUT

![image](https://github.com/user-attachments/assets/dc8aec85-a279-4751-9b4f-eb3325b54045)


seq 10 
## OUTPUT

![image](https://github.com/user-attachments/assets/f4792ecc-8c4a-43f1-be40-aaa6f84cb33d)


seq 10 | sed -n '4,6p'
## OUTPUT
![image](https://github.com/user-attachments/assets/5233499a-d597-4010-98f4-b304ac3f5423)



seq 10 | sed -n '2,~4p'
## OUTPUT
![image](https://github.com/user-attachments/assets/d8dd4b4c-a0a0-47ba-b9d5-638afeb739c4)



seq 3 | sed '2a hello'
## OUTPUT
![image](https://github.com/user-attachments/assets/f3ec91a1-ed26-40e5-b0a5-ec0838fb1941)



seq 2 | sed '2i hello'
## OUTPUT
![image](https://github.com/user-attachments/assets/91a50771-c728-4363-b5b6-d532eac18af3)

seq 10 | sed '2,9c hello'
## OUTPUT
![image](https://github.com/user-attachments/assets/512560cb-b20b-4028-9213-1bfa209cd2ac)


sed -n '2,4{s/^/$/;p}' file23
## OUTPUT
![image](https://github.com/user-attachments/assets/ed2f68dd-2b60-4293-91db-f35d0861fee8)



sed -n '2,4{s/$/*/;p}' file23
![image](https://github.com/user-attachments/assets/f542767b-48be-4b44-b9ba-59281635442e)


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
![image](https://github.com/user-attachments/assets/24aa20b8-bc74-4722-924a-8c2a586ce5a2)


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

![image](https://github.com/user-attachments/assets/d86ef964-2cfa-4118-ba6b-f53efb885f95)


#Using tr command

cat file23 | tr [:lower:] [:upper:]
 ## OUTPUT
![image](https://github.com/user-attachments/assets/20548751-e690-4362-a4ae-854439e02c68)

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
![image](https://github.com/user-attachments/assets/7e73b375-16d0-4367-838d-3768f5a433cb)


 
cat urllist.txt | tr -d ' ' | tr -s '.'
## OUTPUT

![image](https://github.com/user-attachments/assets/b500d60d-6f04-4368-91c7-69caf56bbc57)


#Backup commands
tar -cvf backup.tar *
## OUTPUT

![image](https://github.com/user-attachments/assets/bed872c0-fee3-40ac-92f7-cea21771bce9)

mkdir backupdir
 
mv backup.tar backupdir
 
tar -tvf backup.tar
## OUTPUT
![image](https://github.com/user-attachments/assets/95a65b65-d375-4b8a-94d5-b64a3db60d31)

tar -xvf backup.tar
## OUTPUT
![image](https://github.com/user-attachments/assets/48d51b14-b943-4439-8d48-02c869196364)

gzip backup.tar

ls .gz
## OUTPUT
 ![image](https://github.com/user-attachments/assets/e34a0236-4e18-4042-9cae-8e0078ed4ae2)

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
![image](https://github.com/user-attachments/assets/33544df3-9f99-49f6-9a8b-09bef54777cd)


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
![image](https://github.com/user-attachments/assets/a91195d5-4fad-4f7d-9c50-41c46561cfc7)

 
ls file1
## OUTPUT
![image](https://github.com/user-attachments/assets/e9ed8e76-e12a-4b8a-a613-f1d10c631853)

echo $?
## OUTPUT 
![image](https://github.com/user-attachments/assets/d5b343c6-93a1-4c74-949a-371e8ec62821)

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

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
![image](https://github.com/user-attachments/assets/76aa70dc-7c1f-4af5-8e5b-a7192dfa4ae5)


cat < file2
## OUTPUT
![image](https://github.com/user-attachments/assets/c7443401-0e1f-4985-902c-ae0209cc1a56)


# Comparing Files
cmp file1 file2
## OUTPUT
![image](https://github.com/user-attachments/assets/bb5e682b-8616-424e-b794-f8c7e1ccf72c)

comm file1 file2
 ## OUTPUT
![image](https://github.com/user-attachments/assets/8ecc971b-1c8f-4693-9b04-5c2b707248f1)

 
diff file1 file2
## OUTPUT
![image](https://github.com/user-attachments/assets/b255796c-f333-4bad-8400-9a31d56b591c)


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
![image](https://github.com/user-attachments/assets/c266e7d4-448a-4d69-a1d3-c6390787f966)

cut -d "|" -f 1 file22
## OUTPUT
![image](https://github.com/user-attachments/assets/996bef5c-a827-46d7-a085-8a07a171d0db)

cut -d "|" -f 2 file22
## OUTPUT
![image](https://github.com/user-attachments/assets/7a4c8fde-a4ff-41d5-8c50-6c0b0d80c00a)

cat < newfile 
```
Hello world
hello world
^d
````
cat > newfile 
Hello world
hello world


grep hello newfile 
## OUTPUT
![image](https://github.com/user-attachments/assets/95dd46de-160c-462f-8b6c-7169eeb421e6)

grep -v hello newfile 
## OUTPUT
![image](https://github.com/user-attachments/assets/8187d265-ae57-4c13-92b4-a67bf841fbf8)

cat newfile | grep -i "hello"
## OUTPUT
![image](https://github.com/user-attachments/assets/68e56b9f-5c10-4f0f-b2aa-8881334435dd)


cat newfile | grep -i -c "hello"
## OUTPUT
![image](https://github.com/user-attachments/assets/ee7070c4-fc00-454d-a1b4-bf0a7c6b0dde)

grep -R ubuntu /etc
## OUTPUT
![image](https://github.com/user-attachments/assets/b15cf6ca-16e3-453f-8f3d-2fee8cd74fbc)

grep -w -n world newfile   
## OUTPUT
![image](https://github.com/user-attachments/assets/b80a20cc-0340-4168-b035-71223b57e5c0)

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
![Screenshot from 2024-10-22 18-02-13](https://github.com/user-attachments/assets/4bf14ca8-aa37-47d3-82b4-fb1b6e6e175f)

egrep -w '(H|h)ello' newfile 
## OUTPUT
![image](https://github.com/user-attachments/assets/8310facb-ef7d-451e-b4fa-31341b6c8e4e)

egrep -w '(H|h)ell[a-z]' newfile 
## OUTPUT
![image](https://github.com/user-attachments/assets/0ef467fb-a58a-4805-9faa-2a900bed5e18)

egrep '(^hello)' newfile 
## OUTPUT
![image](https://github.com/user-attachments/assets/46ae79e7-9a35-45c4-b411-ead1f1b164d3)

egrep '(world$)' newfile 
## OUTPUT
![image](https://github.com/user-attachments/assets/651df66b-8e66-461d-b9d5-53c8aeea34b1)

egrep '(World$)' newfile 
## OUTPUT
![image](https://github.com/user-attachments/assets/eca0ab77-8dec-4fa5-a88c-cbffcdee8d5f)

egrep '((W|w)orld$)' newfile 
## OUTPUT
![image](https://github.com/user-attachments/assets/6de3673c-5bcd-45d9-82ad-7320f6a29e73)

egrep '[1-9]' newfile 
## OUTPUT
![image](https://github.com/user-attachments/assets/45c5a54e-c632-4883-8930-75eb285d061e)

egrep 'Linux.*world' newfile 
## OUTPUT
![image](https://github.com/user-attachments/assets/145dca3d-9b18-4c2a-a7bb-2d00f7b960a6)

egrep 'Linux.*World' newfile 
## OUTPUT
![image](https://github.com/user-attachments/assets/72e3ca7b-0ad5-4c71-9499-462e65433015)

egrep l{2} newfile
## OUTPUT
![image](https://github.com/user-attachments/assets/8cf63990-d15d-477d-ace4-7041f7ea6633)

egrep 's{1,2}' newfile
## OUTPUT 
![image](https://github.com/user-attachments/assets/0b5e6d55-f257-40d0-b466-316890686970)


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
![image](https://github.com/user-attachments/assets/9ab5d5f4-c84e-41eb-977a-da59a69fdba8)

sed -n -e '$p' file23
## OUTPUT
![image](https://github.com/user-attachments/assets/fe3b49a2-df80-4afd-8173-ed68818a9f17)

sed  -e 's/Ram/Sita/' file23
## OUTPUT
![image](https://github.com/user-attachments/assets/d322fad5-2599-4aaa-8a9d-a2c54985f375)

sed  -e '2s/Ram/Sita/' file23
## OUTPUT
![image](https://github.com/user-attachments/assets/b3c89cee-adc7-4016-a161-36ea6d7e8d86)

sed  '/tom/s/5000/6000/' file23
## OUTPUT
![image](https://github.com/user-attachments/assets/fae7f1ae-0d50-4ff5-9156-2743a6b1cfd1)

sed -n -e '1,5p' file23
## OUTPUT
![image](https://github.com/user-attachments/assets/f20f1835-5913-4336-b804-072fd738160f)

sed -n -e '2,/Joe/p' file23
## OUTPUT
![image](https://github.com/user-attachments/assets/0b0eb44a-ac71-445c-bb6f-76a3ad637acd)

sed -n -e '/tom/,/Joe/p' file23
## OUTPUT
![image](https://github.com/user-attachments/assets/8254bb56-f56d-458c-8dfe-4eb6c4e5ca5b)

seq 10 
## OUTPUT
![image](https://github.com/user-attachments/assets/3a0b539d-183a-43d6-8ab0-ed6878cf06ac)

seq 10 | sed -n '4,6p'
## OUTPUT
![image](https://github.com/user-attachments/assets/28226e7c-acab-44e0-beef-d332256d48ba)

seq 10 | sed -n '2,~4p'
## OUTPUT
![image](https://github.com/user-attachments/assets/bc5681ae-1d59-45e0-9896-6320ecbd5fe6)

seq 3 | sed '2a hello'
## OUTPUT
![image](https://github.com/user-attachments/assets/dd05e004-abad-4211-a041-87394f848201)

seq 2 | sed '2i hello'
## OUTPUT
![image](https://github.com/user-attachments/assets/2ec85362-37d9-41c6-9d25-5b8a3c0c16f4)

seq 10 | sed '2,9c hello'
## OUTPUT
![image](https://github.com/user-attachments/assets/90903a90-28bf-445f-8d8e-7fa360198b05)

sed -n '2,4{s/^/$/;p}' file23
## OUTPUT
![image](https://github.com/user-attachments/assets/9a9f1155-eaab-4807-87eb-db981e366ba1)

sed -n '2,4{s/$/*/;p}' file23
## OUTPUT
![image](https://github.com/user-attachments/assets/bc77fde6-4ff7-4ebc-b35f-4ed773ceb067)

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
![image](https://github.com/user-attachments/assets/f61aefd8-226a-4997-b48c-8790f502c10f)

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
![image](https://github.com/user-attachments/assets/fbe7ad72-2564-48ae-9108-33f9e7abca22)

#Using tr command

cat file23 | tr [:lower:] [:upper:]
 ## OUTPUT
![image](https://github.com/user-attachments/assets/a1360f1e-e72d-4785-85ff-a4f4132934a1)

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
![image](https://github.com/user-attachments/assets/45272d05-ee80-476c-aefa-ed2d2f595f66)

cat urllist.txt | tr -d ' ' | tr -s '.'
## OUTPUT
![image](https://github.com/user-attachments/assets/37a41e44-9b8d-4751-a96d-a72daaf09461)

#Backup commands
tar -cvf backup.tar *
## OUTPUT
![image](https://github.com/user-attachments/assets/ccdfaa84-a38a-46fa-9469-2913ede19e9f)


mkdir backupdir
 
mv backup.tar backupdir
 
tar -tvf backup.tar
## OUTPUT
![image](https://github.com/user-attachments/assets/db724569-f9bb-4836-9ffb-24812691b30b)


tar -xvf backup.tar
## OUTPUT
![image](https://github.com/user-attachments/assets/3bf372ee-c643-4ada-aa59-326b59d46fb4)

gzip backup.tar

ls .gz
## OUTPUT
![image](https://github.com/user-attachments/assets/d0c455b5-9411-4c4f-a2b2-910a8888ced4)

gunzip backup.tar.gz
## OUTPUT
![image](https://github.com/user-attachments/assets/7125ad68-4e1d-4515-ba8d-49fcabc39a17)

 
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
![image](https://github.com/user-attachments/assets/0af74ce4-3c7e-49d9-8aca-4de3f1fd7e67)


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
![image](https://github.com/user-attachments/assets/bb508d10-1be3-4ef6-bd38-9a20723c42cb)

 
ls file1
## OUTPUT
![image](https://github.com/user-attachments/assets/7e27c1ba-2735-4899-9018-84b71991e127)


./one
bash: ./one: Permission denied
 
echo $?
## OUTPUT 
![image](https://github.com/user-attachments/assets/912be48a-bce1-4a24-9b21-0c3b79dfca7a)
 

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
![image](https://github.com/user-attachments/assets/797d2fd2-6d4b-4590-96d7-3a6ca180fdce)

chmod 755 strcomp.sh
 
./strcomp.sh 
## OUTPUT
![image](https://github.com/user-attachments/assets/e0ee3531-f2c9-4eaa-b0e9-6add911a576d)


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
![image](https://github.com/user-attachments/assets/f84a4ae6-7298-434f-bb68-faac42b3d4bb)

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
![image](https://github.com/user-attachments/assets/96130350-80c8-42db-825e-33709da7b1b5)



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
![image](https://github.com/user-attachments/assets/d426122c-03e7-44e4-8a98-abc6ee9943e0)

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
![image](https://github.com/user-attachments/assets/2386ec1c-9d44-4a47-9a1c-f11092ef79fa)

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
![image](https://github.com/user-attachments/assets/75c6caa1-bae0-4652-912d-f593d795f445)


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
![image](https://github.com/user-attachments/assets/920e2ab1-caf1-408a-b86f-8e107344a7eb)

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
![image](https://github.com/user-attachments/assets/55d1cbd8-2215-4fe6-b354-a9d8af32b6f3)

 
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
![image](https://github.com/user-attachments/assets/d9aa66d5-f161-45f0-9222-b92aae1f4819)

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
![image](https://github.com/user-attachments/assets/0895efea-874d-4091-9780-bc52d27d5585)

 
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
![image](https://github.com/user-attachments/assets/cf7ca4db-4178-49aa-91b8-5a470e4c7bb5)

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
![image](https://github.com/user-attachments/assets/20b7790c-043f-439e-abcb-bbd97a75b9cf)

 
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
![image](https://github.com/user-attachments/assets/262aed49-dea9-48a1-b6c0-5b19a6618ce6)

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
![image](https://github.com/user-attachments/assets/87567908-f6a9-44c7-b6e7-23be128649f4)

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
![image](https://github.com/user-attachments/assets/d21ea1f5-a72d-4c33-bd3e-4cd5c2310b36)


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
![image](https://github.com/user-attachments/assets/60def5d0-f5ef-4b50-92bd-be4b8bc782ff)

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
![image](https://github.com/user-attachments/assets/ad7c6a5c-4e6c-4fc9-b013-31bfa64cc60e)

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
![image](https://github.com/user-attachments/assets/1ca58dd8-3c46-4f0b-b4a6-92138d2e7f74)

 
cat > forbreak.sh 
```
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
echo "The for loop is completed"
```
```
$ chmod 755 forbreak.sh
$ ./forbreak.sh
```
## OUTPUT
![image](https://github.com/user-attachments/assets/f4716dec-9330-41c1-9aca-828599c946b0)
```
cat > forcontinue.sh 
```
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
echo "The for loop is completed"
```
```
$ chmod 755 forcontinue.sh
$ ./forcontinue.sh 
```
## OUTPUT
![image](https://github.com/user-attachments/assets/57ae9915-72d9-4fe2-8ef0-0d15506e0d02)
```
cat > exread.sh 
```
```bash
#!/bin/bash
# testing the read command
echo -n "Enter your name: "
read name
echo "Hello $name, welcome to my program. "
```
```
$ chmod 755 exread.sh 
$ ./exread.sh 
```
## OUTPUT
![image](https://github.com/user-attachments/assets/4d729386-6a63-40f6-9fc7-fbfdaf60717b)
```
cat > exread1.sh
```
```bash
#!/bin/bash
# testing the read command
read -p "Enter your name: " name
echo "Hello $name, welcome to my program. "
``` 
```
$ chmod 755 exread1.sh 
$ ./exread1.sh
```
## OUTPUT
![image](https://github.com/user-attachments/assets/3329b737-dfee-429d-a067-3e4fa33dd33a)

```
cat > funcex.sh
```
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
```
./funcex.sh 
./funcex.sh 1 2
```
## OUTPUT
![image](https://github.com/user-attachments/assets/eb927356-ffa7-4e0e-a003-556577e88180)

``` 
cat > argshift.sh
```
```bash
#!/bin/bash 
 while (( "$#" )); do 
  echo $1 
  shift 
done
```
```
$ chmod 777 argshift.sh
$ ./argshift.sh 1 2 3
```
## OUTPUT
![image](https://github.com/user-attachments/assets/f973ccb2-81b8-4099-a185-bd61073dc6ce)

```
cat > argshift1.sh
```
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
```
$ chmod 777 argshift1.sh
$ ./argshift1.sh 1 2 3
```
## OUTPUT
![image](https://github.com/user-attachments/assets/55e38f66-c0bc-41b6-b574-3a46eebc1a96)
```
cat > argshift.sh
```
```bash
#!/bin/bash 
set -x 
while (( "$#" )); do 
  echo $1 
  shift 
done
set +x
```
```
chmod 777 argshift.sh
./argshift.sh 1 2 3
```
## OUTPUT
![image](https://github.com/user-attachments/assets/a6e3329b-8551-48ef-a2bd-c5073b30f675)
```
cat > nc.awk
```
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
```
cat>data.dat
```
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
```
awk -f nc.awk data.dat
```
## OUTPUT 
![image](https://github.com/user-attachments/assets/380c45bc-5504-4621-91f1-5850c02a4ff5)

```
cat > palindrome.sh
```
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
```
bash palindrome.sh
```
## OUTPUT 
![image](https://github.com/user-attachments/assets/486433e6-bc62-4305-94fd-9e11bd83cc1f)

# RESULT:
The Commands are executed successfully.

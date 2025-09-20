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
```cat > file1```
```
Aarav Mehta
Priya Nair
Rohan Iyer
Kavya Reddy
```
```cat > file2```
```
Emily Carter
Arjun Sharma
Micheal Johnson
Sofia Rossi
Daniel Muller
```
### Display the content of the files

```cat < file1```

## OUTPUT

<img width="910" height="134" alt="1" src="https://github.com/user-attachments/assets/8e21a682-5277-4962-85f8-d97d316dd48b" />

```cat < file2```

## OUTPUT

<img width="910" height="155" alt="1" src="https://github.com/user-attachments/assets/273abe73-52f5-4ee4-84f4-f0b8aab94fa4" />

# Comparing Files

```cmp file1 file2```

## OUTPUT

 <img width="910" height="90" alt="3" src="https://github.com/user-attachments/assets/5778d3bf-d3c3-4cc6-b45d-f284b2b503c7" />

```comm file1 file2```
 ## OUTPUT

 <img width="910" height="282" alt="4" src="https://github.com/user-attachments/assets/6c0c13e9-a367-4df3-9054-fe2380a84441" />

```diff file1 file2```

## OUTPUT

<img width="910" height="272" alt="5" src="https://github.com/user-attachments/assets/789d2434-a72e-45b0-b7b9-b83cae6ef43e" />

## Filters

### Create the following files file11, file22 as follows:

```cat > file11```
```
Hello world
This is my world
This is Siddarth's World
^C
```
```cat > file22```
```
1001 | Haru | 10000 | HR
1002 | Ash |  15000 | Admin
1003 | Sam |  80000 | Developer
^C
```


```cut -c1-3 file11```

## OUTPUT


<img width="722" height="109" alt="6" src="https://github.com/user-attachments/assets/52721426-c5b9-44f7-a7be-c2820eac77c2" />


```cut -d "|" -f 1 file22```

## OUTPUT


<img width="722" height="131" alt="7" src="https://github.com/user-attachments/assets/f01d6cab-344d-48d9-b216-2e9e922ddf4d" />

```cut -d "|" -f 2 file22```

## OUTPUT

<img width="722" height="130" alt="8" src="https://github.com/user-attachments/assets/dece846f-2863-4d88-9e2a-265e81bbe092" />

```cat > newfile ```
```
Hello World
hello world
^C
````
 
```grep Hello newfile ```

## OUTPUT

<img width="641" height="84" alt="10" src="https://github.com/user-attachments/assets/1ec2a62c-61b8-4d2c-84d4-6edf3f167805" />

```grep hello newfile ```

## OUTPUT

<img width="641" height="83" alt="9" src="https://github.com/user-attachments/assets/8eb1961a-1d95-40eb-b140-03e00258ffac" />

```grep -v hello newfile ```

## OUTPUT

<img width="641" height="81" alt="11" src="https://github.com/user-attachments/assets/987dc096-2f02-480e-b16f-2067a0ad635b" />


```cat newfile | grep -i "hello"```

## OUTPUT

<img width="641" height="99" alt="12" src="https://github.com/user-attachments/assets/18b2f430-ce65-4fa8-85e7-a6bf421a68b2" />

```cat newfile | grep -i -c "hello"```

## OUTPUT

<img width="641" height="85" alt="13" src="https://github.com/user-attachments/assets/4bc05d8e-5faa-448c-afd5-79b249159a59" />

```grep -R ubuntu /etc```

## OUTPUT

<img width="1746" height="977" alt="4" src="https://github.com/user-attachments/assets/18f5b59b-68de-482c-8ff9-967422823f5c" />


```grep -w -n world newfile  ``` 

## OUTPUT

<img width="822" height="79" alt="14" src="https://github.com/user-attachments/assets/cba6754d-f7ec-49c3-a92d-0453f2e18018" />


```cat > newfile```

```
Hello World
hello world
Linux is world number 1 OS
Unix is its predecessor
Linux is best in this World
all thanks to Linus Torvalds
^C
 ```
```egrep -w 'Hello|hello' newfile ```

## OUTPUT

<img width="822" height="75" alt="15" src="https://github.com/user-attachments/assets/4aebb69a-239d-4cf3-bbdf-47052b79e6d9" />


```egrep -w '(H|h)ello' newfile``` 

## OUTPUT

<img width="822" height="82" alt="16" src="https://github.com/user-attachments/assets/6eacd541-55ba-41db-a470-1fe67e759db6" />


```egrep -w '(H|h)ell[a-z]' newfile ```

## OUTPUT

<img width="822" height="101" alt="17" src="https://github.com/user-attachments/assets/15f9fe05-dd61-4bf3-a855-6d944b505d5f" />

```egrep '(^hello)' newfile ```

## OUTPUT

<img width="822" height="74" alt="18" src="https://github.com/user-attachments/assets/94c9ed90-56db-47c4-a048-ec4ac14bbd8d" />

```egrep '(world$)' newfile ```

## OUTPUT

<img width="822" height="79" alt="19" src="https://github.com/user-attachments/assets/8e034c1f-b3aa-4b40-9524-4e7b1e631530" />


```egrep '(World$)' newfile ```

## OUTPUT

<img width="856" height="105" alt="20" src="https://github.com/user-attachments/assets/63343021-5e76-449c-999a-ca1b27bb7af4" />

```egrep '((W|w)orld$)' newfile ```

## OUTPUT

<img width="856" height="123" alt="21" src="https://github.com/user-attachments/assets/5ed38267-eae1-4062-aa28-f9be2f8115af" />


```egrep '[1-9]' newfile ```

## OUTPUT


<img width="856" height="79" alt="22" src="https://github.com/user-attachments/assets/4b784607-d92f-4bb1-b104-d5626c5fb0ba" />


```egrep 'Linux.*world' newfile ```

## OUTPUT

<img width="856" height="106" alt="23" src="https://github.com/user-attachments/assets/5a69947a-0ff9-4e46-965a-d00446778dc3" />


```egrep 'Linux.*World' newfile ```

## OUTPUT

<img width="856" height="84" alt="x1" src="https://github.com/user-attachments/assets/97c5a318-d675-475c-b5f7-f8440bc0d3a1" />

```egrep l{2} newfile```

## OUTPUT

<img width="856" height="128" alt="24" src="https://github.com/user-attachments/assets/9bbd9016-d821-44ef-9198-364b5f6ca47f" />


```egrep 's{1,2}' newfile```

## OUTPUT

<img width="856" height="149" alt="25" src="https://github.com/user-attachments/assets/3048660e-9052-436b-8e55-ccad845c2b8d" />


```cat > file23```

```
1001 | Hari   | 10000 | HR
1001 | Hari   | 10000 | HR
1002 | Ash    | 15000 | Admin
1003 | Sam    |  8000 | Dev
1005 | Meera  | 12000 | HR
1004 | Kiran  | 11000 | Admin
1003 | Sam    |  8000 | Dev
1001 | Hari   | 10000 | HR
1006 | Arjun  | 13000 | Dev
1007 | Riya   | 14000 | HR
^C
```



```sed -n -e '3p' file23```

## OUTPUT

<img width="518" height="77" alt="26" src="https://github.com/user-attachments/assets/6920c6a3-33c7-45e3-9154-d09d55aa199c" />




```sed -n -e '$p' file23```

## OUTPUT

<img width="518" height="77" alt="27" src="https://github.com/user-attachments/assets/8d258b93-017d-4977-9645-89f54e361f13" />




```sed -e 's/Hari/Sita/' file23```

## OUTPUT

<img width="518" height="302" alt="28" src="https://github.com/user-attachments/assets/03016171-f0d1-47dd-8fac-665147390040" />




```sed -e '2s/Hari/Sita/' file23```

## OUTPUT

<img width="518" height="305" alt="29" src="https://github.com/user-attachments/assets/449391f3-cfed-47b4-a6a2-7829f006071c" />



```sed '/Ash/s/15000/16000/' file23```

## OUTPUT

<img width="927" height="309" alt="30" src="https://github.com/user-attachments/assets/afa65149-e316-42c5-a22b-6fa2346ba1f9" />





```sed -n -e '1,5p' file23```

## OUTPUT

<img width="927" height="182" alt="31" src="https://github.com/user-attachments/assets/4e4571e7-5334-4900-930a-da20c9cadbd6" />





```sed -n -e '2,/Sam/p' file23```

## OUTPUT


<img width="927" height="134" alt="32" src="https://github.com/user-attachments/assets/6b1347f4-8035-401e-a4b6-84d0d2caaeee" />






```sed -n -e '/Ash/,/Sam/p' file23```

## OUTPUT


<img width="927" height="106" alt="33" src="https://github.com/user-attachments/assets/e1591e13-3179-4f7b-8ccc-5aed5c347f52" />




```seq 10 ```

## OUTPUT

<img width="927" height="301" alt="34" src="https://github.com/user-attachments/assets/9cf08adb-e205-4f1a-8d7b-9bd173640020" />





```seq 10 | sed -n '4,6p'```

## OUTPUT

<img width="871" height="127" alt="35" src="https://github.com/user-attachments/assets/929d5c39-4b3f-44ba-9c8c-e4049c48c31f" />





```seq 10 | sed -n '2,~4p'```

## OUTPUT


<img width="871" height="136" alt="36" src="https://github.com/user-attachments/assets/698a8af6-5813-4f61-ab4b-9bbc13467668" />




```seq 3 | sed '2a hello'```

## OUTPUT


<img width="871" height="159" alt="37" src="https://github.com/user-attachments/assets/d3f83a88-4e8d-40cf-8baf-1a001ee6209e" />





```seq 2 | sed '2i hello'```

## OUTPUT

<img width="871" height="131" alt="38" src="https://github.com/user-attachments/assets/c6b79238-de45-44d7-af90-0473be4a4292" />





```seq 10 | sed '2,9c hello'```

## OUTPUT

<img width="871" height="131" alt="39" src="https://github.com/user-attachments/assets/4d60b6ae-37fc-4936-93c0-ba932d831cef" />






```sed -n '2,4{s/^/$/;p}' file23```

## OUTPUT

<img width="871" height="128" alt="40" src="https://github.com/user-attachments/assets/5490117b-a7b3-4d37-890e-21ae43f6b21a" />





```sed -n '2,4{s/$/*/;p}' file23```

## OUTPUT

<img width="871" height="125" alt="41" src="https://github.com/user-attachments/assets/fb16366e-d118-4969-b9b0-6075f860fc59" />




## Sorting File content

```cat > file21```

```
1001 | Hari   | 10000 | HR
1001 | Hari   | 10000 | HR
1002 | Ash    | 15000 | Admin
1003 | Sam    |  8000 | Dev
1005 | Meera  | 12000 | HR
```

```sort file21```

## OUTPUT

<img width="423" height="182" alt="42" src="https://github.com/user-attachments/assets/bfe42355-d7d7-4743-a620-0c638b069617" />




```cat > file22```

```
1004 | Kiran  | 11000 | Admin
1003 | Sam    |  8000 | Dev
1001 | Hari   | 10000 | HR
1006 | Arjun  | 13000 | Dev
1007 | Riya   | 14000 | HR
```

```sort file22```

## OUTPUT

<img width="423" height="188" alt="43" src="https://github.com/user-attachments/assets/6a06165b-ee77-4384-a81d-5bf27115a1ae" />



```uniq file22```

## OUTPUT


<img width="452" height="180" alt="44" src="https://github.com/user-attachments/assets/4704d895-90ae-4a4a-be37-5f40ee4fd136" />




## Using tr command

```cat file23 | tr [:lower:] [:upper:]```

 ## OUTPUT

 
<img width="452" height="305" alt="45" src="https://github.com/user-attachments/assets/7c94db47-97f4-4c4b-a0ca-6f2fc2139bf4" />



```cat > urllist.txt```
```
www.google.com
www.yahoo.com
www.lms2.cse.saveetha.in
www.saveetha.ac.in

 ```
```cat < urllist.txt```
```
www.google.com
www.yahoo.com
www.lms2.cse.saveetha.in
www.saveetha.ac.in
 ```
```cat urllist.txt | tr -d ' '```

 ## OUTPUT

 
<img width="535" height="151" alt="46" src="https://github.com/user-attachments/assets/c048ad34-0798-4af6-81e0-e5b2e715b0d0" />


 
```cat urllist.txt | tr -d ' ' | tr -s '.'```

## OUTPUT



<img width="623" height="153" alt="47" src="https://github.com/user-attachments/assets/e8f1a63a-bf8d-4820-a006-2ece579d5fc4" />



## Backup commands

```tar -cvf backup.tar *```

## OUTPUT

<img width="535" height="257" alt="48" src="https://github.com/user-attachments/assets/963e185b-aa16-48f8-8021-579aea128dc6" />


```bash

mkdir backupdir
 
mv backup.tar backupdir

cd backupdir
 
tar -tvf backup.tar

```

## OUTPUT



<img width="894" height="406" alt="49" src="https://github.com/user-attachments/assets/9d444eef-9c2f-49a3-916d-ba922c188fb8" />



```tar -xvf backup.tar```

## OUTPUT


<img width="909" height="251" alt="50" src="https://github.com/user-attachments/assets/364def9a-1876-4560-8567-44751026c9f8" />


```bash
gzip backup.tar

ls *.gz
```

## OUTPUT


 <img width="695" height="132" alt="51" src="https://github.com/user-attachments/assets/f1208d63-af7c-403c-9060-9c092eb88ed4" />



```gunzip backup.tar.gz```

## OUTPUT



 <img width="695" height="128" alt="52" src="https://github.com/user-attachments/assets/cb0989f6-5654-48a9-9367-99f258779f91" />

 

# Shell Script
```
echo '#!/bin/sh' > my-script.sh
echo 'echo Hello World' >> my-script.sh
echo 'exit 0' >> my-script.sh
```
```chmod 755 my-script.sh```
```./my-script.sh```

## OUTPUT


<img width="556" height="277" alt="15" src="https://github.com/user-attachments/assets/8125ae75-fbdd-4789-a66a-3c8fd120306c" />



 
```cat << stop > herecheck.txt```

```
hello in this world
I can't stop
learning linux 
because it's so fun
stop
```

```cat herecheck.txt```

## OUTPUT



<img width="820" height="163" alt="53" src="https://github.com/user-attachments/assets/9913064d-49ff-44c2-9a77-f562c652cdd3" />



```cat > scriptest.sh ```

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
 ```

```cat scriptest.sh ```
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
 
```chmod 777 scriptest.sh```
 
```./scriptest.sh 1 2 3```

## OUTPUT


 <img width="862" height="484" alt="54" src="https://github.com/user-attachments/assets/dfc739f2-5a79-47bc-a78e-86b1a9d52338" />



```ls file1```

## OUTPUT


<img width="635" height="75" alt="55" src="https://github.com/user-attachments/assets/9ed4e305-6fec-477c-b35b-590102313c59" />



```echo $?```

## OUTPUT 


<img width="635" height="80" alt="56" src="https://github.com/user-attachments/assets/41c0c728-1ee0-452c-9eab-a9115aea2713" />



```./one bash: ./one: Permission denied```
 
```echo $?```

## OUTPUT 


<img width="635" height="148" alt="57" src="https://github.com/user-attachments/assets/50e12b34-da58-4fbc-955d-d4f8aa227175" />

 
```abcd```
 
```echo $?```

 ## OUTPUT


<img width="635" height="146" alt="58" src="https://github.com/user-attachments/assets/25eb067e-d5ac-4fd7-a9a5-deef61072ba9" />

 
# mis-using string comparisons

```cat > strcomp.sh ```

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

```cat strcomp.sh ```

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

```chmod 755 strcomp.sh```
 
```./strcomp.sh ```

## OUTPUT


<img width="745" height="155" alt="59" src="https://github.com/user-attachments/assets/dae0b62c-6fe0-4322-b3d2-5f7d01f4d7ac" />



## check file ownership

```cat > psswdperm.sh ```

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

```cat psswdperm.sh ```
```bash
/#!/bin/bash
if [ -O /etc/passwd ]
then
echo “You are the owner of the /etc/passwd file”
else
echo “Sorry, you are not the owner of the /etc/passwd file”
fi
 ```

```chmod 755 psswdperm.sh```

```./psswdperm.sh```

## OUTPUT


<img width="785" height="152" alt="60" src="https://github.com/user-attachments/assets/1c332c5f-ad3f-481d-baec-06fac2318a56" />


## check if with file location

```cat > ifnested.sh``` 

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

```cat ifnested.sh ```

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

```chmod 755 ifnested.sh```

```./ifnested.sh ```

## OUTPUT


<img width="827" height="207" alt="21" src="https://github.com/user-attachments/assets/60f4a936-7029-4533-8eb6-ee30d321aa8d" />



## using numeric test comparisons

```cat > iftest.sh ```

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


```cat iftest.sh ```

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

```chmod 755 iftest.sh```
 
```./iftest.sh ```

## OUTPUT


<img width="700" height="172" alt="22" src="https://github.com/user-attachments/assets/ec8171b3-742f-4834-bd18-30ba05297893" />



## looking for a possible value using elif

```cat > elifcheck.sh ```

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

```chmod 755 elifcheck.sh```
 
```./elifcheck.sh ```

## OUTPUT


<img width="795" height="177" alt="23" src="https://github.com/user-attachments/assets/32e98a5d-8419-4a8c-9c97-76d821592315" />



## testing compound comparisons

```cat > ifcompound.sh ```

```bash
\#!/bin/bash
if [ -d $HOME ] && [ -w $HOME ]
then
echo "The file exists and you can write to it"
else
echo "I cannot write to the file"
fi
```
```chmod 755 ifcompound.sh```

```./ifcompound.sh ```

## OUTPUT


<img width="802" height="157" alt="24" src="https://github.com/user-attachments/assets/f9e2491d-2723-4643-a78c-7f23c2e016b5" />



## using the case command

```cat > casecheck.sh ```

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

```chmod 755 casecheck.sh ```
 
```./casecheck.sh ```


 ## OUTPUT


 <img width="428" height="132" alt="25" src="https://github.com/user-attachments/assets/f275a74e-648a-4228-91d0-a9ebb115cc62" />

 

```cat > whiletest.sh```

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

```chmod 755 whiletest.sh```
 
```./whiletest.sh```

## OUTPUT


 
 <img width="480" height="358" alt="26" src="https://github.com/user-attachments/assets/e2da4ff1-2f10-49dd-a9e3-17c18e3bbac6" />



```cat > untiltest.sh ```

```bash
\#using the until command
var1=100
until [ $var1 -eq 0 ]
do
echo $var1
var1=$[ $var1 - 25 ]
done
```

```chmod 755 untiltest.sh```

```./untiltest.sh```
 
 ## OUTPUT

 
 <img width="712" height="226" alt="27" src="https://github.com/user-attachments/assets/cb19021c-299e-4814-8b86-521a26eaa3ac" />

 
```cat > forin1.sh ```

```bash
\#!/bin/bash
\#basic for command
for test in Alabama Alaska Arizona Arkansas California Colorado
do
echo The next state is $test
done
 ```
 
```chmod 755 forin1.sh```

```./forin1.sh```

## OUTPUT


 <img width="691" height="297" alt="28" src="https://github.com/user-attachments/assets/503c30df-12aa-49be-85fe-76b14fef756d" />

 

```cat > forin2.sh ```

```bash
\#!/bin/bash
\# another example of how not to use the for command
for test in I don't know if this'll work
do
echo “word:$test”
done
 ```
 
```chmod 755 forin2.sh```

```./forin2.sh```

 
## OUTPUT


 <img width="818" height="228" alt="29" src="https://github.com/user-attachments/assets/a215b773-72e9-427d-a9ac-8697b878dd72" />

 

```cat > forin3.sh ```


```bash
\#!/bin/bash
\# another example of how not to use the for command
for test in I don\'t know if "this'll" work
do
echo "word:$test"
done
```

```chmod 755 forin3.sh```

``` ./forin3.sh ```

 ## OUTPUT


 <img width="867" height="293" alt="30" src="https://github.com/user-attachments/assets/81530de0-7c7f-4cfb-844f-a672bd400430" />


```cat > forinfile.sh ```

```bash
#!/bin/bash
# reading values from a file
file="cities"
for state in `cat $file`
do
echo "Visit beautiful $file“
done
```

```bash
chmod 777 forinfile.sh

cat > cities

Hyderabad
Alampur
Basara
Warangal
Adilabad
Bhadrachalam
Khammam
```

## OUTPUT


<img width="513" height="600" alt="31" src="https://github.com/user-attachments/assets/f49710d8-1796-44a0-9e2d-03a852a01eb6" />



```cat > forctype.sh ```

```bash
#!/bin/bash
# testing the C-style for loop
for (( i=1; i <= 5; i++ ))
do
echo "The value of i is $i"
done
````

```chmod 755 forctype.sh```

```./forctype.sh```

## OUTPUT


<img width="637" height="226" alt="32" src="https://github.com/user-attachments/assets/dd48c538-61b6-4fa9-ac60-5bcfe9cdec0d" />



```cat > forctype1.sh ```

```bash
#!/bin/bash
# multiple variables
for (( a=1, b=5; a <= 5; a++, b-- ))
do
echo "$a - $b"
done
```

```chmod 755 forctype.sh```

```./forctype1.sh ```

## OUTPUT


<img width="617" height="228" alt="33" src="https://github.com/user-attachments/assets/1d973f0e-c308-42fc-bef5-79f6d14bb6c7" />



```cat > fornested1.sh ```

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

```chmod 755 fornested1.sh```
 
```./fornested1.sh ```


 ## OUTPUT

 
<img width="646" height="488" alt="34" src="https://github.com/user-attachments/assets/cded1d52-4b7f-41a6-a644-57e0bbd67038" />


 
```cat > forbreak.sh``` 

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

```chmod 755 forbreak.sh```
 
```./forbreak.sh ```

## OUTPUT


<img width="900" height="282" alt="35" src="https://github.com/user-attachments/assets/0b879f17-9cf1-42c2-81e4-a24eec0f634b" />

 
```cat > forcontinue.sh ```

```bash
#!/bin/bash
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

 
```chmod 755 forcontinue.sh```
 
```./forcontinue.sh ```

## OUTPUT


 <img width="545" height="321" alt="36" src="https://github.com/user-attachments/assets/badfeead-bee9-449a-bab8-4bb3bfc24433" />



```cat > exread.sh ```

```bash
#!/bin/bash
# testing the read command
echo -n "Enter your name: "
read name
echo "Hello $name, welcome to my program. "
 ```
 
```chmod 755 exread.sh ```
 
```./exread.sh ```


## OUTPUT


<img width="628" height="220" alt="37" src="https://github.com/user-attachments/assets/c30215b9-05a0-429e-834c-dacdf73b9864" />



 ```cat > exread1.sh```
 
```bash
#!/bin/bash
# testing the read command
read -p "Enter your name: " name
echo "Hello $name, welcome to my program."

``` 
```chmod 755 exread1.sh``` 

```./exread1.sh ```

## OUTPUT



<img width="577" height="212" alt="38" src="https://github.com/user-attachments/assets/7f0ccca6-4c68-48a3-8fd9-248e273ce2ca" />



```cat > funcex.sh```

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

```./funcex.sh ```

 
```./funcex.sh 1 2```

 ## OUTPUT

 
 <img width="487" height="271" alt="39" src="https://github.com/user-attachments/assets/8be07a5c-ce87-4f0d-91ab-3764f6938dbf" />



```cat > argshift.sh```

```bash
#!/bin/bash 
 while (( "$#" )); do 
  echo $1 
  shift 
done
```

```chmod 777 argshift.sh```

```./argshift.sh 1 2 3```

## OUTPUT


<img width="536" height="173" alt="40" src="https://github.com/user-attachments/assets/a3992869-30b7-4e8c-924d-624fdf4b7586" />


 
 ```cat > argshift1.sh```
 
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

```chmod 777 argshift1.sh```

```./argshift1.sh 1 2 3```

## OUTPUT



<img width="398" height="176" alt="41" src="https://github.com/user-attachments/assets/016107b7-c7e0-4dfc-9c93-ff1c6bf67074" />


 
```cat > argshift2.sh```

```bash
#!/bin/bash 
set -x 
while (( "$#" )); do 
  echo $1 
  shift 
done
set +x
```

```chmod 777 argshift2.sh```

```./argshift2.sh 1 2 3```
 
## OUTPUT

 
 <img width="678" height="553" alt="42" src="https://github.com/user-attachments/assets/a268409e-23fd-410c-adac-fb26a6d9e72c" />

 

```cat > nc.awk```

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

```cat > data.dat```

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

```awk -f nc.awk data.dat```

## OUTPUT 


 <img width="825" height="376" alt="43" src="https://github.com/user-attachments/assets/b7e95aff-37e1-4d9a-a41c-387141f20dea" />



```cat > palindrome.sh```


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


<img width="547" height="376" alt="44" src="https://github.com/user-attachments/assets/851533df-5728-45ae-beaa-1faa2cca588b" />



# RESULT:

The Commands are executed successfully.

# Bash Script

- Bash is the language that you can write scripts (programs) in Linux

- You can create file name.sh and then write- all commands you need then exwcute it with

-------------------------------------

- first add #!/bin/bash in the first line
- Example: # nano name.sh

```bash
#!/bin/bash

ls

echo "this is red nexus"
```
then save file as CTRL+X then Y
```bash
bash name.sh
```
---------------------------------

#### To print "name tom"

```bash
#!/bin/bash

name="tom adam"
echo $name
```
- Save then
```bash
bash name.sh
```

-----------------------------------
#### To read a file in location /home/name.txt

```bash
#!/bin/bash

file="/home/name.txt"
cat $file
```
---------------------------------------------

#### To take argument from user while executing file
```bash
#!/bin/bash
echo $1
```
- `$1` means the first argument while executing
- `bash xyz.txt rednexus`
- It will print rednexus

---------------------------------------------

#### You can make loop in terminal not in a file as

```bash
 for i in {1..100}; do echo "$i"; done
```
- It will print all numbers between 1 to 100
- If we need to read file lines one by one
```bash
 for I in cat xyz.txt; do echo "$i"; done
Observe() is
```

- To get output of command use ` ` as

```bash
for i in `ifconfig`; do echo $i; done
```

-------------------------------------

### introduction to Sed

- The substitute command
- flags and Delimiters `"g", "i", "d"` flag

#### Command to sed

```bash
sed 's/name/name2/' < name_file.txt
```

```bash
echo "Name tom" | sed 's/tom/adam/'
```

```bash
echo "hello world i am tom" | sed 's/hello/hi/;s/tom/toom/'
```

```bash
sed 's/name1/name2/g' < name.txt
```

```bash 
sed -i 's/name1/name2/g' name_file.txt
```
- Delete Flage 

```bash
sed '/name/name2/d' name_file
```

---------------------------------------------

### Assigning Values to Variables

#### 1. Direct Assignment

```bash
VAR=value
```

- **No spaces** around `=`
- With spaces, the shell treats it as a command, not an assignment

```bash
VAR = value    # Incorrect! interpreted as a command
```

#### Example

```bash
count=5
echo "count: $count"
```

- Use `$` to read the variable's value

#### Tip: Use quotes for clarity

```bash
echo "It's a good day today"
echo "hello \ - backslash and a dash"
```

---------------------------------------------

### Using read to Assing Values

```bash
read VAR
```
- Example:

```bash
echo "Enter your name:"
read name
echo "name: $name"
```
- Prompt lnline with -p:

```bash
read -p "Enter your age: " age
echo "Age: $age
```

- Silent input with `-s` (e.g.,for password):

```bash
read -sp "Enter your password: " password
echo "The Paswword is : @password"
```
### Reading from file:

```bash
read name < /etc/hostname
```

-----------------------------------------

### Pereferred Method: `$(pwd)` (modern and easier to nets.)

```bash
echo "current directory: $current_directory"
```
# copy-file
## AIM:
To write a python program for copying the contents from one file to another file.
## EQUIPEMENT'S REQUIRED: 
PC
Anaconda - Python 3.7
## ALGORITHM: 
### Step 1:

From shutil import copy file

### Step 2: 

 From sys import exit
 
### Step 3:

Getting input for source file

### Step 4:  

Getting input for target file

### Step 5: 

Giving condition for files

### Step 6:

Getting statement from the user to print or not want to print
```
## PROGRAM:
#Developed by :Kavinraja D
#Reg no : 22007928

import sys
count=0
with open(sys.argv[1],'r') as f:
        for line in f:
            word=line.split()
            count+=len(word)
print("Word Count in File=",count)
from shutil import copyfile
from sys import exit

source = input("Enter source file with full path: ")
target = input("Enter target file with full path: ")

# adding exception handling
try:
    copyfile(source, target)
except IOError as e:
    print("Unable to copy file. %s" % e)
    exit(1)
except:
    print("Unexpected error:", sys.exc_info())
    exit(1)

print("\nFile copy done!\n")

while True:
    print("Do you like to print the file ? (y/n): ")
    check = input()
    if check == 'n':
        break
    elif check == 'y':
        file = open(target, "r")
        print("\nHere follows the file content:\n")
        print(file.read())
        file.close()
        print()
        break
    else:
        continue
```

### OUTPUT:
file:///home/sec/Pictures/Screenshots/kavinraja5c.png![image](https://user-images.githubusercontent.com/119875375/214771694-8ce5ba6d-69c5-4534-8025-f898bda32ba5.png)




## RESULT:
Thus the program is written to copy the contents from one file to another file.

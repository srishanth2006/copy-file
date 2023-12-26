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
## PROGRAM:
```
#Developed by :SRISHANTH J
#Reg no : 212223240160

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
<img width="354" alt="Screenshot 2023-12-26 181241" src="https://github.com/srishanth2006/copy-file/assets/150319470/199f26db-6ee7-4c3d-bbfa-a32ba78bb886">+

<img width="356" alt="Screenshot 2023-12-26 181453" src="https://github.com/srishanth2006/copy-file/assets/150319470/46c2dd6e-c9d3-4c15-9120-75cd453f6a9b">


## RESULT:
Thus the program is written to copy the contents from one file to another file.

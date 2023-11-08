### Section 1.1: Hello World 
#### Interactive Shell
The Bash shell is commonly used interactively:It lets you enter and edit commands, then executes them when you press the **Return** key.	

Output "Hello World" by typing the following 
```
    echo "Hello World"
    #> Hello  World # Output Example 
```
 **Notes**

 -  You can change the shell by just typing the name of the shell in terminal. For example: sh,bash etc. 
 -  **echo** is a bash built-in command that writes the arguments it receives to the standard output. 

#### Non-Interactive Shell
The Bash shell can also be run non-interactively from a script, making the shell require no human interaction. 

Follow these steps to create a Hello World script:
```
1. Create a new file called hello-world.sh
    touch hello-world.sh
2. Make the script executable bu running 
    chmod +x hello-world.sh
3. Add this code 
    #!/bin/bash
    echo "Hello World"
```
**Line 1**: The first line of the scriptmust start with the character sequence #!, referred to as sshebang1. It instructs the operating ssytem to run /bin/bash, passinf it th scipt's path as an arguments.
**Line 2**: Uses the echo command to write Hello World to the standart output.
```
4. Execture the hello-world.sh script from the command line using one of the following.
    - ./hello-world.sh – most commonly used, and recommended
    - bin/bash hello-world.sh
    - bash hello-world.sh – assuming /bin is in your $PATH
    - sh hello-world.sh
```

####Section 1.2: Hello World Using Variables
Create a new file called hello.sh with the following content and gice it executable permissions with the chmod +x hello.sh
```
Execute/Run via: ./hello.sh

#!/usr/bin/env bash
# Note that spaces cannot be used around the `=` assignment operator
whom_variable="World"
# Use printf to safely output the data
printf "Hello, %s\n" "$whom_variable"
#> Hello, World
```
This will print **Hello, World** to standard output when executed.


The following code accepts an argument $1, which is the ﬁrst command line argument, and outputs it in a formatted string, following Hello,.

```
Execute/Run via: ./hello.sh World
#!/usr/bin/env bash
printf "Hello, %s\n" "$1"
#> Hello, World
```
It is important to note that $1 has to be quoted in double quote, not single quote. "$1" expands to the ﬁrst
command line argument, as desired, while '$1' evaluates to literal string $1.

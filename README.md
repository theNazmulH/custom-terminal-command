
Creating Bash scripts that are accessible to all users on your computer is straightforward by placing them in the /usr/local/bin directory. However, this requires administrative privileges. Here's a refined set of instructions for your script:

1.  **Create Your Script:** Open your preferred text editor and list the commands you want your script to run, with each command on a separate line. You can include comments in your script by prefixing a line with `#`.
   
    

> #!/bin/bash

> echo "Good Morning"

    
2.  **Move Your Script to the Correct Location:** The designated directory for user scripts is /usr/local/bin. Since this directory is owned by root, administrative privileges are required. Assuming your script is in your home directory (e.g., ~/greet.sh), use the following command in the terminal:
    
    
    `sudo mv ~/greet.sh /usr/local/bin/SCRIPTNAME` 
    
    Replace `SCRIPTNAME` with the desired command name, excluding the .sh file extension.
    
3.  **Set Correct Owner and Permissions:** Ensure the script is owned by root and has appropriate permissions. Run the following commands:
    
    `sudo chown root: /usr/local/bin/SCRIPTNAME
    `
    
    `sudo chmod 755 /usr/local/bin/SCRIPTNAME` 
    
5.  **Run Your Script:** Now, you can execute your script by simply typing the command you assigned to it. In this example, if you named it `greet`, run:
    
    
    `greet` 
    
    Enjoy the convenience of running your custom script system-wide.

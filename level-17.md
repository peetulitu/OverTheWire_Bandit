## OBJECTIVE
There are 2 files in the home directory: passwords.old and passwords.new. The password for the next level 
is in passwords.new and is the only line that has been changed between passwords.old and passwords.new
NOTE: If you have solved this level and see ‘Byebye!’ when trying to log into bandit18, this is related 
to the next level, bandit19

## APPROACH
This level asks for a line that has been changed between two files. Looking at the recommended commands, 
the one that stands out to me the most to solve this is the diff command, so I will look at its man page 
to see if there is anything I can do with it. I found that just using the command on its own paying 
attention to the order of the files without any flags, it outputted the lines that are different, 
providing the password for the next level.

## COMMANDS USED
```bash
diff passwords.new passwords.old
```

## TAKEAWAY
At first, I was placing the passwords.old file first in the command and then copying the first line of
output as the password, of course, that didn't work as it was the old version of the file, so I quickly
realized that I had to use the other one. Overall, it was a very easy level, just enough to learn a new
command, which is always nice.

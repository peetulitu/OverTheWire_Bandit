## Objective
The password for the next level is stored in a file somewhere under the inhere directory and has all of the following properties:
- Human-readable
- 1033 bytes in size
- Not executable

## Approach
This time we got a similar challenge with more complexity, but we followed the same approach as before, first we broke down the
parameters we need our file to match and we construct our command following these, adding a flag for each characteristic we are
looking for.

Breaking down the flags:
- `-type f` -> Regular files only.
- `-size 1033c` -> Exactly 1033 bytes (c=bytes, k=KB, M=MB)
- `! -executable` -> Not executable files (the ! negates the flag)
- `-readable` -> Files that are readable by the current user.

## Commands Used
```bash
find /home/bandit5/inhere -type f -size 1033c ! -executable -readable
```

## Takeaway
This level was very useful to learn more about flags and how to combine them to curate the command you need.

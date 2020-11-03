# nix-oneliners
My personal collection of Unix-like terminal oneliners


## Find a string in all files inside a subdirectory
```
find | awk '{system("cat " $1)}' | grep <string>
```
To use, just replace <string> with the specific string to find

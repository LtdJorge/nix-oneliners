# nix-oneliners
My personal collection of Unix-like terminal oneliners


## Find a string in all files inside a directory (recursive)
```
find | awk '{system("cat " $1)}' | grep <string>
```
To use, just replace <string> with the specific string to find

## Find a string in all files with a specific extension in a directory (recursive)
```
find | grep .<extension> | awk '{system("cat " $1)}' | grep <string>
```
To use, replace <extension> with the extension of the files to search in, and <string> with the string to search for.
Example:

```
find | grep .yaml | awk '{system("cat " $1)}' | grep nginx
```

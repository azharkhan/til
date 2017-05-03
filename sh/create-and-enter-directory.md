# Create and Enter a Directory

A handy shortcut for creating a directory and changing the current working directory to the new directory's location. This should work on most Unix shells (AFAIK)

    mkdir && cd "$_"

`$_` is a special parameter that holds the last argument of the previous command. The quotes around the `$_` makes sure that it works even if the folder name contains spaces!

[source](https://unix.stackexchange.com/a/125459)

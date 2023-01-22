# PACKAGING SCRIPTS

This is a little collection of packaging tools for POSIX systems.

The collection `gettar-create`, `gettar-tmpdir` and `gettar` can be
used as a glue between scripts that build software and the scripts
that deploy software, allowing their separation.

    # Build script.
    > tmp="`gettar-tmpdir my-website-1`"
    > make all install DESTDIR="$tmp"
    > gettar-create -v "$tmp"

    # Deployment script.
    > tars="`gettar my-website-1 my-website-2`"
    > test -n "$tars"

## Help

gettar

    Usage: gettar [NAME-WILDCARD...]
    
    Fetch tars from `~/.gettar` and print their pathnames. You can
    override the directory by setting GETTAR_DIR.
    
    If one of the supplied names is not found then it doesn't print
    anything and shows an error message.
    
    If the wildcard matches more than one file, then it prints an
    error.

gettar-create

    Usage: gettar-create [-v] DIRECTORY [NAME]
    
    Create a tar file in the tar directory.

gettar-tmpdir

    Usage: gettar-tmpdir NAME
    
    Print a temporary directory name to use for creating a package.

## Collaborating

For making bug reports, feature requests and donations visit
one of the following links:

1. [gemini://harkadev.com/oss/](gemini://harkadev.com/oss/)
2. [https://harkadev.com/oss/](https://harkadev.com/oss/)


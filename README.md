[https://www.youtube.com/watch?v=tK9Oc6AEnR4&ab_channel=freeCodeCamp.org](https://www.youtube.com/watch?v=tK9Oc6AEnR4&ab_channel=freeCodeCamp.org)

## Create Text File

1. Create file `vim textfile.txt`
    1. Type `i` to enter `Insert` mode
    2. Enter `Hello World!`
    3. Hit `esc`, then enter `:qw` to write and quit
    4. Output file `cat textfile.txt`
    

## Hello World

1. Create file `vim shellscript.sh`
    1. Type `a` to enter `Append` mode, which outputs character after cursor
    2. Enter `echo Hello World!`
    3. Hit `esc`, then enter `:qw` to write and quit
    4. Run script `zsh [shelltest.sh](http://shelltest.sh)` or `bash shelltest.sh`

## Run Script without ZSH or BASH Command

1. Modify file `vim shellscript.sh`
    
    ```bash
    #!/bin/zsh
    echo Hello World!
    ```
    
    1. modify permissions `chmod u+x shellscript.sh`
    2. Run script `./shellscript.sh`

## Variables

```bash
#!/bin/zsh

## BAD
cp /my/location/from /my/location/to
cp /my/location/from/here /my/location/to/there

## GOOD

MY_LOCATION_FROM=/my/location/from
MY_LOCATION_TO=/my/location/to

cp $MY_LOCATION_FROM $MY_LOCATION_TO
cp "$MY_LOCATION_FROM" "$MY_LOCATION_TO"
```

1. Create file `vim hellothere.sh`
    
    ```bash
    #!/bin/zsh
    FIRST_NAME=Abraham
    LAST_NAME=Choi
    
    echo Hello $FIRST_NAME $LAST_NAME
    ```
    
    1. modify permissions `chmod u+x hellothere.sh`
    2. Run script `./hellothere.sh`
    

## Arguments

1. Create file `vim interactive.sh`
    
    ```bash
    #!/bin/zsh
    
    echo "What is your first name?"
    read FIRST_NAME
    echo "What is your last name?"
    read LAST_NAME
    
    echo Hello $FIRST_NAME $LAST_NAME
    ```
    
    1. modify permissions `chmod u+x interactive.sh`
    2. Run script `./interactive.sh`

1. Create file `vim posargs.sh`
    
    ```bash
    #!/bin/zsh
    
    echo Hello $1 $2
    ```
    
    1. modify permissions `chmod u+x posargs.sh`
    2. Run script `./posargs.sh [ARG 1] [ARG 2]`
[https://www.youtube.com/watch?v=tK9Oc6AEnR4&ab_channel=freeCodeCamp.org](https://www.youtube.com/watch?v=tK9Oc6AEnR4&ab_channel=freeCodeCamp.org)

## Create Text File

1. Create file `vim textfile.txt`
    a. Type `i` to enter `Insert` mode
    b. Enter `Hello World!`
    c. Hit `esc`, then enter `:qw` to write and quit
    d. Output file `cat textfile.txt`
    

## Hello World

2. Create file `vim shellscript.sh`
    a. Type `a` to enter `Append` mode, which outputs character after cursor
    b. Enter `echo Hello World!`
    c. Hit `esc`, then enter `:qw` to write and quit
    d. Run script `zsh [shelltest.sh](http://shelltest.sh)` or `bash shelltest.sh`

## Run Script without ZSH or BASH Command

3. Modify file `vim shellscript.sh`
    
    ```bash
    #!/bin/zsh
    echo Hello World!
    ```
    
    a. modify permissions `chmod u+x shellscript.sh`
    b. Run script `./shellscript.sh`

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

4. Create file `vim hellothere.sh`
    
    ```bash
    #!/bin/zsh
    FIRST_NAME=Abraham
    LAST_NAME=Choi
    
    echo Hello $FIRST_NAME $LAST_NAME
    ```
    
    1. modify permissions `chmod u+x hellothere.sh`
    2. Run script `./hellothere.sh`
    

## Arguments

5. Create file `vim interactive.sh`
    
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

6. Create file `vim posargs.sh`
    
    ```bash
    #!/bin/zsh
    
    echo Hello $1 $2
    ```
    
    1. modify permissions `chmod u+x posargs.sh`
    2. Run script `./posargs.sh [ARG 1] [ARG 2]`
# Welcome to the Go Course!

## Preparing for the Course

### Installing Go

The first step is to download and install Go [here](https://golang.org/dl/)

The most important part of installing Go is setting up the `$GOPATH` environment variable. You can set this variable to whatever folder you wish, but it must have a child `src` folder beneath it. For the purposes of this course, we will use the folder `work`.

#### Mac

1. Create the `~/work` folder and the `src` folder beneath it
1. In the `~/.bash_profile` file, add the following lines:

```
export GOPATH=$HOME/work
export PATH=$PATH:$GOPATH/bin
```

#### Windows

1. Create the `C:\work` folder and the `src` folder beneath it

The installer should have added the appropriate environment variables, but just in case:

1. Add `GOPATH` environment variable

    1. Go to the `Control Panel -> System` and Click on `Advanced system settings`
    1. In the dialog, click the `Advanced` tab
    1. Then click on the `Environment Variables` button
    1. Under `System Variables`, click the `New` button
    1. Enter `GOPATH` for the name, and path to your `work` folder
    1. Click `OK`

### Workspace

The workspace is defined first by the location pointed to by `GOPATH`. Beneath the `src` folder is where projects are located.

Usually, to conform to best practices, beenath the `src` folder are the names of the organizations where the code is stored. Typically, these are SCMs, like `github.com`.

Beneath them is the name or organization name of the account owner for the SCM. For example: `nordstrom` or your own name.

And finally, the final folder is the actual Go project folder. 

```
~/work                              // The main source folder, but can be any folder name
    |
    |-- 📂 src
        |
        |--  📂 bitbucket.org
            |--  📂 nordstrom
                |-- order-guard     // Location of order-guard repo
        |-- 📂 github.com
            |--  📂 andrewlader
                |-- go-course       // Location of go-course work
```

### Verify Go Installation

The easiest way to verify that Go was installed properly is to perform the following command from a terminal window:

```
go env
```

Look at the ouput and ensure that the `GOPATH` environment variable is set appropriately.

# jssh
Bash script for easier input to [cluster-ssh (CSSHX)](https://formulae.brew.sh/formula/csshx) if you have numbered hosts

Supports a single argument in 3 formats
## Single Host
`jssh my-host00` will run the command `csshX my-host00`

## Multiple Hosts
`jssh my-host[00,01,04]` will run the command `csshX my-host00 my-host01 my-host04`

## Range of Hosts
For range of hosts, the script will zero-pad to match the length of the first number provided<br>

`jssh my-host[000-007]` will run the command 

```csshX my-host00 my-host01 my-host02 my-host03 my-host04 my-host05 my-host06 my-host07```

`jssh my-host[000-7]` will run the command

```csshX my-host00 my-host01 my-host02 my-host03 my-host04 my-host05 my-host06 my-host07```

## Prerequisite
```
brew install csshx
```

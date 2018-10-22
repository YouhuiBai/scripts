# scripts for using cluster

## 1 scp 

scp some files to hosts gpu1-18, operating on gpu0, for example:

```shell
$ scripts/scptohosts ~/YouhuiBai/* # will scp all files in YouhuiBai dir to ~/YouhuiBai dir at gpu0-18
```

## 2 operate command on selected hosts

operate some commands on selected hosts

```shell
$ scripts/call_scripts -h #for help
# --command: the command which will be operated
# --hosts: hosts id
# --multithread: operating commands using multithread, namely, operating command on all selected machines parallelly
# --terminal: give the ssh a terminal  
```

for example:
```shell
$ scripts/call_scripts --command "cd YouhuiBai; ls" --hosts $(seq 1 18) --terminal
```
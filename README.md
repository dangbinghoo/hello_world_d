# Dlang hello world for test binary footprint size

## compile cmds

```sh
  > dub build -b release --compiler=ldc2

  > ls -lh
-rw-r--r-- 1 user user  291  april  9 10:43 dub.json
-rwxr-xr-x 2 user user 1.2M  april  9 10:46 hello_world_d
-rw-r--r-- 1 user user    0  april  9 10:44 README.md
drwxr-xr-x 2 user user   60  april  9 10:42 source

  > strip hello_world_d

  > ls -lh
-rw-r--r-- 1 user user  291  april  9 10:43 dub.json
-rwxr-xr-x 2 user user 849K  april  9 10:48 hello_world_d
-rw-r--r-- 1 user user    0  april  9 10:44 README.md
drwxr-xr-x 2 user user   60  april  9 10:42 source
```

You see, print a single line costs 849K !

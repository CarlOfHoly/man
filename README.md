# How to create man pages

[based on this artice](https://www.howtogeek.com/682871/how-to-create-a-man-page-on-linux/)

## Step 1
To review man page run 

```
pandoc <file>.1.md -s -t man | /usr/bin/man -l -
```


## Step 2
To create actual man page

```
pandoc <file>.1.md -s -t man -o <file>.1
```

## Step 3
Gzip and move to manpath

```
sudo cp <file>.1.d /usr/local/man/man1
sudo gzip /usr/local/man/man1/<file>.1.d
```

## Step 4
Update mandb and enjoy

```
sudo mandb
```


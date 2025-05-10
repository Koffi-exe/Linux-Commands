# Day 6 --> CRON, tar and zip

### to see the actual size of a file on disk:
	
``` bash	
	du -sh fileName
```



### create a archive file 

``` bash
	tar -cvf newFileName.tar <fileToBeArchived>
```

### create a copressed fiel

``` bash
	tar -czvf newFielName.tar.gz <fileToBeCompressed>
```


## ZIP ARCHIVE

### 1. create a zip archive

``` bash	
	zip my-archive <file1 file2 ...>
```

### 2. zip a dir

``` bash	
	zip -r my-zip-dir <dirName>
```


## THE OG CRON 

``` bash
***** // Minute (0-59), Hour (0-23), Day of month (1-31), Month(1-12), Day of week (0-7)
```
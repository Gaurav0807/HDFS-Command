# HDFS-Command
HDFS(Hadoop Distributed File System) Command


# Alert :----> I am using cloudera for Hadoop 

# Give list of all command
Command :- hadoop fs or hdfs dfs (both are same command )

# Give list of all command that can be used with ls
command :- hadoop fs -help ls

# List of all the files in local System
command :- hadoop fs -ls

# List of files in directory
command :- hadoop fs -ls /user/cloudera (Here I put /user/cloudera as directory name you can put your directory name.)

# Alert :-----> For hdfs command are same as linux command just difference is that we have to add (hadoop fs -)

# Sort by time in reverse order
command :- hadoop fs -ls -t -r /

# Sort by size by default largest is at top
command :- hadoop fs -ls -S /

# Sort by size ,Size will be displayed in human readable
command :- hadoop fs -ls -S -h /

# Alert :----> Human Readable means it will show size in KB,MB,GB,TB etc...

# List Recursively
command :- hadoop fs -ls R /

# Search in the list 
command :- hadoop fs -ls /user/cloudera/file1.txt |grep hyy

# Creating a new Directory inside home 
command :- hadoop fs -mkdir /user/cloudera/testing

# Creating a hierarchy of directories
command :- hadoop fs -mkdir -p /user/cloudera/folder1/folder2

# Creating a file inside directory
command :- hadoop fs -touchz /user/cloudera/folder1/file1.txt  
   # Here -touchz create a file of zeo bytes

# removing files
command :- hadoop fs -rm /user/cloudera/folder1/file1.txt

# To remove directory we have to give -R(Recursively)
command :- hadoop fs -rm -R /user/cloudera/folder1

# rmdir can only remove empty directories
command :- hadoop fs -rmdir /user/cloudera/folder1
   # Alert :- (This will give error as folder1 directory is not empty)
 

# Copying files or folder from local to hdfs
 command :- hadoop fs -copyFromLocal Desktop/file1.txt  /user/cloudera/folder2
 
 # Check the free disk space
    df command is used to check the free disk space
 command :- hadoop fs -df -h /user/cloudera
 -h stands for human readable.
 
 # Check the disk Usage
 command :- hadoop fs -du -h /user/cloudera
 
 # GetMerge
 command :- hdfs dfs -getmerge -nl /user/file1.txt  /user/file2.txt  /user/filenew.txt
  -nl :- is used for adding new line. this will add a new line between the content of thses n files
  
 # To view the file data
 command :- hadoop fs -cat /user/cloudera/file2.txt
 
 # Copy the files and paste to other directories
 command :- hadoop fs -cp /user/clouder/file1.txt  /user/data/folder1
   # Same for Move  just changes are -cp changes to -mv
 
 
 # Move folder from 1 to 2
 command :- hadoop fs -put folder1 /data
 
# Copying files or folder from hdfs to local

command :- hadoop fs -get /user/cloudera/folder1 . (here (.) dot represent current directory)
hadoop fs -copyToLocal  <hdfs path> <local path>
or hadoop fs -get <hdfs path> <local path>

 
  
  
  
  
  


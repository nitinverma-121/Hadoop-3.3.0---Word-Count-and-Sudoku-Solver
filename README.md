# Hadoop 3.3.0: Word Count and Sudoku Solver

In this project, Hadoop 3.3.0 is installed and word count and Sudoku solver map reduce paradigm is implemented.

# NOTE:
After installation, 
1) Some xml files in etc/hadoop need changes. Kindly refer to our etc contents.
2) Some files in bin folder are missing. Kindly refer to our bin contents.

## Steps

After successful installation of hadoop 3.3.0, the following commands will be implemented.

####  Start all the hadoop daemons
```bash
cd hadoop-3.3.0/sbin
start-all.cmd  
```
####  Confirm that all daemons work properly
```bash
jps
```
####  Create a new directory in hdfs
```bash
hadoop dfs -mkdir /nitin/
```
####  Add source file in the above created directory
```bash
hadoop dfs -put C:/hadoop-3.3.0/source/word.txt /nitin/
```
####  Confirm the presence of the source file
```bash
hadoop dfs -ls /nitin/
```

### Word Count 

####  Run the map reduce code
```bash
hadoop jar C:/hadoop-3.3.0/share/hadoop/mapreduce/hadoop-mapreduce-examples-3.3.0.jar wordcount /nitin/ nitinresult/
```

### Sudoku Solver 

####  Run the map reduce code
```bash
hadoop jar C:/hadoop-3.3.0/share/hadoop/mapreduce/hadoop-mapreduce-examples-3.3.0.jar sudoku C:/hadoop-3.3.0/source/sudoku.txt > C:/hadoop-3.3.0/target/sudoku_ans.txt
```
####  See results of sudoku 
```bash
type sudoku_ans.txt
```

## GUI
http://localhost:9870/

http://localhost:8088/



## Co-Author

- [@Chehak-Batra](https://github.com/Chehak-Batra/)


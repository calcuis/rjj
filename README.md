### rjj (read-joint-jet)
rjj is a simple cmd-based data cleaning tool
#### install it via pip/pip3
```
pip install rjj
```
#### update rjj
```
pip install rjj --upgrade
```
#### check current version
```
rjj -v
```
#### read user manual
```
rjj -h
```
### jointer and splitter
joint or split your csv file(s)
#### jointer
joint all csv files in the current directory together as output.csv; all file names will be stored in te first field
```
rjj j
```
#### splitter
split the selected csv file into different csv files and name it according to the first field
```
rjj s
```

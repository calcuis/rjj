### rjj (read-joint-jet)
rjj is a simple cmd-based data transforming/analysis tool
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
#### convertor
convert json to csv; select a json file in the current directory, then give a name to the output file (don't need the extension)
```
rjj c
```
#### detector
detect the co-existing record(s) between two csv files; select two csv files to execute the detection process, then assign a name for the output file; co-existing record(s) will be indicated in a newly created column `Coexist`
```
rjj d
```
### jointer and splitter
joint or split your data file(s)
#### jointer
joint all csv files in the current directory together; all file names will be stored in the first field of the newly created column `File`; when you execute the command you will be asked for assigning a name for the output file
```
rjj j
```
#### splitter
split the selected csv file into different csv files and name it according to the value in the first field of that selected file
```
rjj s
```
#### xplitter
split the selected excel (.xls or .xlsx) into pieces and name it according to the value in the first field of that selected excel file
```
rjj x
```

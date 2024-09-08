### rjj (read-joint-jet) [![Static Badge](https://img.shields.io/badge/ver-0.4.7-black?logo=github)](https://github.com/calcuis/rjj/releases)
rjj is a simple cmd-based data transforming/analysis tool 🛠⚙
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
### data transformer
help you prepare your csv data file(s)
#### convertor
convert json to csv
```
rjj c
```
*select a json file in the current directory, choose to enter another file name (don't need the extension) for output or not (Y/n); if not, the converted csv will be saved with the same name as the json*♻
#### reversor
reverse csv back to json
```
rjj r
```
*select a csv file in the current directory, choose to enter another file name for output or not (Y/n); if not, the converted json file will be saved with the same name; 🌀support any data type, even emoji*🐷
#### detector
detect the co-existing record(s) between two csv files📃🔍📃
```
rjj d
```
*select two csv files to execute the detection process, then give a name for the output file; co-existing record(s) will be indicated in a newly created column `Coexist`*
#### filter
locate the input `Keyword` among all csv files in the current directory👁‍🗨 (and could opt to expand to its all sub-folder files; cool right?)🔍
```
rjj f
```
*source file (location info) will be indicated in a newly created first column `Source_file`; the exact coordinate (x,y) will be given in the newly created second and third columns, namely `Column_y` and `Row_x`; and the full record will be pasted behind for simplifying your auditing work* 📑
#### matcher
identify matched/repeated record(s)📃📃🔍 among all csv in the current directory and extend to its sub-directories📁
```
rjj m
```
*provide a name to the output file (if not, the output file will be named as output.csv); source file (location) will be indicated in a newly created column `Source_file`*
#### uniquer
identify unique/non-repeated record(s)🔍📃 among all csv in the current directory and extend to its sub-directories📁
```
rjj u
```
*give a name to the output file; source location will be indicated in a newly created column `Source_file`*
#### binder
bind all csv files together by columns in the current directory
```
rjj b
```
*binder is different from jointer below; it can be considered as a horizontal merge whereas jointer is for vertical merge (basically by rows)*
### jointer and splitter 📌✂️
joint or split your data file(s)
#### jointer
joint all csv files in the current directory together🖇
```
rjj j
```
*all file names will be stored in the first field of the newly created column `File`; when you execute the command you will be asked for assigning a name for the output file*
#### splitter
split the selected csv file to different csv files and name it according to the value in the first field of that selected file📑
```
rjj s
```
### extension for excel
extended function/module(s) for handling excel file(s)
#### xplit
split the selected excel (.xls or .xlsx) to pieces and name it according to the value in the first field of that selected excel
```
rjj x
```
#### joint
joint all excels (.xls and .xlsx) in the current directory together; all file names will be stored in the first field of the newly created column `File`
```
rjj t
```
*differ from csv jointer, since both .xls and .xlsx is accepted, and the file extention will not be taken, it will be merged while two of them share the same file name (cannot be split by the command above); understand this condition, make good use of it!* 🙌
#### matxh
identify matched/repeated record(s)🔍 in the current directory and extend to its sub-directories; for excel
```
rjj h
```
*source file (location) will be indicated in a newly created column `Source_file`; the exact sheet name inside that file will be told in another newly created column `Sheet_name`*
#### uniquex
identify unique/non-repeated record(s)🔍 in the current directory and extend to its sub-directories; for excel
```
rjj q
```
*source will be indicated in a newly created column `Source_file`; exact sheet will be told in `Sheet_name`*
#### kilter
locate the input `Keyword` among all excel files (.xls and .xlsx) in the current directory (and could expand to its sub-folders)👁‍🗨
```
rjj k
```
*this feature is similar to the csv filter; but since each excel file is possible to contain more than one sheet📄, the sheet number will be stored in the newly created column `Sheet_z`, then the exact coordinate (x,y) will be given after it, namely `Column_y` and `Row_x`; and the full record will be pasted behind as well; super kooooo* 🍻
### file/folder manager 📂👓
#### analyzor
run file analysis (process time depends on file size)
```
rjj a
```
*return file statistics and a summary report; include sha256 hash, size, duplicate and uniqueness count, etc.*
#### folder creator
create folder(s) according to the selected list (prepare a column storing all the folder name first)
```
rjj dir
```
### statistical analysis 🧮
simple statistical analysis is now available to perform on rjj 🍻
#### one-sample z-test
compare group with norm (population mean and standard deviation known)
```
rjj oz
```
#### one-sample t-test
compare group with norm (population mean known)
```
rjj ot
```
#### paired-sample t-test
compare group across time/paired-feature
```
rjj pt
```
*select first column as pre-test data; second column as post-test data*
#### independent-sample t-test
compare two independent groups; able to opt to calculate it based on equal variance assumed or not assumed
```
rjj it
```
*select first column as data of group 1; second column as data of group 2*
#### levene test
run Levene test for two groups (centered by mean)
```
rjj lv
```
*select first column as data of group 1; second column as data of group 2*
#### homogeneity of variance
run Levene test for two or more groups
```
rjj hv
```
*select first column as group variable; second column as data*
#### one-way anova
compare two or more groups
```
rjj oa
```
*select first column as group variable; second column as data*
#### correlation analysis
calculate Pearson correlation coefficient (r)
```
rjj ca
```
*explore the relationship between two variables*
### power analysis
estimate sample size for `paired-sample t-test`
```
rjj pp
```
estimate sample size for `independent-sample t-test`
```
rjj pi
```
estimate sample size for `one-way anova`
```
rjj po
```
estimate sample size for `correlation analysis`
```
rjj pc
```
estimate sample size for `regression analysis`
```
rjj pr
```
### descriptive statistics
calculate it for a column
```
rjj n
```
calculate it by group(s)
```
rjj g
```
### reliability test
run reliability analysis for a hypothetical construct; cheers! 🍻
```
rjj ra
```
*Cronach alpha if item deleted is provided as well; make your item screening task easy*
### regression analysis
make prediction(s) about the future 🎯
```
rjj ra
```
*evaluate the quality of predictor(s) as well as the intended model*
### plot a graph 📈
draw a scatter plot; awesome! 🙌
#### plotter
```
rjj p
```
*select first column as data for x-axis; second column as data for y-axis*
#### scatter
draw a scatter plot with line connecting points
```
rjj pl
```

[<img src="https://raw.githubusercontent.com/calcuis/rjj/master/demo1.jpg" width="350" height="280">](https://github.com/calcuis/rjj/blob/main/demo1.jpg)
[<img src="https://raw.githubusercontent.com/calcuis/rjj/master/demo2.jpg" width="350" height="280">](https://github.com/calcuis/rjj/blob/main/demo2.jpg)

#### liner
draw a line graph 📉
```
rjj l
```
#### charter
draw a bar chart 📊
```
rjj bar
```
*opt to assign label(s)* 🍻
#### boxplot
draw one boxplot 📦
```
rjj bx
```
#### boxplotter
draw many boxplot(s) 📦📦📦
```
rjj box
```
#### god knows
draw a map from god angle 👼
```
rjj map
```
#### donut
bake me a donut 🍩
```
rjj donut
```
[<img src="https://raw.githubusercontent.com/calcuis/rjj/master/demo4.jpg" width="350" height="280">](https://github.com/calcuis/rjj/blob/main/demo4.jpg)

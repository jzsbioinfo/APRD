# APRD
 APRD is an R package that caluclate growth rate using sliding window method. The package takes data from plate reader as input and return figures and excel file as output, it can process data from 96well plate or 384well plate. If fluorescence data is provided, it can also calculate fluorescence expression level according to the method of (Keren, Zackay et al. 2013. Fluorescence Protein expression per cell per second).


## Usage:
```
growth_rate_and_expression(inputfile, skip_num, plate,
                                       read_times_per_hour,
                                       total_read_times, blank_wells,
                                       X_hours_SW, medimum1="carbon",
                                       medimum2="nitrogen",
                                       outputdir,outputfile,
                                       outputfile2)
                                       
# inputfile="./dat-001-001-sd-p121.123.3AT_SCD-H.xlsx";
# skip_num=40; how many lines before the real data
# plate=96 means 96 well plate, plate=384 means 384 well plate.
# read_times_per_hour=6;total_read_times=217;
# blank_wells=c(1:12); the wells only with medimum as control. For example, A01:A12 (first row) is 1:12 and A01:H01 (first column) 
# X_hours_SW = 2; The time length (hours) of sliding window, need to be less than the total time.
# medimum1="carbon"; medimum2="nitrogen"; no meaning
# outputdir="./20200303output/";  the folder you want to output 
# outputfile = "20200303saad.xlsx" the growth rate result file 
# outputfile2 = "./20190731test96fi_2.xlsx" the fluoresence result file, if no, set like this.                                      

```

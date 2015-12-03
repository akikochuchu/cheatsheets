# File Fuzzing 
``` radamsa -o pdf_fuzz/mupdf_fuzz_%n.pdf -n 100 ../mupdf_test.pdf -M - ```
* -o : output
* %n : test case number
* -n : number of generated outputs
* -M - : write metadata to stdout


```
radamsa -p od -m ft=2,fo=2,fn,num=3,td,tr2,ts1 -v -n 10000 -o mutations/CDF-%n cdf.doc
```
* -p : Patterns - Which mutation patterns to use
* -m 

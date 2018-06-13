

# BamSplit
<b>BamSplit: A efficient software tools to split Bam form all chromosome together to each chr one bam</b>


</br></br></br>
The newest version of this funtion was integrated into toolkit <b>[BamDeal](https://github.com/BGI-shenzhen/BamDeal) </b>,please replace BamSplit by this <b>[BamDeal](https://github.com/BGI-shenzhen/BamDeal)</b>.

```php
           ./BamDeal  modify  bamSplit
```

</br></br>


1) Install
------------

Please replace BamSplit with this toolkit <b>[BamDeal](https://github.com/BGI-shenzhen/BamDeal)</b>.

</br></br></br>

  This software rely htslib，so should Pre-install htslib first [samtools-1.5/htslib-1.5](https://sourceforge.net/projects/samtools/files/samtools)
  </br>Then Just  [make]  or [sh  make.sh ]  to compile this software.
  </br>the final software can be found in the Dir [bin/BamSplit]

 For <b>linux /Unix </b> and <b>macOS </b>
<pre>
        tar -zxvf  BamSplit-XXX.tar.gz
        cd BamSplit-XXX;                             # if Link do not work ,Try <b>re-install</b>  two  library
        cd src;                                      #【zlib and htslib】 and copy them to the  library Dir
        make ; make clean                            # BamSplit-XX/src/include/zlib 
        ../bin/BamSplit                              # BamSplit-XX/src/include/gzstream
</pre>
</br>


2) Example
------------
* 1) Calculate bam files
```
#To Calculate bam
	./bin/BamSplit  -List  bam.list 
#Remain all read with -MinQ  -1 
	./bin/BamSplit  -List  bam.list  -OutDir  ./  -MinQ -1
#Remain The same header with all chr
	./bin/BamSplit  -List  bam.list -SameHead 

```

* 2) Calculate sam files
```
# To cCalculate sam
	./bin/BamSplit  -List  sam.list  -OutDir  ./  -SameHead 
# Also you the  add the  -MinQ to filter some reads
	./bin/BamSplit  -List  sam.list  -OutDir  ./   -OutSam 


```

3) Introduction
------------

* <b> Parameter description</b>

```php

/BamDeal  modify  bamSplit

        Usage: bamSplit  -InList  <bam.list>  -ReSetHead
        Usage: bamSplit  -InFile A.bam  B.bam

                -InFile    <str>     Input Bam/Sam File to split by chr
                -InList    <str>     Input Bam/Sam File List

                -OutDir    <str>     OutPut Dir for split [./]
                -MinQ      <int>     classify low mapQ<X read to unmap.bam[10]
                -OutSam              OutPut sam.gz File, not [bam]
                -ReSetHead           Reset Out.bam Header only with it's chr

                -help                Show this help [hewm2008 v1.02]

```

4) Results
------------
Format Introduction

* [sam bam format](https://samtools.github.io/hts-specs/SAMv1.pdf)

5）Discussing
------------
- email: hewm2008@gmail.com / hewm2008@qq.com  
- join the<b><i> QQ Group : 125293663</b></i>



######################swimming in the sky and flying in the sea ########################### ##

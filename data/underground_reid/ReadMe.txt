The GRID dataset is organised in two folders:

Folder 'probe' contains 250 probe images captured in one view (file names starts from 0001  to 0250).

Folder 'gallery' contains 250 true match images of the probes (file names starts from 0001  to 0250). Besides, there are a total of 775 additional images that do not belong to any of the probes (file name starts with 0000). These extra images should be treated as a fixed portion in the testing set during cross validation.


Features are extracted following the method outlined in 

Person Re-Identification: What Features are Important? 
C. Liu, S. Gong, C. C. Loy, and X. Lin 
International Workshop on Re-Identification, European Conference on Computer Vision, Firenze, Italy, 2012 (Re-Id @ ECCV 2012)

A MATLAB script sample.m is included to demonstrate how we perform a 10-fold cross validation. The correspondence.txt shows which gallery images relate to which row in ftrset in features_and_partitions.


Please cite our publication if this dataset is used in any academic and research reports.

Person Re-Identification: What Features are Important? 
C. Liu, S. Gong, C. C. Loy, and X. Lin 
International Workshop on Re-Identification, European Conference on Computer Vision, Firenze, Italy, 2012 (Re-Id @ ECCV 2012)

Time-Delayed Correlation Analysis for Multi-Camera Activity Understanding 
C. C. Loy, T. Xiang, and S. Gong 
International Journal of Computer Vision, vol. 90(1), pp. 106-129, October 2010 (IJCV 2010)


Please check http://personal.ie.cuhk.edu.hk/~ccloy/downloads_qmul_underground_reid.html for the latest benchmarking results. If you have new results using your method on this dataset, please feel free to drop me an email. I can include your results in the benchmark comparison table.

For any questions please direct to Chen Change Loy (ccloy@ie.cuhk.edu.hk)
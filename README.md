# Multiple-Alignments-Clustering

//  Created by Walfred MA in 2019, wangfei.ma@ucsf.edu.
//  Copyright © 2019 UCSF-Kwoklab. All rights reserved.

Multiple Alignments Clustering: selected most representative insertion from all overlap SVs. 



1.	Distract all SVs from their assemblies based on coordinates to a single file for all overlap SVs.



2.	Using Repeatmasker to find all masked coordinates and annotate on original file.



3.	Using Kalign to run fast multiple alignment.



4.	A cluster cycle use to cluster all SVs:

        a.-Calculate a global score for every insertion in a component based on multiple alignment results.
  
        b.-Pick the one with highest global score as the new template for new cluster. 
  
        c.-Align rest SVs to this new template and get pairwise scores. 
  
        d.-Assign SV to this cluster if it passes the cutoff for pairwise alignment score. 
  
        e.-For all SVs that do not pass the cutoff, repeat a new cycle. 


<p>
    <img src="https://github.com/WalfredMA/Multiple-Alignments-Clustering/blob/master/clustering.png" width="1000" height= auto/>
</p>


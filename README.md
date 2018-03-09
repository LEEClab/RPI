# RPI
Road Permeability Index function (RPI)
Description: 
This function aims at calculating potential fauna crossing  at road positions by estimating the chance of a taxon to cross any road position. 
It is based on qualitative, reliable expert opinion integrated with landscape attributes and road structures. 
This index can help identify potential location of road kill hotspots where no data are available. 

    Input parameters: (V, ek)
      V   matrix n x m of presence (1) and absence (0) of each variable (k) in each location (l).
		    n   total number of locations (l)
		    l		each location (we use l instead of i in the function to avoid conflict with R language)
		    m		total number of variables (k)
		    k		each landscape or road variable
		    t		total number of taxa (j)
		    j		each taxon
 
      ek  dataframe with Eljk value for each location (l) x	taxon (j) x variable (k).
		
    eg.
		local	taxa	var1		var2		var3
		l1		j1		E111		E112		E113
		l2		j1		E211		E212		E213
		l1		j2		E121		E122		E123
		l2		j2		E221		E222		E223

		  Eljk  represents the influence of each variable (k) on each taxon (j) in a location (l).
              E value is assigned by experts as positive (1), indifferent (0) or negative (-1).
              NA is used when variable is not present in the location.

      Output: List of 3
          $ RPI_i: 	a vector with average value of RPI for all taxa	in each location.
          $ RPI_ij: a matrix with RPI value for each taxon at each location.
          $ w_kj: 	a matrix with the average E value for each variable (k) and taxon (j) considering the locations k where is present.


This repository provides the R code and sample input for calculating thr Road Permeability Index. This files are supplementary material for the article:
Assis JC, Giacominni H, Ribeiro MC (in preparation) Road Permeability Index: evaluating the heterogeneous permeability of roads for wildlife crossing.

No rights are reserved anywhere in the world. Feel free to use, share, and modify.

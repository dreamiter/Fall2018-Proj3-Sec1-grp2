# Project: Can you unscramble a blurry image? 
![image](figs/Comparison4Pic.png)

### [Full Project Description](doc/project3_desc.md)

Term: Fall 2018

+ Team #2
+ Team members
	+ Jannie Chen (mc4398)
	+ Shilin Li   (sl4261)
	+ Yiding Xie  (yx2443)
	+ Yang Xing   (yx2416)
	+ Zhibo Zhou  (zz2520)

+ Project summary: In this project, we created and improved the regression engines to enhance the resolution of images. The train set includes 1500 images of high resolution and low resolution, respectively. At first, we improved the baseline model (GBM) by varying the depth from 1 to 11 and we determined 11 to be the optimal depth to use. The training time of baseline model is more than 6 hours. The test time of baseline model is around 53 minutes. Then, we applied the XGBoost model to get higher resolution. The training time and test time of XGBoost model are around 4 minutes and 35 seconds each. 

+ Models used:
	+ Baseline: GBM
	+ Improved: XGBoost

+ Feature extraction:
	+ ![image](figs/featmat_calc.png)
	+ ![image](figs/labmat_calc.png)
	+ ![image](figs/Feature%20Extraction.png)
+ FeatMat: Instead of using for loops, we instead defined a particular direction, and then we tried to find a neighbor in that direction for every point in the whole matrix and subtracted that value from the corresponding center point. For example, in picture above, if the middle point is 5, then the value in its upper left direction should be 1-5. if the middle point is 6, then it should be 2-6.  We could then move the matrix to the opposite direction, which is lower right. After calculating (the new matrix – the original matrix), we could get the values from the upper left direction. We applied the similar idea 8 more times and get the featmat.

+ LabMat: 


**Model Comparison**
![image](figs/Comparison_Complete.png)
Picture above shows the comparison in running time between the different models we utilized. 
	
**Contribution statement**: ([default](doc/a_note_on_contributions.md)) All team members contributed equally in all stages of this project. All team members approve our work presented in this GitHub repository including this contributions statement. 

Following [suggestions](http://nicercode.github.io/blog/2013-04-05-projects/) by [RICH FITZJOHN](http://nicercode.github.io/about/#Team) (@richfitz). This folder is orgarnized as follows.

```
proj/
├── lib/
├── data/
├── doc/
├── figs/
└── output/
```

Please see each subfolder for a README file.

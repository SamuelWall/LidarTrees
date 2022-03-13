## Lidar Trees
### All code can be found within the Jupyter Notebook file [here](Lidar_Depth2.ipynb)
Research Poster from the CCNY ORCA Symposium can be viewed [here](Orca Poster.pdf)
Renders can be found [here](https://drive.google.com/drive/folders/1Xu9fa5HYFKRKH1WIIbnasEz7e1svVwG-?usp=sharing)

Research in this repository is by Samuel Wolnerman, with mentorship and guidance from Professor Michael Grossberg and Professor Nicholas Steiner

Over the past 3 semesters of my studies, I have been studying machine learning and data analysis with 
Professor Michael Grossberg and gaining a solid understanding for how research works in academia. 
After some work in computational fluid dynamics, our research was pivoted to using machine 
learning to help with climate change. The main goal of this research is to develop an algorithm 
instituting machine learning to estimate biomass and carbon levels of forests through video. 
These measurements are important as biomass relates directly with carbon percentage stored in 
trees, giving insight into the environmental impact a forest has on the local and global 
environment. Ordinarily, biomass of forests is estimated through tedious measurements of 
individual trees with measuring tapes and approximating the entire forest using a smaller sample 
size. By developing a way to autonomize these measurements, we hope to expediate the process 
of forest sampling while trying to improve the accuracy of the measurements taken. Some 
research questions that we will consider are the accuracy of standard RGB images against RGB-D images in estimating these values, how different machine learning models to be used and trained compare to other ways of taking measurements, and the capability of an algorithm trained 
on artificial images to classify real world images

The current approach to this algorithm consists of taking an input RGB image, segmenting it with a form of Scipy's SLIC algorithm, classifying the respective segments as a part of a trunk or not, combing segments that consist of the same trunk (superpixels) and measuring the width of these segments using either real depth measurements via LIDAR images (RGB-D) or artificial depth measurements made by a machine learning algorithm.

### Pipeline of Algorithm Simplified
***Input Image &#8594; SLIC Segmentation &#8594; Classification of Trunks &#8594; Combination of Superpixels &#8594; Measurement of Trunk Width***

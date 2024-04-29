# kMeans-GeneticAlgorithm
An image segmentation project using k-means algorithm to segment pictures, and improving the segmentation by using a genetic algorithm metaheuristic approach to output the best centroids.

## Part 1: Vanilla k-Means Segmentation
- Just using openCV library to perform this task with k = 2, as I wanted to only segment the image into 2 parts
  
## Part 2: Finding Optimal Centroids using Genetic Algorithm (GA) approach
You need 2 functions for this:

- Objective Function
It is just one iteration of K-means which returns the sum all distances between each data point and their corresponding centroids.

- Fitness Function
It returns the inverse of the value of the objective function, since GA is for solving maximizing problems.

## Evaluation Part:
Parts 1 & 2 are evaluated using Peak Signal to Noise Ratio (PSNR) compared to the ground-truth (GT) image as its evaluation metrics.
Morpholical Operations are also done after each respective part:
- Erosion
- Dilation
- Opening
- Closing\n
These operations are also evaluated using PSNR to see if they improve the segmentation results.

# Conclusion
The result obtained from applying K-means clustering method to the coins image is quite decent.
Vanilla k-Means: 65.20 dB. 
After the morphological operations:
- Erosion: 59.65 dB
- Dilation: 59.52 dB
- Opening: 59.65 dB
- Closing: 59.52 dB
 None of which improved the results.

After obtaining the GA solution centroids: 70.46dB, which is quite a big improvement, 
it is also visually more segmented.
After the morphological operations:
- Erosion: 60.62 dB
- Dilation: 59.13 dB
- Opening: 65.51 dB
- Closing: 66.81 dB
Also did not improve the PSNR score.

Thank you for visiting this repository, you can try it out for yourself and have fun with it! :) 

### Flowchart of Genetic Algorithm:
![GA Flowchart](https://github.com/s7eady/kMeans-GeneticAlgorithm/assets/152954536/7e8e034b-32d6-4a00-aebd-5b69e97b4bb2)

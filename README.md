# ChannelShiftAnalysis
This is code to analyze the movement of channels in a timelapse image sequence

Our lab developed a method of shifting channels through the surrounding PDMS matrix. Analysis of the channel movement had involved a significant amount of manual work and lack of reproducibility given the small amount of measurements able to be performed on our large datasets. This Python script was developed to improve the accuracy of the results and to enable analyses not possible with single point manual measurements. 

We start with images of the three microfluidic channels as shown below. 
![Image of channels](https://github.com/brubaked/ChannelShiftAnalysis/blob/master/images/trichannelshift%20(1).png)

The images are thresholded into binary (pixel values are 1 or 0) black and white images shown below.
![Thresholded Image](https://raw.githubusercontent.com/brubaked/ChannelShiftAnalysis/master/images/images0000.png)

The thresholded images are converted into skeletonized images, highlighting the channel edges in the process. 
![Skeletonized Image](https://raw.githubusercontent.com/brubaked/ChannelShiftAnalysis/master/images/SkeletonizedImage.PNG)

The edges from the skeletonized images are then extracted into an array that can be easily analysed. 

Overlaying edges from multiple timelapse images results in the following plot:
![Raw Channel Edges](https://raw.githubusercontent.com/brubaked/ChannelShiftAnalysis/master/images/ChannelEdges.png)

Using a known stable location along the channels, shifting of the channels along the y-axis can be readily corrected. 
![Aligned Edges](https://raw.githubusercontent.com/brubaked/ChannelShiftAnalysis/master/images/AlignedEdges.png)

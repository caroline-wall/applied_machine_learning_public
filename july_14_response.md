# July 14, 2020 Response

1. The first filter transformed the image by diminishing the details:
<img width="314" alt="image" src="https://user-images.githubusercontent.com/67920492/87839014-05a35b80-c867-11ea-978e-59e24523ba55.png">

The second filter transformed the image by emphasizing vertical lines:
<img width="300" alt="image" src="https://user-images.githubusercontent.com/67920492/87839067-3a171780-c867-11ea-99f8-11cc0bb88f79.png">

Finally, the third filter transformed the image by emphasizing horizontal lines:
<img width="295" alt="image" src="https://user-images.githubusercontent.com/67920492/87839123-6b8fe300-c867-11ea-9d45-135c5c1f5066.png">

A convolution works by taking an array (the filter) that corresponds to a set of pixels in the image. The array is the same size as the central pixel and all of its neighbors (so usually 3x3). The value of each pixel in this set of the current image is multipled by the corresponding value in the filter array. Those values are then added together to create the new pixel value for the central pixel. This new value should be in the same range as the original pixel value, otherwise a weight needs to be applied. This process is iterated over each pixel until the entire image has been transformed. Applying a convolving filter to an image is useful for computer vision because it can highlight the pertinent parts of the image and diminish the rest. Therefore, the model is only taking in the raw features of each image, so it'll be more likely to recognize those aspects in the testing data. Different values in the filter array provide different transformations over the image, so you can determine which one is most appropriate for the task at hand.


2. Pooling was applied to the convolved image:
<img width="297" alt="image" src="https://user-images.githubusercontent.com/67920492/87840439-adbc2300-c86d-11ea-880a-6d862b38f89a.png">

In applying this filter, I have minimized the image by only extracting the largest pixel values as a way of detecting the features of the image. This code is applying MAX pooling, meaning that out of each chunk (4 neighbor pixels) of pixels the code pulls out as it moves through the image, it selects the pixel with the highest value to become a pixel in the new, transformed image. This is seen in the code snipet because the values appended to the list pixels are sorted in reverse order, or descending, and from that last, the first pixel value is selected, which would be the largest value. This decreases the size of the image, as for every four pixels, only one is found in the new image. For my pooling, I used the image that was convolved to emphasize vertical lines. Therefore, my final image resulted in a smaller image in which the vertical lines stood out even more. This is why pooling is useful; it gets rid of some of the unecessary background, making the image smaller and more centered around important features.


3. Yes, the accuracy of the model increased after applying the convolutions and pooling, going from an accuracy of 97 to 98. However, the model also took much longer to run. 

Here are the convolutions for the number 9:
<img width="407" alt="image" src="https://user-images.githubusercontent.com/67920492/87840887-f1b02780-c86f-11ea-81fe-0ce4566735f8.png">

As you can see, the convolutions are trying to pull out the different features of the nine, notably the tail and the circle. The pixels of those important features are then amplified as a result of pooling, as the size of the image decreases. These convolutions seem to be focusing on the higher circle and the tail as an indication that this is a nine, as the top of the circle and the bottom of the tail are what have been pulled out in the final convolutions.

Using 32 and 16 made just slightly less accurate models, yet the training time was also slightly diminished. Additionally, adding more convolutional layers had the opposite effect, increasing both the accuracy of the model and the training time.

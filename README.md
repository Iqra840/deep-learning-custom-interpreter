# deep-learning-custom-interpreter
A custom built tool that shows what parts of a picture are most critical when making classifications.
The data I used is a stock video of a day's timelapse, and I parsed the video into frames and categorized them into recongizeable times of the day (sunrise, sunset, afternoon, night). A standard machine learning model then makes predictions.

The deep learning interpretor comes into play when we want to find out how the system identified the critical areas of the picture that led to the label it was assigned when categorizing. We take a sample picture, and cover it with a black square thats 1/10th of the picture's total area. By sliding the box around on all parts of the picture and calculating the probability difference after every shift in the black square, we can generate a heatmap of sorts that can tell us what areas are the most crucial in the picture when finding out what time of the day it is.

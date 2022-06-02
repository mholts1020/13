# 13

# Venture Funding with Machine Learning

In this project we try to use our Machine Learning abilities to see if we can create a model that can correctly predict whether a startup is likely to succeed based on training a model with previous startup data. This could be a very useful tool for venture capital funds or angel investors.

---

## Technologies

The following technologies were used to build and deploy this application:

* Python - Version 3.9.7
* Anaconda (Which includes Jupyter Lab and Pandas)
* Path (from pathlib)
* TensorFlow
* sklearn
* NumPy
* Seaborn

---

## Installation and Usage Guide

### Using Google Colab

In this project, we used Google Colab instead of using our traditional IDEs or Jupyter Lab, Google Colab is very similar to a Jupyter Notebook but does not require us to install libraries and dependencies on our local machine but rather install and import them directly onto the platform. The platform comes with many preinstalled libraries so it is only necessary to install some as you can see on the code.

For more information about using Google Colab:
 * [Google Colab](https://colab.research.google.com/?utm_source=scs-index "Google Colab")


### 3. Downloading the Venture Funding with Machine Learning

Navigate to your desired location where you would like to save the documents for this application. You can do this by using the ```cd``` command followed by a space and the file path inside quotations ```" file path "```. In my example I have gone to Desktop.

![image](https://user-images.githubusercontent.com/94983278/149385012-181d1769-0af6-487e-8e04-823a28f2c3ed.png)

Clone this project's repository from GitHub using the following link

```https://github.com/epocaterrasus/VentureFundingUsingMachineLearning.git```

### 4. Opening the notebook

For information about opening the notebook on Google Colab, please visit the following link:
* [Opening Notebooks - Google Colab](https://developers.google.com/earth-engine/guides/python_install-colab "Opening Notebooks - Google Colab")

---


## Results and Images

For this exercise I did four models, my original model along with three alternative models, trying to increase the accuracy and reduce the loss.

### Original Model 

* Total Hidden Layers: 1
* Total Hidden Nodes for Layer 1: 9
* Total Hidden Nodes for Layer 2: 6
* Activation Function: linear
* Loss: binary_crossentropy
* Epochs: 50
* Loss: 0.6261879801750183
* Accuracy: 0.7320116758346558

### Alternative Model 1 

* Total Hidden Layers: 1
* Total Hidden Nodes for Layer 1: 20 (Just one hidden layer)
* Activation Function: linear
* Loss: binary_crossentropy
* Epochs: 100
* Loss: 0.6917281746864319
* Accuracy: 0.7329446077346802

### Alternative Model 2

* Total Hidden Layers: 1
* Total Hidden Nodes for Layer 1: 15
* Total Hidden Nodes for Layer 2: 10
* Total Hidden Nodes for Layer 3: 5
* Activation Function: sigmoid
* Loss: binary_crossentropy
* Epochs: 100
* Loss: 0.556820273399353
* Accuracy: 0.7294460535049438

### Alternative Model 3

* Total Hidden Layers: 6
* Total Hidden Nodes for Layer 1: 12
* Total Hidden Nodes for Layer 2: 9
* Total Hidden Nodes for Layer 3: 6
* Activation Function: sigmoid
* Loss: binary_crossentropy
* Epochs: 150
* Loss: 0.5537480115890503
* Accuracy: 0.7306122183799744

For this last model I tried using some tools to better select my parameters to train the model. First, I created and plotted (using Seaborn) a correlation matrix to see if there were any variables with little correlation that could be removed. Using this method I did not gain much insight and decided to try other methods. I then tried using Variance Threshold and K Best models to have my data "cleaned" using machine learning techniques, however I was getting poorer efficiency using these method than with simpler methods. I believe this was happening because my dataset dosen't have enough parameters for these tools to be really useful.

* Correlation
![image](https://user-images.githubusercontent.com/94983278/160289646-47d15a38-daee-4bed-83a2-3f2ef2ad82cb.png)

* Other methods I tried to use
![image](https://user-images.githubusercontent.com/94983278/160289686-7f078e95-ac1f-4908-9408-134d7c76e623.png)


As you can see our best performing model was the simplest (Alternative Model 2), using just one hidden layer and 1 hidden node.



## Contributors
Maxwell Snyder
---

## License

MIT License

Copyright (c) 2022 mholts1020

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.

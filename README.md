# NST, using AI to create art
NST was first introduced in 2015 [paper](https://arxiv.org/abs/1508.06576) it took advantage of how convolution neural network works, The system uses neural representations to separate and recombine content and style of arbitrary images. In simple words, it transfer the style from one image to another and their weights. The results vary depending on style image and the content image. In this notebook, it is designed in a way where you can easily use the Neural Style transfer with your own images with minimum adjustments.
# literature review

![VGG19](https://raw.githubusercontent.com/MightyStud/NST-AI-to-create-art/main/diagrams/VGGNet-architecture-19-edited.png)
Using VGG19 network with pretrained weights excluding the top fully connected layers, usually for training purposes the weights of different layers are adjusting to minimize the loss function, however in NST, all the layers are frozen(not changed) except the input layer which in that case is the generated image.

The generated image is free to change its values to minimize the loss function.

How does the loss function look like in this case, you might ask? The loss function is combination of the content image loss and style image loss. The content loss compares the original image with the generated image for every convoloution layer. The style loss, on the other hand, uses the gram matrix to compare the style loss and the generated image loss.

More details are explained in the reserch paper.

# results:
The results will vary dramatically depending on the parameters you use, you can think of this as a filter for your images but with AI help rather than tools like photoshop.
![github image of result](https://github.com/MightyStud/NST-AI-to-create-art/blob/main/diagrams/0875.jpg?raw=true)

![github image of result 2](https://raw.githubusercontent.com/MightyStud/NST-AI-to-create-art/main/diagrams/showcase.png)

[Timelapse video on youtube](https://youtu.be/ERyrYhHjTNU)


# References and heavy influencers:
+ [A Neural Algorithm of Artistic Style (paper)](https://arxiv.org/abs/1508.06576)
+ [Image Style Transfer Using Convolutional Neural Networks (paper)](https://ieeexplore.ieee.org/document/7780634)
+ [Real-Time Neural Style Transfer for Videos (paper)(feedforward approach)](https://ieeexplore.ieee.org/document/8100228)
+ [TheAIEpiphany youtube channel](https://www.youtube.com/c/TheAIEpiphany)
+ [gordicaleksa's repo](https://github.com/gordicaleksa/pytorch-neural-style-transfer)
+ [Aladdin Persson youtube video](https://www.youtube.com/watch?v=imX4kSKDY7s&t=1236s)
+ [Tensorflow NST tutorial](https://www.tensorflow.org/tutorials/generative/style_transfer#total_variation_loss)

# TextFromImage

visit: https://laconicml.com/ for FREE AI tutorials

This repository contains .zip file named text_from_image.
In the zip file, you can find few pictures that I used for testing my model, and a folder called data, that contains the training data.
There are also two .py files, problem, which contains the training of the model and text_creator that forms words from letters.
The main goal of my unfinished problem, was to be able to read text directly form picture.
There are already libraries that make this possible, but i wanted to try somenthing on my own.
The main idea behind the solution is that computer can learn the letters based on their contours.
I use Random forest classifier form the Scikit-learn library that classifies the contours of the images containing the letter.
I take the contours using functions from opencv-python library.
The classifier is learning the average value of the contour and classifies it in the right class.
When we want to test the model, we just gave an image to it, and it finds all contorus on the image. For each of them, the model will find the
closest contour form the training data and than predict for that contour.
The model can work with images that contain text font around 72. 
The model doesn't predict with highest precision because the functions from the opencv-python that determines the closest contorus are not 
very precise in doing that. However it works nice for words that doesn't contain letters I and C.
In the text_creator, I use dictionary of all words in order to create one from the letters I get as a result of the prediction. It creates the
word using probability.

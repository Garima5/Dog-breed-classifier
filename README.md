# Dog-breed-classifier
Udacity - deep learning project 2 - dog breed classifier

# Summary
Create an application where user supplies images. If a dog is detected in the image, the model gives the nearest detected dog breed. If a human is detected, the model gives the nearest resembling dog breed to that human face.

# Steps
<ul>
  <li>Step 0: Import Datasets</li>
  <li>Step 1: Detect Humans</li>
<li>Step 2: Detect Dogs</li>
<li>Step 3: Create a CNN to Classify Dog Breeds (from Scratch)</li>
<li>Step 4: Create a CNN to Classify Dog Breeds (using Transfer Learning)</li>
<li>Step 5: Write the Algorithm</li>
<li>Step 6: Test the Algorithm</li>
</ul>

# Libraries Used
<ul>
  <li>Numpy </li>
  <li>glob : Use Unix shell rules to find filenames matching a pattern.</li>
  <li>Pytorch </li>
  <li>Opencv</li>
  <li>matplotlib</li>
  
  </ul>
  
 ## Step 0
 Load data using glob and numpy
 
 ## Step 1 - Detecting human faces
<p> Use OpenCV's implementation of Haar feature-based cascade classifiers to detect human faces in images.
  <br> Before using any of the face detectors, it is standard procedure to convert the images to grayscale. The detectMultiScale function executes the classifier stored in face_cascade and takes the grayscale image as a parameter.
In the above code, faces is a numpy array of detected faces, where each row corresponds to a detected face. Each detected face is a 1D array with four entries that specifies the bounding box of the detected face. The first two entries in the array (extracted in the above code as x and y) specify the horizontal and vertical positions of the top left corner of the bounding box. The last two entries in the array (extracted here as w and h) specify the width and height of the box.
</p>

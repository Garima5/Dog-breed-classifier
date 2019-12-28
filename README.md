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
  <li>PIL - The Python Imaging Library adds image processing capabilities to your Python interpreter.</li>
  
  </ul>
  
 ## Step 0
 Load data using glob and numpy
 
 ## Step 1 - Detecting human faces
<p> Use OpenCV's implementation of Haar feature-based cascade classifiers to detect human faces in images.</p>

### Important points to keep in mind
 <ol>
  <li>Before using any of the face detectors, it is standard procedure to convert the images to grayscale.</li>
  <li>In the code, faces is a numpy array of detected faces, where each row corresponds to a detected face. Each detected face is a 1D array with four entries that specifies the bounding box of the detected face. The first two entries in the array (extracted in the above code as x and y) specify the horizontal and vertical positions of the top left corner of the bounding box. The last two entries in the array (extracted here as w and h) specify the width and height of the box.</li>
  </ol>
  
## Step 2 - Detecting dogs
 Using transforms from Pytorch's functionalities and transfer learning trough VGG16 model, find if a dog is detected in the image or not. The function gives the index that has the probability among all the classes. Since the indexes between 151 and 268 correspond to dog breeds, hence if the maximum index returned follows in this range, the images contains a dog.

## Step 3 - reate a CNN to Classify Dog Breeds (from Scratch)
Code a convulation neural network to classify dog breeds from scratch.

### Challenges undertaken to create the CNN from scratch to classify dog breed classifier
 <ol>
  <li>Code a CNN from scratch, without using transfer learning and must attain a test accuracy of at least 10%</li>
  <li>The task of assigning breed to dogs from images is considered exceptionally challenging. To illustrate, consider that even a human would have trouble distinguishing between a Brittany and a Welsh Springer Spaniel.</li>
<li>Similarly, labradors come in yellow, chocolate, and black. My algorithm will have to conquer this high intra-class variation to determine how to classify all of these different shades as the same breed.</li>
</ol>

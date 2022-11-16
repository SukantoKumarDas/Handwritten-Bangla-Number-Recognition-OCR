# Handwritten Bangla Number Recognition
**Our Approach**:
1. Build a digit (০-৯) classifier using a CNN architecture.
2. Apply character segmentation for the handwritten number image.
3. Classify each segmented digit and then get the final number in the image.

**Dataset** : We used Ekush dataset which contains bangla digit images.

**Total Number of image Data** : 30,687<br>
**Mean Number of image Data per digit** : 3068<br>
**Number of Training Data** : 24546 (80%)<br>
**Number of Validation Data** : 6141 (20%)<br>
**Input Image Dimension** : 32x32 pixel<br>

**Model Description** :<br>

We are using the CNN sequential model. In a total of three layers we use filters of size  32 , 64 and 128 sequentially. And we use a kernel of fixed size 3x3 in each case. We perform two max-pooling operations in between. After flattening 512 nodes gets generated which then mapped against 128 nodes in the dense layer . Finally the model outputs 10 classes each representing bengali digits from ০ to ৯ .  <br>

**Segmentation** :<br>

Firstly we convert the input image to grayscale. Then images of individual digits are separated and forwarded to the digit recognizer. Finally, predicted individual digits are assembled together to form the corresponding number.<br>

**Limitations** :<br>
1. The digit recognition system can not segment multiple numbers in a single image.<br>
2. It can not detect number with other characters correctly( ‘’১১-১২’’, “৫,৫৫০”).<br>



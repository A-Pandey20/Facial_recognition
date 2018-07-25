# Facial_recognition
The code trains a network to find the dissimilarity between two images using CNN which can be used for facial recognition and detection. This is implemented using pytorch. 
The trainig data should be in data folder and the data for testing in testing folder. I have trained the network using AT&T face dataset, which is easily available online. <br/>
More dataset -: https://www.microsoft.com/en-us/research/project/ms-celeb-1m-challenge-recognizing-one-million-celebrities-real-world/ <br/>
https://drive.google.com/file/d/0B5MzpY9kBtDVZ2RpVDYwWmxoSUk - Link of a pretrained model for facial dissimilarity. <br/>
How to use a pre-trained model for our use case. Here are the steps.<br/>
Collect the images of all employees.<br/>
Align the faces using MTCNN (Multi-task Cascaded Convolutional Neural Networks), dlib or Opencv. These methods identify, detect and align the faces by making eyes and bottom lip appear in the same location on each image.<br/>
Use the pre-trained facenet model to represent (or embed) the faces of all employees on a 128-dimensional unit hyper sphere.<br/>
Store the embeddings with respective employee names on disc.<br/>

# DeepLearning-Final-Project

In this project, you will use features from off-the-shelf pre-trained CNNs to classify different
types of food. You will then learn to fine-tune your own CNN for classification. To learn more
about using CNN features and fine-tuning, please read the papers [1, 2],the Caffe guide [3] and
the explanation on transfer learning from Stanford cs231 [4]. You will be using the Food-101
dataset [5], which has 101 food categories. Each category has 1000 images, 750 for training
and 250 for testing. Training images contain some noise from intense colours and sometimes
wrong labels; test images are clean and manually reviewed.

Tasks For each of the following tasks, select randomly 3 subsets of 10 and 2 subsets of
30 classes and use the same splits for all the experiments. Report the average classification
accuracy over the 3 random splits of 10 classes as well as the 2 random splits of 30 classes.
For each task, plot the confusion matrix for one of the 3 random splits consisting of 10 classes
and report the classification accuracy for each class individually; use the same split for plotting
the confusion matrix for the tasks as well. Finally, compute the classification accuracies with
training and testing on all of the 101 classes. Report the top 5 classes with highest classification
accuracy and the 5 worst performing classes. Explain your results (certain classes share visual
similarity making it harder for the networks to reason and distinguish etc.).

1. Using the responses from the final fully connected layer as features, train a linear SVM
to perform classification. You can use the lib-SVM2 package which is available for both
C++ and Python. Compare the classification accuracy on the features obtained from
using off-the-shelf VGG-163 and ResNet-344.

2. Starting with the base VGG-16, fine tune the network to classify the same 10 and 30
splits from the previous part. Also fine tune the network to classify all the 101 classes.
Repeat the same experiment with ResNet-34.
3. In the lecture on regularization, we discussed explicit handling of incorrect ground truth
labels in the training via label smoothing regularization. In this regularization scheme,
the factor  is an estimate of how frequently you expect the label to be incorrect. You can
find out more details about this in Section 7 of the work by Szegedy et al. [6]. Incorporate
label smoothing regularization into your fine-tuning scheme for both VGG and ResNet
and apply to the split considering all 101 classes. Do the classification results get better
or worse ?

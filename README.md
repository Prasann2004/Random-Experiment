# Random-Experiment
[Notebook Of Experiment](https://www.kaggle.com/code/newtonbaba12345/random-experiment-data)
[Dataset](https://www.kaggle.com/datasets/newtonbaba12345/random-exp-data)

This weekend I had nothing much to do and did not knew what to do. So I decided to do some random experiment with weights of simple neural network. I bacsicly trained two NN to classify 3 classes : 0,1 and 2. First model was trained on data containing 0 and 1 class only with just one class of 2.Second model was trained on data containing 0 and 2 class only with just one class of 1. Then I tried to combine the weights to improve the performance of the model .

**w_0and1 :** weight model that was trained on data containing 0 and 1 class.

**w_0and2 :** weight model that was trained on data containing 0 and 2 class.

**w :** combined model weight.


Results :
-  **w = alpha*w_(0and1) + (1-\alpha)*w_(0and2)** :
-  
![](https://www.googleapis.com/download/storage/v1/b/kaggle-forum-message-attachments/o/inbox%2F13602048%2F0b1492a217562c83dd405d7a0fc50ae0%2Foutput.png?generation=1711308726207012&alt=media)

Clearly combining model in such a way was not a good idea as the accuracy droped significantly.

- **w = alpha*(w_(0and1))^2 + (1-\alpha)*(w_(0and2))^2** :
- 
![](https://www.googleapis.com/download/storage/v1/b/kaggle-forum-message-attachments/o/inbox%2F13602048%2Fe256c6c4e7c74d070e39fc90a075b037%2Foutput.png?generation=1711308937079103&alt=media)

Again I got terrible results 🥲.

- **w =( (w_0and1)^n+(w_0and2)^n)/2** :
- 
![](https://www.googleapis.com/download/storage/v1/b/kaggle-forum-message-attachments/o/inbox%2F13602048%2F8652084c3f6a2e368e636169f2135b41%2Foutput.png?generation=1711308993594322&alt=media)

![](https://www.googleapis.com/download/storage/v1/b/kaggle-forum-message-attachments/o/inbox%2F13602048%2F0726ca5712219c9a2feccf7be68f4f0c%2Foutput.png?generation=1711309023071418&alt=media)

Now I got something intresting . These spikes are very much intresting and till now I have not find any reason to explain this . The pattern is that there is a spike in accuracy at **even values of n** and have **higher accuracies** as compared to nearby **odd values of n**.

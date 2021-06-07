**Bengali Handwritten Digits**

The English handwritten digit recognition is one of the most popular problems in machine learning and computer vision. This problem is solved using various techniques. In this assignment, we will classify Bengali Handwritten Digits using logistic regression.
 
Handwritten Digits classification can be used in various applications like optical character recognition, restore text from old documents, etc.
In this assignment our main goal will be to achieve a good result using logistic regression and tuning hyperparameters correctly to get a better result.
 




**Dataset**


> For this experiment, we will use the dataset [NumtaDB](https://www.kaggle.com/BengaliAI/numta/) which is available in **Kaggle**. 
There will be a total of **54908** images, and it was split in a **90:10** ratio. **90%** (**49417**) of data is used in training and **10%** (**5491**) was used in testing.

Snapshot of Dataset

> <div align="center">
<img src="https://drive.google.com/uc?id=1LvkNwV1My2RniR_JsbasBET1fa97eMQu" width="500">
</div>

**Experimental Setup**


> All of these experiments were performed using Google Colab free GPU, Models were created in PyTorch. 


During the whole experiment,
* The height and width of the input was **28*28 =784** 
* Output dimension was **(০,১,২,৩,৪,৫,৬,৭,৮,৯)=10**
* Each batch size was different if each setting
* The number of iteration was **15000**
* Different activation function was used 
* GPU **Tesla T4** was availabe
* Number of Epochs was different if each setting

- **totaldata:** 54908
  - $epochs = iterations \div \frac{totaldata}{minibatch}  $

We will use different learning rate to achieve better performance

**Result**

**Using Logistic Regression**

| Experiment Number      | Optimizer     | Learning Rate    | | Accurecy of last 500 iterations    |
| :------------- | :----------: | :-----------: || :-----------: |
|  1 |SGD   | 0.01    ||38.12  |
|  2 |SGD   | 0.02    ||  40.07 |
| 3   | SGD | 0.03 || 36.24 |
|  4 |Adam   | 0.0001    ||35.95 |
|  5 |Adam  | 0.0002   || 38.72 |
|  6 |Adam   | 0.0003    || 40.23 | |



**Using Deep Neural Network**

| Experiment Number      | Optimizer     | Learning Rate     |  Num of Hidden Layer   | Btach Size |Num of epoch    | |  Accurecy of last 1000 iterations    |
| :------------- | :----------: |:----------: | :-----------: | :-----------:  | :-----------: || :-----------: |
|  1 |SGD   | 0.09 | 4| 128 | 38   ||72.93  |
|  2 |SGD   | 0.5 | 4| 256 | 77   ||77.52  |
|  3 |SGD   | 0.11 | 4| 128 | 38   ||76.12  |
|  4 |SGD   | 0.04 | 4| 512 | 155   ||80.84  |






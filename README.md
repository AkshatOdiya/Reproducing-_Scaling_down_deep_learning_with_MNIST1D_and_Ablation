# Reproducing-_Scaling_down_deep_learning_with_MNIST1D_and_Ablation

This Repository contains an attempt to reproduce the paper along with ablation in Effective areas.
All the iteration are done in google colab. And the notebooks can be used as it is wihtout any change if run in colab.

1. Prep: Folder contains the original paper along with the proposal sent for Recruitment.
   
2. Reproducing_the_paper: Contains a notebook combined for all the experiments which were thought of being significant according to the paper. The author has also done experiments under "Benchmark pooling", which is not included in this notebook.

Ablation study was much interesting part;

Whatever done under ablation, graphs are also plotted to study the effect of changing parameters on losses(mainly).


# 1. Ablation under Deep Double Descent:
   # Explanations are also given in the notebook itself under concerned cell.
   i) This notebook Contains different study files and the titles are given itself under each ablation.
   
   ii) Effect of hidden layers: Tests the effect of numbers of hidden layers on Classification Error. And the graph is plotted below to clearly show the effect.
   
   iii) Effect of label noise: Iterates through values for noise to be introduced in Testing dataset for study and a graph to show the effect.
   
   iv) Dropout: To study if any regularization is required, but the graph shows something else(explanation is given under cell).
   
   v) Effect of hidden layer sizes: Itreates through different values of hidden layer sizes and plotting the graph to study the effect.
   
   vi) An attempt is also made to study the effect of changing the parameters altogether, parameters include hidden layer sizes, number of layers, noise levels, dropout rate. It is difficult to plot the effect altoghter, but a heat map is plotted that shows the effect of changing dropout rate and noise on test error. The results are also stored in pickle file, and can be used to plot other graphs.
   

# 2. Ablation under Meta-learning Rate,Learning Rate:
   i) Effect of changing initial learning rates.
   
   ii) Effect of changing Hidden layer sizes.
   
   iii) Effect of changing meta-leanrning rate.
   
   Some explanations are given in the notebook itself and graph plots.
   

# 3. Ablation under Meta-learning Rate,Activation Function:
   The studies are done in different notebooks for each changing parameter due to problem with colab Memory allocations and Runtime.
   1. Hidden sizes(hs): Includes changing the hidden layers sizes([100,200,500]; It is depicted in notebook names too that which notebook inlcude which layer size and same for pickle files). A notebook is also there that combined the results(stored in pickle files) and plotting the effect with different sizes. Other Graphs also Obserbvable in the notebooks(excluding combined one).
   2. Changing Rate of momentum(mu): The notebooks for different mu is written under name of file like [mu3:mu=0.3] [mu5:mu=0.5] and so on, but different for one notebook [mu1one:mu=1] and same for pickle files too. A combined notebook(muCombined) is also there that combines the results and a graph to understand the difference in using different mu. Other Graphs also Obserbvable in the notebooks(excluding combined one).
   3. Noise: Removing the line that introduces the noise, not much effect is observable.
      

# 4. Ablation under lottery ticket & spatial inductive biases:
   The explanation is given where it is required otherwise graphs are enough to understand the effect and study.
   Includes:
   1. changing hyperparameter(learning rate),
   2. Perturbation(noise injecting, label permutation, input cropping), explanation about these terms are given in the notebook itself.
   3. Using Exponential sparsity schedule instead of linear schedule.
   4. Introducing xavier initialization in the model.


All the pickle files are uploaded here: https://drive.google.com/drive/folders/1KbNnp8C7aheVsfqr6vg7_Bhqam23j8d9?usp=sharing
   

Tips:

* As SIRR utilizes DDN as the supervised part, we deactivate the items corresponding to unsupervised part in loss function and regard the predicted results 
as the recovery results of DDN. More importantly, it is quite necessary to adjust the parameter "factor" according to the scale of rain streaks when using the function "Network.inference" to test samples. 

* The code styles of RESCAN and SPANet are almost the same. Before training/testing  your own samples, you need to concat the groundtruth/rainy image and the corresponding rainy image. 

* For JORDER_E, as released in github, in the training stage, the authors also do an evaluation and choose the best model as the final trained model where the evaluation result on synthetic datasets
has the best PSNR. However, in this case, its generalization performance is hardly competitive. For simplicity, we directly select the latest model as the pretrained model. 
 
* We expect that these pretrained models would facilitate you in performance comparison of current rain removal methods. Besides, maybe it is necessary for you to adjust the corresponding hyper-parameters in accordance with your research motivation.
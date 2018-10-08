# Predicting Future Instance Segmentation by Forecasting Convolutional Features
### Pauline Luc, Camille Couprie, Yann LeCun and Jakob Verbeek

Code to be released soon here, for our [ECCV 2018 paper](https://arxiv.org/pdf/1803.11496.pdf).

In the mean time, for ease of comparison with our work, we provide the predictions of our models on the Cityscapes [1] validation set.
- for 3 frames ahead (about 0.17s). This one is obtained by taking frames 8, 11, 14, 17 of each sequence in input and predicting frame 20. These are the predictions of the model before autoregressive finetuning, which get 40.2 AP-50.
- for 9 frames ahead (about 0.51s). This one is obtained by taking frames 2, 5, 8, 11 of each sequence in input, and predicting frames 14, 17, 20. These are the predictions of the autoregressively finetuned model, which get 19.4 AP-50% and 41.2 mIOU over the moving classes. The second result is obtained by converting the instance segmentations to semantic segmentations using the simple procedure we describe in the paper, with threshold=0.5. We have also used this threshold for all our visualizations.

Also, take a look at our qualitative results on the [project website](http://thoth.inrialpes.fr/people/pluc/instpred2018) !

*[1] Cordts, M., Omran, M., Ramos, S., Rehfeld, T., Enzweiler, M., Benenson, R., Franke, U., Roth, S., Schiele, B.: The Cityscapes dataset for semantic urban scene understanding. CVPR 2016*

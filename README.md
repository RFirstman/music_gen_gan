# Music-generation-RNN-GAN

## c-RNN-GAN
The repository contains the original code for C-RNN-GAN by Olof Mogren forked from the repository https://github.com/olofmogren/c-rnn-gan/
The code is ported from its original implementation on an older version of tensorflow to the latest version of tensorflow 1.4.

## How to run?

An example command to run the model (NOTE: make sure to specify `datadir` and `traindir` appropriately)
'''
python rnn_gan.py  --datadir "relative-path-to-data" --traindir "path-to-generated-output" --feed_previous --feature_matching --bidirectional_d --learning_rate 0.1 --pretraining_epochs 6 
'''

In case you wish to run the models again, either use a different name for the traindir of remove the one generated by previous run.

## Sample Output

Samples of generated data can be found in the `train`, `train_large`, and `train_large_discriminator` directory.

The `train` directory contains results from a small model trained over 6 epochs. The `train_large` directory
contains results from a large model trained over 126 epochs. The `train_large_discriminator` contains results from
a similar model to `train_large` except for a larger discriminator model (500 hidden units, 3 layer LSTM cells)
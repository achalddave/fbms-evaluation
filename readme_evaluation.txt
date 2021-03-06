Linux 64bit binaries and code for the evaluation on the 

      Freiburg Berkeley Motion Segmentation dataset

as proposed in the paper

==================================================================
||  Segmentation of moving objects by long term video analysis  ||
==================================================================


Copyright (c) 2013 Peter Ochs

__________________________________________________________________

Terms of use
__________________________________________________________________

This program is provided for research purposes only. Any commercial
use is prohibited. If you are interested in a commercial use, please 
contact the copyright holder. 

If you used this program in your research work, you should cite the 
following publication:

Peter Ochs, Jitendra Malik, Thomas Brox 
Segmentation of moving objects by long term video analysis
IEEE Transactions on Pattern Analysis and Machine Intelligence, preprint, 2013. 

This program is distributed WITHOUT ANY WARRANTY.

__________________________________________________________________

Usage Evaluation binaries for the 
Freiburg Berkeley Motion Segmentation Dataset (FBMS)
__________________________________________________________________

YOU MUST RUN YOUR METHOD ON ALL SEQUENCES USING EXACTLY THE SAME
CODE AND PARAMETERS. 

Usage: 
------

./MoSegEvalAll allShots.txt all allTracksFileList.txt threshold


allShots.txt 
is a txt file containing the number of sequences 
to be evaluated and the references to the files defining the 
evaluation for a sequence. 
See allShotsTrainingSet.txt or allShotsTestSet.txt for details.

all 
specifies that the complete sequences are considered.

allTracksFileList.txt
is a txt file containing the references to the track-files 
generated by your method. 
See eval_test_all or eval_training_all for an automatic 
generation and evaluation for the training and test set.

threshold (default: 0.75)
specifies a value for an object specific F-measure to be 
accepted and counted as an object, i.e., objects with 
F-measure higher than threshold increase the number of object counter.
For your final evaluation you should use the default value 0.75.


The evaluation code provides a result file for each sequence and
evaluation length in the directory of your trajectory file. 
Additionally it provides a summary for all sequences in the main
directory. Refer to the paper to learn how to interpret the 
numbers. The evaluation source code is also provided as a 
reference.


Evaluation on all sequences:
----------------------------
You can use eval_training_all or eval_test_all to evaluate your 
method on the full training or test set. Please refer to these 
files for the required arguments.

_________________________________________________________________

Links
__________________________________________________________________

The full benchmark dataset can be downloaded from: 

http://lmb.informatik.uni-freiburg.de/resources/datasets/FBMS_Trainingset.tar.gz 
http://lmb.informatik.uni-freiburg.de/resources/datasets/FBMS_Testset.tar.gz.

__________________________________________________________________

Bugs
__________________________________________________________________

Please report any bugs to Peter Ochs:    ochs@cs.uni-freiburg.de


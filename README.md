# Teacher and student Model

Based on TANG21. The basic idea is transfer learning (TL): take full advantage of old knowledge rather than train a new model from zero when getting a new similar task.

### The process is as follows:

1. Train a teacher model with the Opportunity dataset;
2. Store the teacher model and extract the optimal parameters (weights, w);
3. Load the graph and weights w in the student model;
4. Train student model with the Daphnet dataset using the weights w.


### Files Description:

1. datareader.py: read dataset
2. teacher.py: train a teacher model
3. model: contain all the information about the teacher model
4. student.py: train a student model


### How to run?

1. Download Opportunity dataset (it can be downloaded from: [https://archive.ics.uci.edu/ml/datasets/opportunity+activity+recognition]) and Daphnet Gait dataset (it can be downloaded from: [https://archive.ics.uci.edu/ml/datasets/Daphnet+Freezing+of+Gait]) and put them in the corresponding folder;
2. Run python datareader.py opp to get opportunity.h5 and run python datareader.py dap to get daphnet.h5;
3. Run python teacher.py opp using opportunity.h5 and then store all the information in the file model;
4. Run python student.py dap using daphnet.h5.




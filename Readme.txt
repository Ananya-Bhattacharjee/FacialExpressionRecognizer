
Execution order is given below. We will assume that current directory is your project folder.
Following script is for windows. For linux the python command will not contain .exe extention. Command line arguments in the same line with python command are input files. Following files are output files.
###############################################################################################################################################################
python.exe data.py .\Data\data.zip 
.\Data\Train\Best_hyperparameter_80_percent\ 
.\Data\Validation\Validation_10_percent\ 
.\Data\Test\Test_10_percent\ 
.\Data\Train\Under_10_min_training\ 
.\Data\Train\Under_90_min_tuning\ Data\Validation\3_samples\
python.exe tune.py .\Data\Train\Under_90_min_tuning\data.zip .\Data\Validation\Validation_10_percent\data.zip
.\tuning_results.txt
.\hyperparameter.txt
python.exe train.py .\Data\Train\Best_hyperparameter_80_percent\data.zip .\hyperparameter.txt
.\model.h5
python.exe test.py .\Data\Test\Test_10_percent\data.zip .\model.h5
###############################################################################################################################################################


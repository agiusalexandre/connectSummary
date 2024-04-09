# How to create Amazon connect Summary Call

## create two bucket 
1 bucket to copy your .wav file
1 bucket to receive the conversation transcript and summary of the call
Update the Jupyter Notebook accordingly

## create the lambda fonction layer
https://docs.aws.amazon.com/lambda/latest/dg/creating-deleting-layers.html

Update your os variables : 
os.environ['LEARNERS3BUCKETNAMETEXT']
os.environ['LAMBDALAYERVERSIONARN'] 
os.environ['LEARNERS3BUCKETNAMEAUDIO']

## Create a jupyter notebook
[1/ Amazon Sagemaker Studio Classic](https://docs.aws.amazon.com/sagemaker/latest/dg/notebooks.html)

## Create a dialog with your amazon connect instance
copy with the name 'dialog.wav'

## Run
Run your notebook the result will in the Result.txt file inside your ['LEARNERS3BUCKETNAMEAUDIO'] bucket
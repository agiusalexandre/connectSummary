# How to create Amazon connect Summary Call

## create two bucket 
- 1 bucket to copy your .wav file
- 1 bucket to receive the conversation transcript and summary of the call
- Create your lambda layer using the "dlai-bedrock-jinja-layer.zip" file [https://docs.aws.amazon.com/lambda/latest/dg/creating-deleting-layers.html]
- pdate the Jupyter Notebook accordingly
 
Update your os variables (GenerateAmazonConnectCallSummary.ipynb): 
- os.environ['LEARNERS3BUCKETNAMETEXT']
- os.environ['LAMBDALAYERVERSIONARN'] 
- os.environ['LEARNERS3BUCKETNAMEAUDIO']

## Create a jupyter notebook env
[1/ Amazon Sagemaker Studio Classic](https://docs.aws.amazon.com/sagemaker/latest/dg/notebooks.html)

## Create a dialog with your amazon connect instance ( or use the dialog.wav file in the repo.. )
copy with the name 'dialog.wav'

## You're ready, Run it !
Run your notebook the result will in the Result.txt file inside your ['LEARNERS3BUCKETNAMEAUDIO'] bucket

## Customization
Update your template file instruction to customize the result content !

## Integration with Amazon Connect contact Lens
- Enable Amazon connect contact Lens [https://docs.aws.amazon.com/connect/latest/adminguide/enable-analytics.html]
- Use Amazon s3 trigger to invoke your lambda function [https://docs.aws.amazon.com/lambda/latest/dg/with-s3-example.html] ( Update your jupiter NB )


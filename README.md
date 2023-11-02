# hf_textClassification
I have done Text classification using hugging face APIs using the weights of the "distilbert-base-uncased-finetuned-sst-2-english" classifier model provided by hugging face.

Basic Pipeline:
---------------
![image](https://github.com/krishnapranayangara/hf_textClassification/assets/33367492/3229af5a-6919-4f56-bb5a-09f766be8b60)

Basic Steps in Creating a Sequence Classifier:

**Step 1: Use an Autotokenizer to convert text to numerical values**
- Using the checkpoint name of the desired model helps us automatically fetch the data associated with the model’s tokenizer and cache it.
- This is how a tokenizer is initiated with a checkpoint from a pre-trained model.

**Step 2: Create a Model**
- we can create a model directly from TFAutoModel*.
- There are many models for audio classification, sequence classification, and image classification.
- These models are used to help us choose the output labels that match our output needs.

**Step 3: Convert logits to predictions**
- To get output predictions we need to convert logits to accuracy predictions.
- we use the softmax function to do this.
- There are many loss functions but the prediction values might change depending on the loss function we use.

> [!NOTE]
> [model.config.id2label] is used to display the labels being used.

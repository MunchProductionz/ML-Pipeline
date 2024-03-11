# Open Source models with Hugging Face
-
Consists of code from the introductory course on Open Source Models with Hugging Face by DeepLearning.AI: [Course](https://learn.deeplearning.ai/courses/open-source-models-hugging-face/lesson/1/introductionn)


## Concepts

- 0 NLP
- 1 Translation and Summarization
- 2 Sentence Mebeddings
- 3 Text Classification and Q/A
- 4 Zero-Shot Audio Classofication
- 5 Automatic Speech Recognition (ASR)
- 6 Text to Speech (TTS)
- 7 Object Detection
- 8 Image Segmentation
- 9 Image Retrieval
- 10 Image Captioning
- 11 Multimodel Visual Question Answering
- 12 Zero-Shot Image Classification
- 13 Deployment


## Selecting models

Rule of thumb:
- Look at the size of `pytorch_model.bin` and multiply by 1.2, and this is approximately how much memory you need to run this model.

Use the "Task" page to learn more about a specific task, what models are recommended, datasets that can be used, and demos.

When you have decided on the model, press the "Use in Transformers" to get useful code snippets to import the model.

Using a `pipeline` object, you can abstract away preprocessing of different data types, ex. handling tokens in text models, logmel spectrogram in audio models, normalization/resizing of images in imgae models.
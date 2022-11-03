# CodeSeoul - Over the Hump - ML on the Web

## artclassificationmodel.json
An example of the JSON (web format) model output from Teachable Machine. You can also get something similiar with tensorflowjs_convert when converting GraphDef (eg. Python) models to the tf.js web format.

## p5-js.html
Image file uploading and text/icon display is done by p5.js and the predictions are done by ml5.js, using the exported Teachable Machine model. You can also load the 

## js-ml5.html
An example of using only vanilla JS to get images from the webcam and passing to ml5.js with the MobileNet model (most likely defaults to V2?) for classification.

## tf.html
A recreation of the Teachable Machine with just TensorFlowj.js (tf.js), to show how it may have been all put together (minus the KNN classifier for brevity). This uses vanilla JS to get the images from the webcam and feeds the images to either the training sets or the prediction sets. Training and predictions are done using tf.js with the MobileNetV3-Small model. (Note: predictions on Teachable Machine most likely uses a KNN classifier, so as an exercise, perhaps you can rewrite this to use MediaNet to generate the logits and KNN for the predictions!)
Please note that if you are going to load the models from local files (how it is now), you'll have to use a webserver to host this so you don't run into CORS issues of loading external files on the browser. You can, however, change the code to load the model from the web (TFHub) -- this snippet can be found commented out. Loading from the web will let you run without a web server (you can just double click on the file to open on a browser, or open with a file:// URL).

## Other Notes
You can find all the 1000 classifications for the ImageNet model here: https://github.com/tensorflow/tfjs-models/blob/master/mobilenet/src/imagenet_classes.ts

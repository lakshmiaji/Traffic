# Traffic
This Repository includes a model trained on Kaggle dataset Car License Plate Detection using Faster RCNN model on Detectron2 and testing on realtime traffic videos and recognizing license plate numbers and speed of corresponding vehicles.

## Detectron2
Object detection is a computer vision technique that works to identify and locate objects within an image or video. Specifically, object detection draws bounding boxes around these detected objects, which allow us to locate where said objects are in (or how they move through) a given scene.

Detectron2 is Facebook AI Research(FAIR)'s most widely accepted open source project,which is flexible, extensible and super easy to work on. Implemented in PyTorch, consisting bundle of models like Faster R-CNN, Mask R-CNN, RetinaNet,DensePose, Cascade R-CNN, Panoptic FPN, and TensorMask performing Object detection,Semantic segmentation and Instance segmentation. Along with using these pretrained models, we could also train our own models.

Using Detectron2 in real time applications like License plate detection could bring great advancements in AI. Along with that, recognising License plate numbers and detecting speed of those vehicles could finally be a Traffic Monitoring System!

## Dataset
The dataset used for training License plate detection is from Kaggle Car License plate Detection. The original dataset consists of 433 images and their annotations in .xml format. For training using Detectron2, I converted annotations to coco format using voc2coco.py.
Train images with annotations after registering our dataset to Detectron2 library.

![1](https://user-images.githubusercontent.com/71822090/135727275-4a468039-eb6d-4cb1-af97-cbe4abe881ce.JPG)

![2](https://user-images.githubusercontent.com/71822090/135727284-970c6828-16cf-4ea6-8509-106d26c267e2.JPG)

## Model Architecture

Trained model using Faster RCNN (https://github.com/facebookresearch/detectron2/blob/main/configs/COCO-Detection/faster_rcnn_R_101_FPN_3x.yaml)
Model saved as config.yaml and weight saved as model_final.pth

![3](https://user-images.githubusercontent.com/71822090/135729875-b962842d-a192-4f4a-83c2-0fa60c2fe911.JPG)

Test images


![4](https://user-images.githubusercontent.com/71822090/135729905-665a239c-10e2-48b6-a692-782cdf4e5731.JPG)


## Testing on video dataset

Tested my model on real-time traffic videos and recognised numbers from detected license plates also estimated vehicles speed using distance/time formulae

### Results

![outputcsv](https://user-images.githubusercontent.com/71822090/135730062-e9e4f179-ba97-4e39-a407-2b30a19475d0.JPG)

## Conclusion

Using detectron2 for real-time applications like License plate detection could be very promising for the future AI generation.
Implementing Traffic Monitoring System like this could be very useful for our safety and control regulations.

## Further Modifications

More accurate speed detection method.

Training a model to detect characters of number plate using Detectron2

## References

Detectron2 documentation - https://detectron2.readthedocs.io/en/latest/

Used coco.py from https://github.com/karndeepsingh/custom_model_detectron2







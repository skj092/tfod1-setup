# tfod1-setup


1. conda create -n tfod python==3.6.9
2. conda activate tfod
3. pip install pillow lxml Cython contextlib2 jupyter matplotlib pandas opencv-python tensorflow==1.14.0
4. downloading tensorflow models repository - https://github.com/tensorflow/models/archive/refs/heads/r1.13.0.zip
5. downloading and extract pretrained model : http://download.tensorflow.org/models/object_detection/faster_rcnn_inception_v2_coco_2018_01_28.tar.gz
6. downloading dataset and utils : https://drive.google.com/file/d/12F5oGAuQg7qBM_267TCMt_rlorV-M7gf/view
7. Protobuf installing : conda install -c anaconda protobuf
8. Protobuf to .py conversion :from research folder :  protoc object_detection/protos/*.proto --python_out=.
9. Move "object_detection_tutorial.ipynb" from research/object_detection to research.
10. Open object_detection_tutorial.ipynb make these below 4 changes and execute it. 

from object_detection.utils import label_map_util
from object_detection.utils import visualization_utils as vis_util
PATH_TO_LABELS = os.path.join('object_detection/data', 'mscoco_label_map.pbtxt')
PATH_TO_TEST_IMAGES_DIR = 'object_detection/test_images'


# custom object-detection
1. download the data
2. label it using labelimg
3. convert .xml to .csv
4. convert .csv to .tfrecord
5. editing config file
6. moving slim/file to research

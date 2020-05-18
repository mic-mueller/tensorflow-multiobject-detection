# tensorflow-multiobject-detection
full commandline installtion instruction at the bottom

## install python
Download Python 3.7.7 64-bit (not 32-bit, recommended by tensoflow)
https://www.python.org/downloads/windows/

On installtion:
 - click, add python to path


## install tensoflow
for more see: https://www.tensorflow.org/install/pip

Donwload and install:
- https://aka.ms/vs/16/release/vc_redist.x86.exe
- https://aka.ms/vs/16/release/vc_redist.x64.exe

Check:
 - `python3 --version` (3.5–3.7)
 - `pip3 --version` ( >= 19.0)


Create a project folder e.g. c:\tensoflow
```cmd
mkdir c:\tensoflow
cd c:\tensoflow
python3 -m venv --promt tensoflow .venv
pip install --upgrade tensorflow
```


## full commandline installation windows 10 64bit

## install tensoflow object detection api
```cmd
bitsadmin /transfer /download /priority foreground /dynamic https://github.com/tensorflow/models/archive/master.zip c:\tensoflow\models.zip 
bitsadmin /transfer /download /priority foreground /dynamic https://github.com/EdjeElectronics/TensorFlow-Object-Detection-API-Tutorial-Train-Multiple-Objects-Windows-10/archive/master.zip c:\tensoflow\models\research\object_detection\tut_repo.zip
bitsadmin /transfer /download /priority foreground /dynamic http://download.tensorflow.org/models/object_detection/faster_rcnn_inception_v2_coco_2018_01_28.tar.gz c:\tensoflow\models\research\object_detection\faster_rcnn_inception_v2_coco_2018_01_28.tar.gz

pip install protobuf
pip install pillow
pip install lxml
pip install Cython
pip install contextlib2
pip install jupyter
pip install matplotlib
pip install pandas
pip install opencv-python

set PYTHONPATH=C:\tensorflow1\models;C:\tensorflow1\models\research;C:\tensorflow1\models\research\slim
bitsadmin /transfer /download /priority foreground /dynamic !TODO! protoc.exe to system32

cd C:\tensorflow1\models\research
protoc --python_out=. .\object_detection\protos\anchor_generator.proto .\object_detection\protos\argmax_matcher.proto .\object_detection\protos\bipartite_matcher.proto .\object_detection\protos\box_coder.proto .\object_detection\protos\box_predictor.proto .\object_detection\protos\eval.proto .\object_detection\protos\faster_rcnn.proto .\object_detection\protos\faster_rcnn_box_coder.proto .\object_detection\protos\grid_anchor_generator.proto .\object_detection\protos\hyperparams.proto .\object_detection\protos\image_resizer.proto .\object_detection\protos\input_reader.proto .\object_detection\protos\losses.proto .\object_detection\protos\matcher.proto .\object_detection\protos\mean_stddev_box_coder.proto .\object_detection\protos\model.proto .\object_detection\protos\optimizer.proto .\object_detection\protos\pipeline.proto .\object_detection\protos\post_processing.proto .\object_detection\protos\preprocessor.proto .\object_detection\protos\region_similarity_calculator.proto .\object_detection\protos\square_box_coder.proto .\object_detection\protos\ssd.proto .\object_detection\protos\ssd_anchor_generator.proto .\object_detection\protos\string_int_label_map.proto .\object_detection\protos\train.proto .\object_detection\protos\keypoint_box_coder.proto .\object_detection\protos\multiscale_anchor_generator.proto .\object_detection\protos\graph_rewriter.proto .\object_detection\protos\calibration.proto .\object_detection\protos\flexible_grid_anchor_generator.proto

python setup.py build
python setup.py install

cd C:\tensorflow1\
jupyter notebook models\research\object_decetion\object_detection_tutorial.ipynb

´´´

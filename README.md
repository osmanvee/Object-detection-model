# Object-detection-model
Setup for CNN object detection model using compute canada MNIST servers

<b> Note: </b> You must have a compute canada MNSIT account for access
Accessing compute canada servers:

**Loading modules**
* Inside `/darknet` run the following: `module load cuda/10.2.89 gcc/8.4.0 cudnn/7.6.5.32 opencv/4.5.0 openblas/0.3.9`
* `make`

**Copying test photos to the directory**
*Run `scp -r <Local image path> username@mist.scinet.utoronto.ca:/scratch/j/jcoop/username/darknet/build/darknet/x64/data/obj/test/` 
** We have copied the test photo in the test directory. *Note* : For Windows, you may use WinSC

**Perform the test on the test photo**
Run `./darknet detector test build/darknet/x64/data/training.data build/darknet/x64/yolov4-custom.cfg build/darknet/x64/backup/yolov4-custom_final.weights build/darknet/x64/data/obj/test/TEST-IMAGE.jpg`
Example of a log can be seen in `test-log.txt`

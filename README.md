## Machine Learning LEGO (R) Brick detection using Yolo engine

The purpose of this project is to detect a specific piece of LEGO(R) in a pile of bricks.
The result works on a laptop using the built-in camera.

Training was done using 200 images, labelled using ImgLabel by 8 and 11 years olds.

I've used the Yolov5 model: https://github.com/ultralytics/yolov5

The result looks promissing with detection of the "R2D2" named brick with average lighting and shaky camera.
![brick result](https://github.com/tibocap/YoloBrick/blob/main/Result.jpg)


Next stage will be to port this on an Android phone to run easily over the pile of bricks.

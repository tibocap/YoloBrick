1. Install Anaconda (download from Anaconda site on Internet)
2. Create a new env : LegoDetector 
3. Install GIT (install git for Windows from http://gitforwindows.org)
4. Clone the Yolo5 report using GitUI https://github.com/ultralytics/yolov5


5. Start Env LegoDetector in Anaconda
6. Intall pytorch : python -m pip install torch===1.7.0+cu110 torchvision===0.8.1+cu110 torchaudio===0.7.0 -f https://download.pytorch.org/whl/torch_stable.html


train:
------

cd C:\Source\LegoDetector\Yolov5
python train.py --img 640 --batch 8 --pepochs 100 --data bbc.yaml --cfg models/yolov5s.yaml --name BCCM

On Laptop this lasts a long time.(3 min per epoch, and we have 100 epoch = 300 min)


detect:
-------
cd C:\Source\LegoDetector\Yolov5
# detect images on a folder "dataset/test/"
python detect.py --source ../dataset/test/ --weights ./runs/train/BCCM5/weights/best.pt --view-img

# detect from webcam
python detect.py --source 0 --weights ./runs/train/BCCM5/weights/best.pt --view-img


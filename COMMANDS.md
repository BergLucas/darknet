# Create

ffmpeg -i myvideo.avi -vf fps=8 myvideo/img%03d.jpg

# Dataset

python process.py

# Partial

darknet.exe partial .\cfg\yolov2-tiny-voc.cfg .\yolov2-tiny-voc.weights .\yolov2-tiny-voc.conv.13 13

# Train

darknet.exe detector train .\cfg\coco.data .\cfg\yolov2-tiny-obj.cfg .\yolov2-tiny-voc.conv.13 -map

# Backup

darknet.exe detector train .\cfg\coco.data .\cfg\yolov2-tiny-obj.cfg .\backup\yolov2-tiny-obj_last.weights -map

# Detect

darknet.exe detect .\cfg\yolov2-tiny-obj.cfg .\backup\yolov2-tiny-obj_best.weights .\data\obj\metal333.jpg

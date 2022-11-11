# Partial

darknet.exe partial .\cfg\yolov2-tiny-voc.cfg .\yolov2-tiny-voc.weights .\yolov2-tiny-voc.conv.13 13

# Train

darknet.exe detector train .\cfg\obj.data .\cfg\yolov2-tiny-obj.cfg .\yolov2-tiny-voc.conv.13 -clear -map

# Detect

darknet.exe detect .\cfg\yolov2-tiny.cfg .\backup\yolov2-tiny-voc_final.weights .\data\obj\pos-1.jpg

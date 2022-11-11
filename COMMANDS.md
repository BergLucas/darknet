# Partial

darknet.exe partial .\cfg\yolov2-tiny-voc.cfg .\yolov2-tiny-voc.weights .\yolov2-tiny-voc.conv.13 13

# Train

darknet.exe detector train .\cfg\obj.data .\cfg\yolov2-tiny-obj.cfg .\yolov2-tiny-voc.conv.13 -clear -map

# Backup

darknet.exe detector train .\cfg\obj.data .\cfg\yolov2-tiny-obj.cfg .\backup\yolov2-tiny-obj_last.weights -clear -map

# Detect

darknet.exe detect .\cfg\yolov2-tiny-obj.cfg .\backup\yolov2-tiny-obj_best.weights .\data\obj\pos-1.jpg

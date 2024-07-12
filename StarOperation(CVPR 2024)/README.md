
#Removed components:
	- self.norm: The final batch normalization layer
	- self.avgpool: The adaptive average pooling layer
	- self.head: The final linear layer for classification

#Purpose change:
	- Before: The network was designed as a classifier, with a final linear layer (self.head) to output class probabilities.
	- After: The network now appears to be used as a feature extractor, returning features from different stages of the network.
	
#New output:
	- Instead of returning a single output (class probabilities), the new version returns a list of features (features) from different stages of the network.

#New attribute:
	- self.channel: This stores the number of channels at each stage, calculated by running a forward pass with a dummy input.
	
## References
  - https://github.com/ma-xu/Rewrite-the-Stars
  - https://github.com/z1069614715/objectdetection_script/blob/master/yolo-improve/yolov5-backbone/CVPR2024-StarNet

# `KeypointsDetectionModel`

Run inference on a keypoint detection model.

## Step parameters
* `type`: must be `KeypointsDetectionModel` (required)
* `name`: must be unique within all steps - used as identifier (required)
* `model_id`: must be either valid Roboflow model ID or selector to  input parameter (required)
* `image`: must be a reference to input of type `InferenceImage` or `crops` output from steps executing cropping (
`Crop`, `AbsoluteStaticCrop`, `RelativeStaticCrop`) (required)
* `disable_active_learning`: optional boolean flag to control Active Learning at request level - can be selector to 
input parameter 
* `confidence`: optional float value in range [0, 1] with threshold - can be selector to 
input parameter 
* `class_agnostic_nms`: optional boolean flag to control NMS - can be selector to 
input parameter 
* `class_filter`: optional list of classes using as filter - can be selector to 
input parameter 
* `iou_threshold`: optional float value in range [0, 1] with NMS IoU threshold - can be selector to 
input parameter. Default: `0.3`.
* `max_detections`: optional integer parameter of NMS - can be selector to input parameter 
* `max_candidates`: optional integer parameter of NMS - can be selector to input parameter 
* `keypoint_confidence`: optional float value in range [0, 1] with keypoints confidence threshold - can be selector to 
input parameter 

## Step outputs:
* `predictions` - details of predictions
* `image` - size of input image, that `predictions` coordinates refers to 
* `parent_id` - identifier of parent image / associated detection that helps to identify predictions with RoI in case
of multi-step pipelines
* `prediction_type` - denoting `keypoint-detection` model
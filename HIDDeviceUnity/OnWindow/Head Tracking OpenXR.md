# Basic Info
Path:/HeadTrackingOpenXR  
Display Name:Head Tracking - OpenXR  
Product Name:Head Tracking - OpenXR  
Manufacurer:OpenXR  
Interface:XRInputV1  
Buttons count:2  
Axis count:41  
##  All Buttons
``` 
userpresence istracked
``` 
##  All Axis
``` 
trackingstate trackingstate deviceposition x deviceposition y deviceposition z devicevelocity x devicevelocity y devicevelocity z deviceangularvelocity x deviceangularvelocity y deviceangularvelocity z centereyeposition x centereyeposition y centereyeposition z centereyevelocity x centereyevelocity y centereyevelocity z centereyeangularvelocity x centereyeangularvelocity y centereyeangularvelocity z lefteyeposition x lefteyeposition y lefteyeposition z lefteyevelocity x lefteyevelocity y lefteyevelocity z lefteyeangularvelocity x lefteyeangularvelocity y lefteyeangularvelocity z righteyeposition x righteyeposition y righteyeposition z righteyevelocity x righteyevelocity y righteyevelocity z righteyeangularvelocity x righteyeangularvelocity y righteyeangularvelocity z x y z w
``` 
##  All Buttons Ref
``` 
/HeadTrackingOpenXR|>userpresence
/HeadTrackingOpenXR|>istracked
``` 
##  All Axis ref 
``` 
/HeadTrackingOpenXR|>trackingstate trackingstate
/HeadTrackingOpenXR|>deviceposition x
/HeadTrackingOpenXR|>deviceposition y
/HeadTrackingOpenXR|>deviceposition z
/HeadTrackingOpenXR|>devicevelocity x
/HeadTrackingOpenXR|>devicevelocity y
/HeadTrackingOpenXR|>devicevelocity z
/HeadTrackingOpenXR|>deviceangularvelocity x
/HeadTrackingOpenXR|>deviceangularvelocity y
/HeadTrackingOpenXR|>deviceangularvelocity z
/HeadTrackingOpenXR|>centereyeposition x
/HeadTrackingOpenXR|>centereyeposition y
/HeadTrackingOpenXR|>centereyeposition z
/HeadTrackingOpenXR|>centereyevelocity x
/HeadTrackingOpenXR|>centereyevelocity y
/HeadTrackingOpenXR|>centereyevelocity z
/HeadTrackingOpenXR|>centereyeangularvelocity x
/HeadTrackingOpenXR|>centereyeangularvelocity y
/HeadTrackingOpenXR|>centereyeangularvelocity z
/HeadTrackingOpenXR|>lefteyeposition x
/HeadTrackingOpenXR|>lefteyeposition y
/HeadTrackingOpenXR|>lefteyeposition z
/HeadTrackingOpenXR|>lefteyevelocity x
/HeadTrackingOpenXR|>lefteyevelocity y
/HeadTrackingOpenXR|>lefteyevelocity z
/HeadTrackingOpenXR|>lefteyeangularvelocity x
/HeadTrackingOpenXR|>lefteyeangularvelocity y
/HeadTrackingOpenXR|>lefteyeangularvelocity z
/HeadTrackingOpenXR|>righteyeposition x
/HeadTrackingOpenXR|>righteyeposition y
/HeadTrackingOpenXR|>righteyeposition z
/HeadTrackingOpenXR|>righteyevelocity x
/HeadTrackingOpenXR|>righteyevelocity y
/HeadTrackingOpenXR|>righteyevelocity z
/HeadTrackingOpenXR|>righteyeangularvelocity x
/HeadTrackingOpenXR|>righteyeangularvelocity y
/HeadTrackingOpenXR|>righteyeangularvelocity z
/HeadTrackingOpenXR|>x
/HeadTrackingOpenXR|>y
/HeadTrackingOpenXR|>z
/HeadTrackingOpenXR|>w
``` 
# Capabilities  
``` json
{"deviceName":"Head Tracking - OpenXR","manufacturer":"OpenXR","serialNumber":"","characteristics":33,"deviceId":1,"inputFeatures":[{"name":"UserPresence","usageHints":[{"content":"UserPresence","id":1221106003}],"featureType":1,"customSize":4294967295},{"name":"IsTracked","usageHints":[{"content":"IsTracked","id":1429429695}],"featureType":1,"customSize":4294967295},{"name":"TrackingState","usageHints":[{"content":"TrackingState","id":1636970542}],"featureType":2,"customSize":4294967295},{"name":"DevicePosition","usageHints":[{"content":"DevicePosition","id":3323297731}],"featureType":5,"customSize":4294967295},{"name":"DeviceRotation","usageHints":[{"content":"DeviceRotation","id":3528255621}],"featureType":6,"customSize":4294967295},{"name":"DeviceVelocity","usageHints":[{"content":"DeviceVelocity","id":1066346694}],"featureType":5,"customSize":4294967295},{"name":"DeviceAngularVelocity","usageHints":[{"content":"DeviceAngularVelocity","id":2550892527}],"featureType":5,"customSize":4294967295},{"name":"CenterEyePosition","usageHints":[{"content":"CenterEyePosition","id":1253450285}],"featureType":5,"customSize":4294967295},{"name":"CenterEyeRotation","usageHints":[{"content":"CenterEyeRotation","id":215671052}],"featureType":6,"customSize":4294967295},{"name":"CenterEyeVelocity","usageHints":[{"content":"CenterEyeVelocity","id":2624447366}],"featureType":5,"customSize":4294967295},{"name":"CenterEyeAngularVelocity","usageHints":[{"content":"CenterEyeAngularVelocity","id":1178896158}],"featureType":5,"customSize":4294967295},{"name":"LeftEyePosition","usageHints":[{"content":"LeftEyePosition","id":306680142}],"featureType":5,"customSize":4294967295},{"name":"LeftEyeRotation","usageHints":[{"content":"LeftEyeRotation","id":3537142890}],"featureType":6,"customSize":4294967295},{"name":"LeftEyeVelocity","usageHints":[{"content":"LeftEyeVelocity","id":27953601}],"featureType":5,"customSize":4294967295},{"name":"LeftEyeAngularVelocity","usageHints":[{"content":"LeftEyeAngularVelocity","id":677769599}],"featureType":5,"customSize":4294967295},{"name":"RightEyePosition","usageHints":[{"content":"RightEyePosition","id":327099329}],"featureType":5,"customSize":4294967295},{"name":"RightEyeRotation","usageHints":[{"content":"RightEyeRotation","id":1559063499}],"featureType":6,"customSize":4294967295},{"name":"RightEyeVelocity","usageHints":[{"content":"RightEyeVelocity","id":4084349234}],"featureType":5,"customSize":4294967295},{"name":"RightEyeAngularVelocity","usageHints":[{"content":"RightEyeAngularVelocity","id":3749378945}],"featureType":5,"customSize":4294967295}],"CanQueryForDeviceStateAtTime":false}  
``` 

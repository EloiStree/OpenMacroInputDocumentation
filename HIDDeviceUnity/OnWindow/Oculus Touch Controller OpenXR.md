# Basic Info
Path: `/OculusTouchControllerOpenXR`  
Display Name: `Oculus Touch Controller (OpenXR)`  
Product Name: `Oculus Touch Controller OpenXR`  
Manufacurer: `Oculus`  
Interface: `XRInputV1`  
Buttons count: `13`  
Axis count: `25`  
##  All Buttons
``` 
grippressed menu primarybutton primarytouched secondarybutton secondarytouched triggerpressed triggertouched thumbstickclicked thumbsticktouched thumbresttouched istracked isTracked
``` 
##  All Axis
``` 
thumbstick x thumbstick y grip trigger trackingstate trackingstate devicePosition x devicePosition y devicePosition z pointerPosition x pointerPosition y pointerPosition z x y trackingState trackingState position x position y position z velocity x velocity y velocity z angularVelocity x angularVelocity y angularVelocity z z w
``` 
##  All Buttons Ref
``` 
/OculusTouchControllerOpenXR|>grippressed
/OculusTouchControllerOpenXR|>menu
/OculusTouchControllerOpenXR|>primarybutton
/OculusTouchControllerOpenXR|>primarytouched
/OculusTouchControllerOpenXR|>secondarybutton
/OculusTouchControllerOpenXR|>secondarytouched
/OculusTouchControllerOpenXR|>triggerpressed
/OculusTouchControllerOpenXR|>triggertouched
/OculusTouchControllerOpenXR|>thumbstickclicked
/OculusTouchControllerOpenXR|>thumbsticktouched
/OculusTouchControllerOpenXR|>thumbresttouched
/OculusTouchControllerOpenXR|>istracked
/OculusTouchControllerOpenXR|>isTracked
``` 
##  All Axis ref 
``` 
/OculusTouchControllerOpenXR|>thumbstick x
/OculusTouchControllerOpenXR|>thumbstick y
/OculusTouchControllerOpenXR|>grip
/OculusTouchControllerOpenXR|>trigger
/OculusTouchControllerOpenXR|>trackingstate trackingstate
/OculusTouchControllerOpenXR|>devicePosition x
/OculusTouchControllerOpenXR|>devicePosition y
/OculusTouchControllerOpenXR|>devicePosition z
/OculusTouchControllerOpenXR|>pointerPosition x
/OculusTouchControllerOpenXR|>pointerPosition y
/OculusTouchControllerOpenXR|>pointerPosition z
/OculusTouchControllerOpenXR|>x
/OculusTouchControllerOpenXR|>y
/OculusTouchControllerOpenXR|>trackingState trackingState
/OculusTouchControllerOpenXR|>position x
/OculusTouchControllerOpenXR|>position y
/OculusTouchControllerOpenXR|>position z
/OculusTouchControllerOpenXR|>velocity x
/OculusTouchControllerOpenXR|>velocity y
/OculusTouchControllerOpenXR|>velocity z
/OculusTouchControllerOpenXR|>angularVelocity x
/OculusTouchControllerOpenXR|>angularVelocity y
/OculusTouchControllerOpenXR|>angularVelocity z
/OculusTouchControllerOpenXR|>z
/OculusTouchControllerOpenXR|>w
``` 
# Capabilities
``` json
{"deviceName":"Oculus Touch Controller OpenXR","manufacturer":"Oculus","serialNumber":"","characteristics":356,"deviceId":4,"inputFeatures":[{"name":"thumbstick","usageHints":[{"content":"Primary2DAxis","id":2655220405}],"featureType":4,"customSize":4294967295},{"name":"grip","usageHints":[{"content":"Grip","id":1590085501}],"featureType":3,"customSize":4294967295},{"name":"grippressed","usageHints":[{"content":"GripButton","id":518426673}],"featureType":1,"customSize":4294967295},{"name":"menu","usageHints":[{"content":"MenuButton","id":2565854125}],"featureType":1,"customSize":4294967295},{"name":"primarybutton","usageHints":[{"content":"PrimaryButton","id":683514853}],"featureType":1,"customSize":4294967295},{"name":"primarytouched","usageHints":[{"content":"PrimaryTouch","id":318342609}],"featureType":1,"customSize":4294967295},{"name":"secondarybutton","usageHints":[{"content":"SecondaryButton","id":2243835638}],"featureType":1,"customSize":4294967295},{"name":"secondarytouched","usageHints":[{"content":"SecondaryTouch","id":2419066958}],"featureType":1,"customSize":4294967295},{"name":"trigger","usageHints":[{"content":"Trigger","id":2448783467}],"featureType":3,"customSize":4294967295},{"name":"triggerpressed","usageHints":[{"content":"TriggerButton","id":3798928494}],"featureType":1,"customSize":4294967295},{"name":"triggertouched","usageHints":[{"content":"TriggerTouch","id":2909594861}],"featureType":1,"customSize":4294967295},{"name":"thumbstickclicked","usageHints":[{"content":"Primary2DAxisClick","id":672085376}],"featureType":1,"customSize":4294967295},{"name":"thumbsticktouched","usageHints":[{"content":"Primary2DAxisTouch","id":833943802}],"featureType":1,"customSize":4294967295},{"name":"thumbresttouched","usageHints":[{"content":"ThumbrestTouch","id":2737618197}],"featureType":1,"customSize":4294967295},{"name":"devicepose/isTracked","usageHints":[{"content":"IsTracked","id":1429429695}],"featureType":1,"customSize":4294967295},{"name":"devicepose/trackingState","usageHints":[{"content":"TrackingState","id":1636970542}],"featureType":2,"customSize":4294967295},{"name":"devicepose/position","usageHints":[{"content":"DevicePosition","id":3323297731}],"featureType":5,"customSize":4294967295},{"name":"devicepose/rotation","usageHints":[{"content":"DeviceRotation","id":3528255621}],"featureType":6,"customSize":4294967295},{"name":"devicepose/velocity","usageHints":[{"content":"DeviceVelocity","id":1066346694}],"featureType":5,"customSize":4294967295},{"name":"devicepose/angularVelocity","usageHints":[{"content":"DeviceAngularVelocity","id":2550892527}],"featureType":5,"customSize":4294967295},{"name":"pointer/isTracked","usageHints":[{"content":"IsTracked","id":1429429695}],"featureType":1,"customSize":4294967295},{"name":"pointer/trackingState","usageHints":[{"content":"TrackingState","id":1636970542}],"featureType":2,"customSize":4294967295},{"name":"pointer/position","usageHints":[{"content":"PointerPosition","id":2471560843}],"featureType":5,"customSize":4294967295},{"name":"pointer/rotation","usageHints":[{"content":"PointerRotation","id":4200285459}],"featureType":6,"customSize":4294967295},{"name":"pointer/velocity","usageHints":[{"content":"PointerVelocity","id":1785130220}],"featureType":5,"customSize":4294967295},{"name":"pointer/angularVelocity","usageHints":[{"content":"PointerAngularVelocity","id":3334673051}],"featureType":5,"customSize":4294967295},{"name":"IsTracked","usageHints":[{"content":"IsTracked","id":1429429695}],"featureType":1,"customSize":4294967295},{"name":"TrackingState","usageHints":[{"content":"TrackingState","id":1636970542}],"featureType":2,"customSize":4294967295}],"CanQueryForDeviceStateAtTime":false}  
``` 

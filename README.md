# edge_auto_individual_params

A parameter management repository for [tier4/edge-auto](https://github.com/tier4/edge-auto) and [tier4/edge-auto-jetson](https://github.com/tier4/edge-auto-jetson).


## Directory Structure

```sh
individual_params/
├── config
│   └── <vehicle-id>    ## "default" is the default name
│       └── <camera-id> ## camera number
│           ├── camera_info.yaml
│           ├── trigger.param.yaml
│           └── v4l2_camera.param.yaml
├── CMakeLists.txt
└── package.xml
```

## Parameter files

Parameter files to activate a camera processing.

| File               | Description                                  |
| ------------------ | -------------------------------------------- |
|camera_info.yaml | Intrinsic camera parameters (ref: [image_pipeline/CameraInfo](http://www.ros.org/wiki/image_pipeline/CameraInfo))
|trigger.param.yaml | Camera shutter trigger settings (ref: [tier4/sensor_trigger](https://github.com/tier4/sensor_trigger))
|v4l2_camera.param.yaml | Camera driver settings (ref: [tier4/ros2_v4l2_camera](https://github.com/tier4/ros2_v4l2_camera))|

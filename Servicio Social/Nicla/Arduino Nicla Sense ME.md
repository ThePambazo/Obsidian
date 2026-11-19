## Sensor Classes
- Sensor: This class handles all the other sensors which have a single value to be read, like temperature, gas, pressure, etc. And also the event sensors, like the step detector. This generic sensor class provides the sensor data through the value property that returns a float.

- SensorOrientation: This class handles sensors with the Euler format, used for example with orientation. It allows you to read the pitch, roll and heading property.

- SensorXYZ: This class handles sensors with the XYZ format, like the accelerometer and the gyroscope. It contains x y and z values

- SensorQuaternion: Can be used to handle sensors with the quaternion format, can be used to calculate rotation vector, game rotation vector and geomagnetic rotation vector. You can access the x, y, z and w property using this class.

- SensorActivity: Use this class to handle sensors with the activity format. The activity is encoded as ID and can be retrieved from the value property. Use getActivity to get a human readable version of the activity e.g. "Walking activity started".

- SensorBSEC: BSEC stands for Bosch Sensortec Environmental Cluster, basically you can access the air quality (IAQ) level and it contains the following data:



| Function   | Description                        |   Data Type    |
| ---------- | ---------------------------------- | :------------: |
| iaq()      | IAQ value for regular use case     | unsigned 16bit |
| iaq_s()    | IAQ value for stationary use cases | unsigned 16bit |
| b_voc_eq() | breath VOC equivalent (ppm)        |     float      |
| co2_eq()   | CO2 equivalent (ppm) [400,]        | unsigned 32bit |
| comp_t()   | compensated temperature (Celsius)  |     float      |
| comp_h()   | compensated humidity               |     float      |
| comp_g()   | compensated gas resistance (Ohms)  | unsigned 32bit |
| accuracy() | accuracy level: [0-3]              | unsigned 8bit  |


### Sensor ID's
The IDs to address the sensors both through ESLOV and WebBLE are as follows:

| ID  | Description                         | SENSOR_ID MACRO              | Class             |
| --- | ----------------------------------- | ---------------------------- | ----------------- |
| 1   | Accelerometer passthrough           | SENSOR_ID_ACC_PASS           | SensorXYZ         |
| 3   | Accelerometer uncalibrated          | SENSOR_ID_ACC_RAW            | SensorXYZ         |
| 4   | Accelerometer corrected             | SENSOR_ID_ACC                | SensorXYZ         |
| 5   | Accelerometer offset                | SENSOR_ID_ACC_BIAS           | SensorXYZ         |
| 6   | Accelerometer corrected wake up     | SENSOR_ID_ACC_WU             | SensorXYZ         |
| 7   | Accelerometer uncalibrated wake up  | SENSOR_ID_ACC_RAW_WU         | SensorXYZ         |
| 10  | Gyroscope passthrough               | SENSOR_ID_GYRO_PASS          | SensorXYZ         |
| 12  | Gyroscope uncalibrated              | SENSOR_ID_GYRO_RAW           | SensorXYZ         |
| 13  | Gyroscope corrected                 | SENSOR_ID_GYRO               | SensorXYZ         |
| 14  | Gyroscope offset                    | SENSOR_ID_GYRO_BIAS          | SensorXYZ         |
| 15  | Gyroscope wake up                   | SENSOR_ID_GYRO_WU            | SensorXYZ         |
| 16  | Gyroscope uncalibrated wake up      | SENSOR_ID_GYRO_RAW_WU        | SensorXYZ         |
| 19  | Magnetometer passthrough            | SENSOR_ID_MAG_PASS           | SensorXYZ         |
| 21  | Magnetometer uncalibrated           | SENSOR_ID_MAG_RAW            | SensorXYZ         |
| 22  | Magnetometer corrected              | SENSOR_ID_MAG                | SensorXYZ         |
| 23  | Magnetometer offset                 | SENSOR_ID_MAG_BIAS           | SensorXYZ         |
| 24  | Magnetometer wake up                | SENSOR_ID_MAG_WU             | SensorXYZ         |
| 25  | Magnetometer uncalibrated wake up   | SENSOR_ID_MAG_RAW_WU         | SensorXYZ         |
| 28  | Gravity vector                      | SENSOR_ID_GRA                | SensorXYZ         |
| 29  | Gravity vector wake up              | SENSOR_ID_GRA_WU             | SensorXYZ         |
| 31  | Linear acceleration                 | SENSOR_ID_LACC               | SensorXYZ         |
| 32  | Linear acceleration wake up         | SENSOR_ID_LACC_WU            | SensorXYZ         |
| 34  | Rotation vector                     | SENSOR_ID_RV                 | SensorQuaternion  |
| 35  | Rotation vector wake up             | SENSOR_ID_RV_WU              | SensorQuaternion  |
| 37  | Game rotation vector                | SENSOR_ID_GAMERV             | SensorQuaternion  |
| 38  | Game rotation vector wake up        | SENSOR_ID_GAMERV_WU          | SensorQuaternion  |
| 40  | Geomagnetic rotation vector         | SENSOR_ID_GEORV              | SensorQuaternion  |
| 41  | Geomagnetic rotation vector wake up | SENSOR_ID_GEORV_WU           | SensorQuaternion  |
| 43  | Orientation                         | SENSOR_ID_ORI                | SensorOrientation |
| 44  | Orientation wake up                 | SENSOR_ID_ORI_WU             | SensorOrientation |
| 48  | Tilt detector                       | SENSOR_ID_TILT_DETECTOR      | Sensor            |
| 50  | Step detector                       | SENSOR_ID_STD                | Sensor            |
| 52  | Step counter                        | SENSOR_ID_STC                | Sensor            |
| 53  | Step counter wake up                | SENSOR_ID_STC_WU             | Sensor            |
| 55  | Significant motion                  | SENSOR_ID_SIG                | Sensor            |
| 57  | Wake gesture                        | SENSOR_ID_WAKE_GESTURE       | Sensor            |
| 59  | Glance gesture                      | SENSOR_ID_GLANCE_GESTURE     | Sensor            |
| 61  | Pickup gesture                      | SENSOR_ID_PICKUP_GESTURE     | Sensor            |
| 63  | Activity recognition                | SENSOR_ID_AR                 | SensorActivity    |
| 67  | Wrist tilt gesture                  | SENSOR_ID_WRIST_TILT_GESTURE | Sensor            |
| 69  | Device orientation                  | SENSOR_ID_DEVICE_ORI         | SensorOrientation |
| 70  | Device orientation wake up          | SENSOR_ID_DEVICE_ORI_WU      | Sensor            |
| 75  | Stationary detect                   | SENSOR_ID_STATIONARY_DET     | Sensor            |
| 77  | Motion detect                       | SENSOR_ID_MOTION_DET         | Sensor            |
| 91  | Accelerometer offset wake up        | SENSOR_ID_ACC_BIAS_WU        | SensorXYZ         |
| 92  | Gyroscope offset wake up            | SENSOR_ID_GYRO_BIAS_WU       | SensorXYZ         |
| 93  | Magnetometer offset wake up         | SENSOR_ID_MAG_BIAS_WU        | SensorXYZ         |
| 94  | Step detector wake up               | SENSOR_ID_STD_WU             | Sensor            |
| 115 | BSEC data                           | SENSOR_ID_BSEC               | SensorBSEC        |
| 128 | Temperature                         | SENSOR_ID_TEMP               | Sensor            |
| 129 | Barometer                           | SENSOR_ID_BARO               | Sensor            |
| 130 | Humidity                            | SENSOR_ID_HUM                | Sensor            |
| 131 | Gas                                 | SENSOR_ID_GAS                | Sensor            |
| 132 | Temperature wake up                 | SENSOR_ID_TEMP_WU            | Sensor            |
| 133 | Barometer wake up                   | SENSOR_ID_BARO_WU            | Sensor            |
| 134 | Humidity wake up                    | SENSOR_ID_HUM_WU             | Sensor            |
| 135 | Gas wake up                         | SENSOR_ID_GAS_WU             | Sensor            |
| 136 | Hardware Step counter               | SENSOR_ID_STC_HW             | Sensor            |
| 137 | Hardware Step detector              | SENSOR_ID_STD_HW             | Sensor            |
| 138 | Hardware Significant motion         | SENSOR_ID_SIG_HW             | Sensor            |
| 139 | Hardware Step counter wake up       | SENSOR_ID_STC_HW_WU          | Sensor            |
| 140 | Hardware Step detector wake up      | SENSOR_ID_STD_HW_WU          | Sensor            |
| 141 | Hardware Significant motion wake up | SENSOR_ID_SIG_HW_WU          | Sensor            |
| 142 | Any motion                          | SENSOR_ID_ANY_MOTION         | Sensor            |
| 143 | Any motion wake up                  | SENSOR_ID_ANY_MOTION_WU      | Sensor            |
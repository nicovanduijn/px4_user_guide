# Snapdragon Hardware Setup Example

This guide documents in detail one particular build based on the Snapdragon Flight platform. The PX4 development team has built, tested and documented this specific setup.

![](../../assets/hardware/snapdragon/snapdragon_minimal_finished.jpg)


## PX4 Dev Team Recommended Setup

We suggest using the Snapdragon Flight with the Lumenier QAV-R 250 frame and our custom hardware mounts. This setup uses a conventional PWM ESC board and therefore needs to be built with the `eagle_default` make target (see our instructions [here](https://dev.px4.io/en/setup/building_px4.html)). 

### Components
* Snapdragon Flight: [available here](https://www.intrinsyc.com/vertical-development-platforms/qualcomm-snapdragon-flight/)
* Stereo-vision add-on kit [available here](https://www.intrinsyc.com/vertical-development-platforms/qualcomm-snapdragon-flight/)
* Frame: [Lumenier QAV-R 250](https://www.getfpv.com/qav-r-fpv-racing-quadcopter-5.html)
* ESC: [Hobbywing 4in1 40A](https://www.getfpv.com/hobbywing-xrotor-micro-4-in-1-blheli-s-dshot600-esc.html)
* Motors: [Lumenier RX2206 2350KV](https://www.getfpv.com/lumenier-rx2206-11-2350kv-motor.html)
* Receiver: [Spektrum RC FPV Racing Serial Receiver](https://www.spektrumrc.com/Products/Default.aspx?ProdID=SPM4648)
* Wi-Fi Antenna: [Laird Multiband](https://www.lairdtech.com/products/maf95056-nanoblade-internal-embedded-antenna-2400-2500-4900-6000-mhz)
* GPS module: [mRo GPS + Compass module](https://store.mrobotics.io/mRo-GPS-u-Blox-Neo-M8N-HMC5983-Compass-p/gps002-mr.htm)
* Optional:[Trone range finder](http://www.teraranger.com/product/teraranger-one-distance-sensor-for-drones-and-robotics)
* Along with Trone: [I2C Adapter](http://www.teraranger.com/product/adapters-for-oneduo/)
* TODO: insert links to 3D printed parts

![](../../assets/hardware/snapdragon/snapdragon_components.jpg)


### Wiring
> **Warning** Although the Snapdragon uses DF13 connectors, the pinout is different from Pixhawk.

![](../../assets/hardware/snapdragon/snapdragon_wiring.jpg)


### Building the frame
The Lumenier QAV-R250 can be assembled normally, ignoring the side-plates intended for the FPV camera mount. In order to mount the motors along with the custom printed legs, you will need longer screws than the ones provided with the motors. Regular M3x10mm screws will do.

The Hobbywing 4in1 ESC fits the frame nicely as seen in the picture below.

![](../../assets/hardware/snapdragon/snapdragon_motors.jpg)

> **Warning** We noticed that the snapdragon is very susceptible to frame vibrations. Make sure to tighten all screws well, but not so much that you damage the windings in the plastic nut on the other end.

To attach the snapdragon to the frame, first port it over to the stereo-vision add-on kit's mounting plate. This task is quite delicate, make sure not to damage the cameras when taking them out of the old plastic housing. We recommend attaching the Wi-Fi antenna's uFL connector during this step, as it will become incredibly difficult to do so once the snapdragon is in its new housing.

![](../../assets/hardware/snapdragon/snapdragon_stereo_assembly.jpg)

After the snapdragon is mounted on the new housing, screw on the two custom printed brackets using the spare M3 screws of the Lumenier frame. Again, since you are putting metal screws into plastic, don't tighten them to the extend that you damage the platic and the screws no longer have any traction.

Finally, attach the brackets to the frame using double-sided tape. We achieved best performance when using two strips of vibration-dampening foam in between the carbon frame and the custom mounting brackets for the stereo-vision part. Cutting two strips out of the piece provided with the QAV-R frame works very well.

![](../../assets/hardware/snapdragon/snapdragon_vibration_dampening.jpg)

You can mount the GPS module and teraranger module in addition, but they are not required for normal VIO-based flight. You can now attach the snapdragon module to the QAV frame and connect the  ESC and receiver.

![](../../assets/hardware/snapdragon/snapdragon_minimal_finished_closeup.jpg)

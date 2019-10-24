# vscpl1drv-can232
VSCP Level I driver for SLCAN

This is a driver for the Lawicel CAN232 CAN adapter and other slcan devices.

Info about the adaper is available at http://www.can232.com

## LINUX/UNIX
The driver should be installed in the system search path. Default installation directory is /usr/local/lib

In the configuration file (/etc/vscpd/vscpd.conf) there should be a line as

```xml
        <canaldriver>  <!-- Information about CANAL drivers -->

		<!-- Other drivers
			.....
		  -->

                <driver>
                        <name>can232</name>
                        <parameter>/dev/ttyS0;19200;0;0;125</parameter>
                        <path>/usr/local/lib/can232drv.so</path>
                        <flags>0</flags>
                </driver>
        </canaldriver>
```

to enable the driver

(ice@geomi.org)
NOTE for Linux version of driver: !!!
	This driver was not tested on real Lawicel CAN232 CAN adapter.
	It was tested and worked on my own self made adapter based on Lawicel's documetation. It must be fully compatible with
	original but not tested.

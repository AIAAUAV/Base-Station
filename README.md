Base Station
====================

UWP that is run on the device acting as the base station during [UAV](https://github.com/AUUAV/MainUAV) flight.

Spec
---------------------

* Authenticate with the [cloud backend](https://github.com/AUUAV/Cloud-Backend)
* Receive live telemetry from the [cloud backend](https://github.com/AUUAV/Cloud-Backend)
* Send instructions for flight to the [cloud backend](https://github.com/AUUAV/Cloud-Backend)
* Connect to the [UAV](https://github.com/AUUAV/MainUAV) directly through the radio hardware TBD and monitor signal strength
* Send kill signal to the [UAV](https://github.com/AUUAV/MainUAV) directly through the radio hardware TBD

Notes
--------------------

Presumably the radio hardware chosen will be some form of proprietary interface, hopefully this is simply USB, but a wrapper (hardware and/or software) may need to be written.
Multiple instances of the base station software can connect to the UAV at once but only one can be in 'control mode' (to elimate conflicting flight instructions). This will be handled by the [cloud backend](https://github.com/AUUAV/Cloud-Backend).

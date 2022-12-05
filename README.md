# PID_OCTOPRINT

------
PID Tuning
------

Code: M503
* M503 = the main command that triggers the PID Autotune calibration.

Results:


Code: M106 S255 

* M106 = the command for Set Fan Speed
* S255 = Speed, from 0 to 255. S255 provides 100% duty cycle; S128 produces 50%


Code: M503
* M503 is the main command that triggers the PID Autotune calibration.




Code: M303 E-1 S60 C10 U1
* M303 is the main command that triggers the PID Autotune calibration.
* E-1 is the number of the heat bed that will be calibrated.
* S60 is the temperature of the heat bed that needs to be tuned at which is 60° in this case.
* C10 is the number of cycles. It’s a good idea to let the test run 5-15 times for the best results.
* U1 automatically replaces your existing heat bed PID values with the calibrated ones so you don’t have to do another step.

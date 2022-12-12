# PID_OCTOPRINT

------
** PID Tuning
------

<hr style="border:8px solid gray"> </hr>

## Setup

Check the settings before PID-tuning

###Code: 
```
M503
```

* M503 = the main command that triggers the PID Autotune calibration.

Results example:

```
function test() {
  console.log("notice the blank line before this function?");
}
```


<hr style="border:8px solid gray"> </hr>

## Setup Hotend

Code: M106 S255 

* M106 = the command for Set Fan Speed
* S255 = Speed, from 0 to 255. S255 provides 100% duty cycle; S128 produces 50%

Code: M303 E-0 S220 C10 U1

* M303 is the main command that triggers the PID Autotune calibration.
* E-0 is the hotend that will be calibrated.
* S220 is the temperature of the hotend.
* C10 is the number of cycles. It’s a good idea to let the test run 5-15 times for the best results.
* U1 automatically replaces your existing heat bed PID values with the calibrated ones so you don’t have to do another step.

Code: M503
* M503 is the main command that triggers the PID Autotune calibration.


<hr style="border:8px solid gray"> </hr>

## Setup Bed


Code: M303 E-1 S60 C10 U1
* M303 is the main command that triggers the PID Autotune calibration.
* E-1 is the number of the heat bed that will be calibrated.
* S60 is the temperature of the heat bed that needs to be tuned at which is 60° in this case.
* C10 is the number of cycles. It’s a good idea to let the test run 5-15 times for the best results.
* U1 automatically replaces your existing heat bed PID values with the calibrated ones so you don’t have to do another step.

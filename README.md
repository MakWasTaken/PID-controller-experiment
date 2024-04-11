Summary:

on/off controller has only two output conditions and switches abruptly between these two conditions. In a PID controller is responsible for ensuring that the process remains as close to the desired value as possible regardless of various disruptions, it determines how much and how quickly correction is applied by using varying amounts of the PID actions. The proportional block creates an output signal proportional to the magnitude of the error signal. The integral block creates an output proportional to the duration and magnitude of the error signal. The derivative block creates an output signal proportional to the rate of change of the error signal. Controller tuning involves correctly setting the controller P, I, and D values.

-----------------------------------------------------------------------------------------------------------------------------
Temperature control:
A house has a furnace that distributes heat throughout and a wall mounted controller called a thermostat
Thermostat has a sensor tat measures the house temperature
It compares the measurement to an adjustable setpoint
If the room temperature is below the setpoint, the furnaces turns ON
When the room temperature increases above the setpoint, the furnace turns OFF.
This type of control is called ON/OFF or Bang-Bang Control
ON/Off control is not okay for industrial processes or motion control because of inconsistency

PID controller: proportional, integral, and derivative
It determines how much and how quickly correction is applied using proportional, integral, and derivative (think of them as 3 blocks)
Each block contributes a unique signal that is added together to create the controller output signal

Feedback control loop
The controller is responsible for ensuring that the precess remains as close to the desired value as possible regardless of various disruptions
The controller compares the Transmitter Process Variable or PV signal, and the Setpoint.
Based on that comparison, the controller produces an output signal to operate the Final Control Element.
This PID Controller output is capable of operating the Final Control Element over its entire 100% range.

Programmable logic controller (PLC)
Most PID controllers are part of a PLC
Created in the program control logic using block commands
 Before PLC was a thing, a PID controller was a stand-alone device responsible for controlling one loop.

PID controller parameter
The difference between the process variable and setpoint a the error signal
Proportional block creates an output signal proportional to the magnitude of the error signal
But the closer you get to the set point, the less it pushes
Eventually, the process just runs continuously close to the setpoint (not quite there)
Here is where the integral does its work
It creators an output proportional to the duration and magnitude of the error signal
The longer the error and the greater the amount, the larger the integral output.
As long as an error exist, integral action will continue
Derivative creates an output signal proportional to the rate of change of the error signal
The faster the error changes, the larger the derivative output
Derivative control looks ahead to see what the error will be in the future and contributes to the controller output
Also known as controller tuning

Controller tuning
Correctly setting the controller P, I, and D values for specific process requirements
Correct settings achieved by controller tuning can vary between processes due to specific requirements
Could be disastrous in certain process if correct settings from one process is used on another that is unsuitable for it

Tuning methods
Increasing the amount of setpoint change and repeating the procedure until the process enters a state of steady-state oscillation
Produces adequate results, but is often impractical
autotuning 
Pid controller learns how the process responds to a change in setpoint and suggested PID settings

Write and submit one complete Java program to solve the following requirements. Your program will employ packages (that is, source directories), and contain multiple source files. Because you are using packages, your code should be in a directory named “Greenhouse.” You should be able to compile your code using the command “javac Greenhouse\*.java” from a directory just below the Greenhouse directory.

In the program for this assignment, class names have been specified. You must use the supplied class name for both class and source file name (i.e. Animal will be in a file Animal.java). If a program specifies multiple classes, then each class should be in its own separate source file.

Greenhouse is a house in which many events could happen, for example, doors may open and close, windows may open and close, fans may turn on or off, lights may turn on or off, an alarm may sound, the thermostat may turn on or off, watering machines may start or stop, and so on. Each event has its own timer and jobs (hint: use a superclass with separate subclasses, and a thread). For example, the alarm may sound five times when the thermostat has failed, and the fans may not come on until this situation is resolved, even if the fans are supposed to be on. Different events may have different priorities.

At the very beginning, a greenhouse (i.e., an object/instance of the Greenhouse class) has to read the operating plan from the file greenhouse_plan.txt. The contents and format of the file are listed below. Note: You cannot alter the format of this file, but you may add additional events when testing.

greenhouse_plans.txt:
priority=*,10
priority=Light,5
priority=Bell,1
priority=Thermostat,2
event=Thermostat,1000,*
event=Light,1000,1000
priority=Water,5
event=Water,3000,5000
test=Bell,1000
failed=Thermostat,7000
event=Water,8000,5000
event=Fan,10000,2000

The greenhouse should be able to restart the process if either of two conditions are met: (1) the user asks the greenhouse to do so; (2) the greenhouse catches an exception when doing jobs according to greenhouse_plan.txt —for example, if an event is not able to start because no specific event class is implemented. If the second condition occurs, the greenhouse will restart the process, skipping the instruction that caused the problem.

Provide the means to read classes from the file, and create classes from their names (hint: Class.forName()). Use the same methods to provide the capability to add new Event classes, and to modify any Event classes without recompiling the Greenhouse class. Note: You should not use inner classes for designing and developing Event classes. Test your program by adding at least two Event classes, and make any necessary changes to greenhouse_plan.txt.

Before the greenhouse restarts everything, it first has to turn off all events. You may need to use ArrayList or Vector to store the events (and scheduling information). Doing so will avoid the need for additional variables to represent different events, and will also allow you to have new Event classes anytime you want.

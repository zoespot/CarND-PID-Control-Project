# CarND-Controls-PID
Self-Driving Car Engineer Nanodegree Program Term2 Project 4 

My code built without error with cmake .. && make, and connected to GUI with ./pid .2 0.001 5. Final parameters for Kp, Ki, Kd are 0.2, 0.001 and 5 respectively. The vehicle successfully drove a lap around the track without leave the drivable portion of the track surface. The video recording is at 

![PID controlled run video](./pid_run.mp4)

*Reflection on PID components:*

P component is proportional to cross track error (CTE). It compensates the devition of car position from its intended trajectory. 
D component is propotional to the differential term of CTE. It reduces the oscillation with P component alone. 
I component is propotional to the integral term of CTE. It reduces the bias from the trajectory with only Pand D components. 

Their effects meet my expectation when I manually tune the parameters. First, I found a suitable P value only with a few tries. Then I added nonzero D value to reduce the oscillation. Finally I used a small amount of I to adjust the bias. The final hyperparmeters as above are achieved by a manual tuning foowling the twiddle method. 

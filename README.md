# sumobot V2    
This is my second attempt at the robot rumble competition.  
I went with the classic short and low center of mass build to have an actual shot, and got decently far (ranked 5 or something).    
## some wins
  
https://github.com/user-attachments/assets/15af0bae-5b80-4fdd-9d02-d62901c0f0b4  
  
https://github.com/user-attachments/assets/9dc7dadc-61f7-4a2c-ac24-aab5cbf59ea7  
  
https://github.com/user-attachments/assets/c91372ee-f006-4f6c-a1a5-534759aa3588  
  
https://github.com/user-attachments/assets/16831eb5-7c30-4b27-af2f-86062f862708  
  
https://github.com/user-attachments/assets/5d7bd1a6-5a12-44d0-9d3c-9b39b902b117  

## and some losses  
there were more but we dont talk about it
  
https://github.com/user-attachments/assets/7525d7b8-45e1-47ec-9dad-0a6cbb2b9bac  
  
https://github.com/user-attachments/assets/d7fa636f-afda-482d-a88f-3e85041dbb13  

## strategy  
The starting position in each match was known and constant, so the plan was to detect the opponent right at power-on and pick a response before the match even started. I made two opening sequences, selected by how close my hand was held in front of the sensor when the robot powered on.  
  
Turn and ram - spin toward the opponent's known starting position and immediately charge in  
Retreat - back away instead, meant as a counter to an opponent who opens with the strat above  
  
In practice, turning and ramming was reliable enough that it ended up being used almost every match.  
  
## hardware & sensing  
  
The original plan was 3 ToF distance sensors for better positional awareness.  
Unfortunately, each ToF sensor object turned out to eat up a large chunk of memory, and the Arduino Nano could only fit 2 sensor instances before overflowing  
Even with 2, they worked fine individually but broke when running together, so I ended up running the competition with just the single center mounted sensor.  
The code was written the hour before the competition started. Barebones but enough to get me through with the starting sequences and reacting to sensor data. 

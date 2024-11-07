# Modeling
#Specifications

Key Elements in the Diagram
Traffic Light States:

EW, WN_ES, SW_NE, and NS: These states refer to different traffic flows or directions at the intersection:
EW: East-West traffic.
WN_ES: West-North and East-South traffic.
SW_NE: South-West and North-East traffic.
NS: North-South traffic.
Each directional traffic flow has three states for the lights:
Green: Vehicles in that direction can go.
Yellow: Caution, signaling that the light will soon turn red.
Red: Vehicles must stop.
Pedestrian Signals:

There are pedestrian crossing signals for two main directions:
Pedestrian_EW Green (Cross): Pedestrians can cross East-West.
Pedestrian_NS Green (Cross): Pedestrians can cross North-South.
Timers and Transitions:

Timer expires: When a timer expires, it causes a state transition.
Pedestrian signals on/off: Indicates whether the pedestrian crossing lights are active or inactive.
Transition Rules:

Transitions occur based on the expiration of a timer, indicating the time allotted for each traffic phase.
Caution and Stop steps are added to transition states, allowing a smooth change from green to yellow to red.
All directions stop: All traffic lights turn red, providing a safe crossing time for pedestrians.
State Transitions and Specifications
EW Red → Pedestrian_EW Green (Cross):

All vehicle lights in EW direction turn red.
Pedestrian light for crossing EW direction turns green to allow pedestrians to cross.
Pedestrian_EW Green (Cross) → EW Green:

After the timer expires, pedestrian light turns off.
EW vehicle light turns green, allowing East-West traffic to proceed.
EW Green → EW Yellow → NS Green:

The EW light transitions from green to yellow, then to red.
The NS traffic light turns green, allowing North-South traffic to proceed.
NS Green → Pedestrian_NS Green (Cross):

After NS traffic has the green light, the pedestrian light for crossing North-South turns green to allow pedestrian crossing.
WN_ES Green and SW_NE Green Cycles:

These states are part of an alternating flow between different traffic directions (WN_ES and SW_NE) that must cross in sequence.
Similar transitions with yellow caution lights ensure smooth switching between directions.
Pedestrian Control
Pedestrian crossings are alternated with vehicle flows and are activated when all directions are stopped for safe crossing.
After each pedestrian crossing, the vehicle flow resumes in a specified direction.

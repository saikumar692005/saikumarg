# Simple autonomous robot avoiding an obstacle and moving to a target
# Environment setup
robot_pos = [0, 0] # Starting point
target = [5, 5] # Target position
obstacle = [3, 3] # Obstacle position
path = [robot_pos.copy()]
# Movement loop
while robot_pos != target:
if robot_pos[0] < target[0]:
robot_pos[0] += 1
elif robot_pos[0] > target[0]:
robot_pos[0] -= 1
if robot_pos == obstacle:
# Obstacle detected — go around
robot_pos[1] += 1 # Step up
if robot_pos[1] < target[1]:
robot_pos[1] += 1
elif robot_pos[1] > target[1]:
robot_pos[1] -= 1
path.append(robot_pos.copy())
# Print the path taken
print("Robot path to target:")
for step in path:
print(step)

output:
Robot Path to target:
      [0,0]
      [1,1]
      [2,2]
      [3,3]<-abstcle detected,goes around
      [3,4]
      [4,5]

# Model-Checking-of-warehouse-robotics

The project consists in creating a model to simulate an automated warehouse using UPPAAL. 
In our model there are a certain number of robots and a controller. 

The controller has the role to publish new tasks from a stack, removing those that are claimed by robots and handle the requests for claiming. 

The robot, accordingly, can claim a task and move around the grid to pick, transport or release a pod. 

Both robots and controller start in an idle status until the first tasks are generated. When a task is generated and randomly assigned to a pod, the first robot (currently free from tasks) that will open a request to claim it, will receive the task from the controller. Once the task is claimed the controller removes it from the stack meanwhile the robot will start to move itself to reach the pod and to pick it up with the objective to bring it in front of the delivery point. At the delivery point, according to the specifications of the homework, a human will have to withdraw the package, so that the robot can once more pick up the pod and crawl back to the original position of the pod to let it down. Once the robot is taken back, the robot returns in idle status waiting for a new task to claim.

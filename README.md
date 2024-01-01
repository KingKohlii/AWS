First Create Ec2 Instance.
Then Create IAM Policy with JSON, Code uploaed here with name of "IAMPolicyEC2"
Then Create IAM Roles.
In IAM Roles select AWS Service and in use case select Lambda then select policy which we created.
Give name to the Role and create Role.
Then Open Lambda and create function in Lambda.
Author from scratch, Fn Name, RunTime- Python3.9. Then in Default execution select Existing Role and create.
Then on next page in code tab put the code for EC2StartInstance. code provide here check it.
Then Deploy that code and in Config. edit general Config. add timeout and save it.
Create function for EC2StopInstance by same steps as of above like Startinstance steps.
Then click on Test and create event.
Give name to event and save it. Then click on Test check Ec2 starting and stopping.
Then Go to AWS EventBridge and create Rules.
Then in rules add name then select rule type as a schedule.
Then, select Continue to create rule.
Then in define schedule select second tab and add min/hr so after that time ec2 will get stopped.
Then Next, select target lambda function and in function select EC2StopInstances and press next and create Rule.
Done

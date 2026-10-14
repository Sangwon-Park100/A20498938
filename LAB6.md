Lab 6

1.
![](assets/L6-1.png)


2.
![](assets/L6-2.png)


3.
![](assets/L6-3.png)


4.
![](assets/L6-4.png)


5.
![](assets/L6-5.png)


6.
![](assets/L6-6.png)


7.
![](assets/L6-7.png)


8.
![](assets/L6-8.png)


Questions

1. What Dominated the Recovery Time?

In my tests, the uploader recovered in about 74 seconds and the viewer recovered in about 84 seconds. Both passed the 180-second SLO. The uploader failed when the SLO was changed to 60 seconds. Most of the recovery time came from launching a new EC2 instance and waiting for the application to start. The target group health checks also added some time.


2. What Changed in the Create and Delete Scripts?

In the previous lab, the create script used run-instances to start EC2 instances directly. In this lab, Auto Scaling Groups replaced run-instances and automatically launched replacement instances. The Application Load Balancer and target groups were also added. The delete script was changed to remove the Auto Scaling Groups, load balancer, target groups, and related resources before deleting the older lab resources.

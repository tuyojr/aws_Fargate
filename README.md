# Create a CI/CD pipeline to deploy your app to AWS Fargate (AWS Training and Certifications Lab)

AWS CodePipeline is used to model, orchestrate, and visualize a three-stage pipeline that deploys a containerized application using a blue/green deployment strategy. This strategy launches a new version of the application that runs alongside the old version and then slowly shifts traffic to the new version. Blue/green deployments are commonly employed when performing in-place application upgrades. Administrators can use these to validate new code while simultaneously running the old application version. If errors are detected in the new code, the deployment can be rolled back quickly and reliably.

When complete, your pipeline automatically builds a new container image whenever new code is pushed to your source repository and then uses AWS CodeDeploy and Amazon ECS to manage its deployment and shift traffic to it.

## Task 1: Explore the application and review the Fargate configuration

In this task, you connect to a basic application that displays news about __Amazon Web Services (AWS)__. The application has been deployed on __Amazon ECS__ using the __AWS Fargate__ launch type. After exploring the application, you review how the __Amazon ECS__ cluster, service, and task definition have been configured.

Start by reviewing the application functionality.

1. In the panel to the left of the instructions, find the value labeled __LoadBalancerUrl__. Copy it to your clipboard, paste it into a new browser tab, and press `Enter`.

    >NOTE:
    - As you can see, the application pulls in a list of recent announcements related to __AWS__ services. Each item in the list includes a brief summary in addition to a headline that links to a blog post that provides additional details.
    - The website background is __blue__. In the subsequent tasks, you update the application source code and then build a CI/CD pipeline to deploy the change. If successful, the newly deployed application features a __green__ background.

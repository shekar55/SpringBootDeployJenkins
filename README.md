- Build maven project
- Job chaining
- Create Jenkins Pipeline
- Docker
    - Install Docker Pipeline plugin .
    - To store the Docker image resulting from our build, we'll be using Docker Hub
- Devops    
![img](https://betsol.com/wp-content/uploads/2018/11/dfgsdf.png)
 The various stages in the pipeline are shown in the figure below:

1. Code changes are committed to the version control system – GitHub
1. Each commit to GitHub automatically triggers Jenkins build. Jenkins uses Maven to compile the code, run unit test and perform additional checks – code coverage, code quality, etc.
1. Once the code has been successfully compiled and all the tests have been passed. Jenkins builds a new docker image and pushes it to the Docker registry.
1. Jenkins notifies Kubernetes of the new image available for deployment.
1. Kubernetes pulls the new docker image from the docker registry.
1. Kubernetes deploys and manages the docker instance/container.

In short:
1. Checkout code.
1. Compile code.
1. Run test cases.
1. Build a docker image.
1. Push image to docker registry.
1. Pull new images from the registry.
1. Deploy and manage images and containers

More info:
<br>intro:
https://www.youtube.com/watch?v=56jtwSrNvrs&list=PLS1QulWo1RIbY8xXPqz6ad_sNHkIP3IXI&index=18
<br>Docker:
https://getintodevops.com/blog/building-your-first-docker-image-with-jenkins-2-guide-for-developers
https://www.youtube.com/watch?v=6tcoRIPBd8s
<br> Devops:
https://samratpriyadarshi.com/kubernetes-tutorial-series-setup-ci-cd-pipeline-on-kubernetes-using-jenkins/
https://betsol.com/devops-using-jenkins-docker-and-kubernetes/
https://github.com/justmeandopensource/playjenkins
https://www.youtube.com/watch?v=4E80gEen-o0
<br>Other:
https://medium.com/@khandelwal12nidhi/ci-cd-with-jenkins-and-ansible-e9163d4a6e82

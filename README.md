<p align="center">
<h1>CI/CD labs</h1>
<h3>Pipline automatically buil Docker image and Push to DockerHub</h3>
<img src="https://github.com/Joska99/jenkins-docker/blob/main/diagram.drawio.svg">
</p>

<h2>Requirements:</h2>

1. [Jankins Container with Docker](https://github.com/Joska99/joska/tree/main/docker/stateful-jenkins)
2. Add your Docker Hub credentials to jenkins

<h1> Steps:</h1>

1. In Jenkins portal: Go to "Create Item"
2. Give Name and Chose "Pipeline"
3. Chose Github project and add Github repo
4. In "Building Trigers" select "GitHub hook trigger for GITScm polling"
5. In Pipline select "Pipline script from SCM" and "Script Path" is File name

<h2> Add credential to Jenkins:</h2>

1. In Jenkins portal: Go to "Jenkins Seetings" -> "Managee Credentials"
3. Chose "Add credentials"

> Docker Hub
1. Chose "Username with Password"
2. Fill credentials fields 
3. Name it and add Description
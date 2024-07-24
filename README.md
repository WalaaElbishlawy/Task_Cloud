# Task_Cloud
# Sub task part 1

1-install jenkins using docker 
 ---------------

-- install docker

-- Run following commends in cmd
   --------------------

```bash
 docker pull jenkins/jenkins

```
```bash
docker run -d -p 8080:8080 -v jenkins_home:/var/jenkins_home --name jenkins_container jenkins/jenkins

```
 
-d: Detached mode (runs the container in the background)

-p 8080:8080: Maps port 8080 on the host to port 8080 in the container (Jenkins default port)

-v jenkins_home:/var/jenkins_home: Mounts a volume named jenkins_home to store Jenkins data (this ensures data persistence even if the container is stopped or removed)

--name jenkins_container: Assigns a name to the container for easier management

then opening a web browser and navigating to http://localhost:8080 then enter adminstrior password

2-complete configuration 
 -----------------

install plugns 

3-create admin user
 -----------------

4-create a pipeline that executes and prints "Hello world"
   --------------------------------

to create a New Pipeline Project:-

-Click on "New Item" on the Jenkins dashboard.

-Enter a name for your pipeline project, select "Pipeline", and click "OK".

-Define Pipeline Script:

-Scroll down to the Pipeline section, select "Pipeline script" from the Definition dropdown.

-In the script area, paste the following code:

```bash
pipeline {

    agent any

        stages {

            stage('Hello') {
    
                steps {
        
                    echo 'Hello world aliaa & walaa & basant'
            
                }
        
            }
    
        }

    }
```
-Save the Pipeline: Click on "Save" to save your pipeline configuration

-Click on "Build Now" to start the pipeline execution.
# Sub task part 2
make repo from githup desktop 

add list of files then commit and push

1-Create bash script file that executes the "Is" command 
```bash

#!/bin/bash
# This script lists the files in the current directory 

ls

```

-> the script is written in 'CloudTask.sh' file in main branch

3-Create a new pipeline item on jenkins

-In your Jenkins dashboard, click on your pipeline project.

-Click on "Configure" to edit the pipeline settings.

-Scroll down to the "Pipeline" section and configure the following:-
```bash

.Definition: Pipeline script from SCM

.SCM: Select Git and provide your repository URL.

.Set the branch to */main.

-> the script 'Jenkinsfile' in main branch

.Save your changes.

.build

```

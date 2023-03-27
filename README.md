# ADO_Template
This Github repository contains two files, "pipeline.yml" and "validation.yml" that are used to define and run a Docker pipeline. Here is a brief description of each file:

#### pipeline.yml
This file defines the pipeline that will build and test a Docker container. It includes a trigger that specifies the branch to build, and a pool that specifies the agent pool to use. The pipeline also references a repository called "pipelinetemplates", which contains the "validation.yml" template.

#### The steps in the pipeline include:

Running the "validation.yml" template, passing in several parameters including the Dockerfile, DockerComposeFile, and SmokeTestFile.
Building the Docker container using the Docker@2 task.
Running the Docker Compose command to start the container using the DockerCompose@0 task.
Running a smoke test using the PowerShell@2 task.
Pushing the container to a Docker registry using the Docker@2 task.
#### validation.yml
This file is a reusable template that is used by the "pipeline.yml" file. It defines several parameters that can be customized, including the Dockerfile, DockerComposeFile, and SmokeTestFile. These parameters are passed in when the template is used in the pipeline.

Overall, these two files work together to define and run a pipeline that builds and tests a Docker container.

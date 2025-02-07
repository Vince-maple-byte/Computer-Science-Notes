**Def:** A set of instructions that tells docker how to build a [[Docker Image]] 

### Instructions
*FROM:* Specifies the base image to use for the new image
*WORKDIR:* Sets the working directory for the following instructions
*COPY:* Copies the files from the build context to the image
*RUN:* Executes commands in the shell during image build.
*EXPOSE:* Informs docker that the container will listen to specified ports on runtime
*ENV:* Sets environment variables during the build process
*ARG:* Defines build time variables
*VOLUME:* Creates a mount point for external mounted [[Docker Volume]]
*CMD:* Default command to run when the container starts
*ENTRYPOINT:* Specifies the default executable to be run when the container starts

### CMD vs ENTRYPOINT
CMD and ENTRYPOINT both provide a default command, but they have a main difference between them:

- *CMD:* flexible, can be overridden
- *ENTRYPOINT:* Fixed, cannot be overridden

This main difference allows CMD to be a default command that can be changed while ENTRYPOINT is fixed.

For a more in depth look at these instructions in Docker file here is the documentation:
https://docs.docker.com/reference/dockerfile/

#backend #docker #devops 
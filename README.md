# Learning Docker - Exercise Files

A comprehensive collection of hands-on exercises and practice materials for the LinkedIn Learning course "Learning Docker" taught by Carlos Nunez. These files provide practical experience with Docker fundamentals, from basic container creation to troubleshooting common issues.

## About This Repository

This repository contains the complete exercise files used throughout the Docker course. Each directory corresponds to a specific lesson and includes all necessary files to follow along with the instructor and practice Docker commands in real-world scenarios.

## Course Information

**Instructor:** Carlos Nunez (Cloud and Software Consultant, VMware)  
**Duration:** 2 hours 6 minutes  
**Level:** Beginner  

The course covers essential Docker concepts including containers, Dockerfiles, the Docker CLI, image management, and troubleshooting techniques.

## Repository Structure

The exercises are organized by chapter and lesson number using the format `chapter_lesson`. Below is an overview of what each directory contains.

### Chapter 3: Using Docker

**03_05 - Create a Docker container from Dockerfiles, part 1**

Introduction to writing Dockerfiles with a practical example that demonstrates package installation, file copying, and entrypoint configuration.

- `Dockerfile` - Multi-stage build demonstrating package installation and user management
- `entrypoint.bash` - Script that validates Bash and curl installation, then fetches the current date

Key concepts: Base images, package management, security practices with non-root users, entrypoint scripts

**03_06 - Create a Docker container from Dockerfiles, part 2**

Advanced Dockerfile techniques building upon the previous lesson.

- `Dockerfile` - Extended build configuration
- `entrypoint.bash` - Enhanced entrypoint script
- `server.bash` - Server implementation script
- `server.Dockerfile` - Server-specific Dockerfile

Key concepts: Multiple Dockerfiles, modular script design, server containerization

**03_08 - Stopping and removing the container**

Practice with container lifecycle management using a web server example.

- `web-server.bash` - Web server startup script
- `web-server.Dockerfile` - Web server container definition

Key concepts: Container lifecycle, cleanup procedures, resource management

**03_14_before - Challenge: Starting NGINX**

A hands-on challenge to test your understanding of running web servers in containers. This directory contains the starting point for the NGINX challenge.

- `web-server.bash` - Web server configuration script
- `web-server.Dockerfile` - NGINX container setup
- `website/` - Complete static website with HTML, CSS, JavaScript, and assets

Key concepts: NGINX configuration, static file serving, port binding, volume mounting

**03_14_after - Solution: Starting NGINX**

The complete solution to the NGINX challenge, showing best practices for containerizing web applications.

- `website/` - Fully configured static website demonstrating the correct implementation

### Chapter 4: When Things Go Wrong

**04_03_before - Challenge: Fix a broken container**

A troubleshooting exercise where you'll diagnose and fix a non-functional container. This represents a common real-world scenario where containers fail to run properly.

- `app.sh` - Application script with potential issues
- `Dockerfile` - Container definition that may have problems

Key concepts: Debugging techniques, common failure modes, dependency issues

**04_03_after - Solution: Fix a broken container**

The corrected version showing how to properly resolve container issues.

- `app.sh` - Fixed application script
- `Dockerfile` - Corrected container definition using `ubuntu:xenial` base image with proper permissions

Key concepts: Base image selection, file permissions, dependency management, troubleshooting methodology

## Prerequisites

Before working with these exercises, you should have:

- Docker Desktop installed (Mac/Windows) or Docker Engine (Linux)
- Basic command line familiarity
- A text editor for viewing and modifying files
- Access to the LinkedIn Learning course (recommended but not required)

## Getting Started

1. Clone this repository to your local machine:
```bash
git clone <repository-url>
cd learning-docker-exercises
```

2. Navigate to the exercise directory you want to work with:
```bash
cd 03_05
```

3. Follow the lesson instructions to build and run the containers:
```bash
docker build -t exercise-name .
docker run exercise-name
```

## Working with the Exercises

Each exercise directory is self-contained with all necessary files. The typical workflow is:

1. Review the Dockerfile to understand the container configuration
2. Examine any scripts or application files
3. Build the Docker image using `docker build`
4. Run the container and observe the output
5. Experiment with modifications to deepen your understanding

For challenge exercises (those with `_before` and `_after` versions), try solving the problem yourself before looking at the solution.

## Common Docker Commands

Here are the essential commands you'll use throughout these exercises:

```bash
# Build an image
docker build -t image-name .

# Run a container
docker run image-name

# Run a container interactively
docker run -it image-name /bin/bash

# List running containers
docker ps

# List all containers (including stopped)
docker ps -a

# Stop a container
docker stop container-id

# Remove a container
docker rm container-id

# List images
docker images

# Remove an image
docker rmi image-name
```

## Troubleshooting Tips

If you encounter issues while working through the exercises:

- Ensure Docker is running (check Docker Desktop or `docker ps`)
- Verify file permissions on scripts (they should be executable)
- Check that you're in the correct directory when building images
- Review error messages carefully - they often indicate the specific problem
- Use `docker logs container-id` to view container output
- Try `docker run -it image-name /bin/bash` to explore the container interactively

## Additional Resources

- [Docker Documentation](https://docs.docker.com/)
- [Docker Hub](https://hub.docker.com/) - Official Docker image registry
- [Dockerfile Best Practices](https://docs.docker.com/develop/dev-best-practices/)
- [Docker CLI Reference](https://docs.docker.com/engine/reference/commandline/cli/)

## Course Learning Objectives

By completing these exercises, you will:

- Understand the fundamental differences between containers and virtual machines
- Create and manage Docker containers using the CLI
- Write Dockerfiles to build custom container images
- Bind ports and persist data from containers
- Push images to Docker Hub and other registries
- Troubleshoot common container issues
- Apply Docker best practices in real-world scenarios

## Notes

- The `website` directories contain complete static websites used for the NGINX exercises
- Some exercises build upon previous ones, so working through them sequentially is recommended
- Feel free to modify the files and experiment - that's the best way to learn
- The `_before` and `_after` directories represent challenge problems and their solutions

## License

These exercise files are provided for educational purposes as part of the LinkedIn Learning course "Learning Docker" by Carlos Nunez.

## Acknowledgments

Course created by Carlos Nunez, Cloud and Software Consultant at VMware. All exercise files and examples are designed to provide practical, hands-on experience with Docker fundamentals.

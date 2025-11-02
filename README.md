Objective :
The goal of this assignment was to reduce Docker image size and improve build efficiency using optimization techniques. I was tasked with creating two versions of the same Dockerfile - one basic and one optimized - and comparing their performance in terms of image size, build time, and startup latency. This exercise helped me understand how multi-stage builds, slim base images, and .dockerignore contribute to cleaner, faster, and more efficient containerized applications.

Technologies Used :
I used Docker to build and run container images, Python to create a simple script (app.py), and PowerShell’s Measure-Command to measure build and startup times. I manually created all files using Notepad to maintain clarity and control over the workflow. The Dockerfiles were written using both single-stage and multi-stage approaches. I also used .dockerignore to exclude unnecessary files from the build context.

Approach :
I began by creating a new folder named image-opt to isolate this assignment. Inside it, I manually created all required files: app.py, requirements.txt, .dockerignore, Dockerfile.normal, and Dockerfile.optimized. I wrote a simple Python script that prints a message to confirm container execution. The normal Dockerfile used a single-stage build with python:3.9, while the optimized version used multi-stage builds and python:3.9-slim. I built both images using Docker CLI, tagged them appropriately, and validated their functionality by running the containers. I measured build time and startup latency using PowerShell and recorded all metrics in a structured format.

Comparisons and Findings :
After building both images, I used docker images to compare their sizes and PowerShell to measure build time and startup latency. The optimized image was significantly smaller.
The size of the flask_optimized image is 108 MB, whereas the flask_normal image is 1.6 GB. This means the optimized image is approximately 16 times smaller than the normal one.

The optimized image also builds faster. In this task, Dockerfile.optimized was built in 2.989 seconds, while Dockerfile.normal took 5.580 seconds to build.

Startup latency was also improved. The optimized image started in 1.971 seconds, whereas the normal image took 2.441 seconds. This means the optimized image started almost twice as fast as the normal one.

<img width="960" height="500" alt="Image" src="https://github.com/user-attachments/assets/b4da1642-7663-4c6f-8ec4-73192ac84505" />

<img width="960" height="506" alt="Image" src="https://github.com/user-attachments/assets/cc41fb24-7e82-4fbe-b8b2-df8f05bc8903" />

<img width="960" height="508" alt="Image" src="https://github.com/user-attachments/assets/7f98170a-8adb-4dce-a3b8-b91d009da851" />


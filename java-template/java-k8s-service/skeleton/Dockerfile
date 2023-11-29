# This line specifies the base Docker image to use for building this image.
#  In this case, it's based on OpenJDK 11 with the Alpine Linux distribution, which is a lightweight Linux distribution.
FROM openjdk:11-alpine
# The ENTRYPOINT instruction sets the default executable for the Docker container.
# It specifies the script to be run when the container starts, and the script is referenced using the ${{values.artifact_id}}.sh placeholder.
ENTRYPOINT ["/usr/bin/${{values.artifact_id}}.sh"]

# These lines copy files from the build context into the Docker image.

COPY ${{values.artifact_id}}.sh /usr/bin/${{values.artifact_id}}.sh
COPY target/${{values.artifact_id}}.jar /usr/share/${{values.artifact_id}}/${{values.artifact_id}}.jar


# This Dockerfile is used to create a Docker image for a Java application.
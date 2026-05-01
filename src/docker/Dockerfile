FROM python:3.10.20-slim
# Always use the most specific tag possible

# Architecture from build system (used for binary downloads)
ARG DOCKER_PLATFORM_CPU_ARCHITECTURE


# Leave a trail of breadcrumbs
LABEL base.project.name="${ProjectName}"
LABEL base.version="${Version}"
LABEL base.docker.tag="${DockerTag}"
LABEL base.docker.image.name="${DockerImageName}"

RUN set -eux; \
	apt-get update; \
	apt-get install -y --no-install-recommends \
		ca-certificates \
		netbase \
		tzdata \
	; \
	apt-get dist-clean



ENV ENVIRONMENT="NOT_SET"
ENV PS1="\u@\h:\w \${ENVIRONMENT}\\$ "

CMD ["python3"]

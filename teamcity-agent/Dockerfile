FROM jetbrains/teamcity-agent:latest

# Prepare for mono
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF \
  && echo "deb https://download.mono-project.com/repo/ubuntu stable-xenial main" | tee /etc/apt/sources.list.d/mono-official-stable.list

RUN apt-get update \
  # Install required tools
  && apt-get install -y \
    # Make
    build-essential \
    # Amazon CLI requirements
    python-pip \
    # Install mono
    mono-devel

# Install Amazon CLI
RUN pip install awscli --upgrade --user

COPY link-kube-config.sh /services/link-kube-config.sh

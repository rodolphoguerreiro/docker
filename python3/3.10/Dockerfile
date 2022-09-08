FROM python:3.10

# Add the backports repo to sources.list
RUN echo 'deb http://deb.debian.org/debian bullseye-backports main' > /etc/apt/sources.list.d/backports.list

# Update the list of available packages
RUN apt update -y

# Install git-filter-repo, adding the required /bullseye-backports suffix
RUN apt-get install -y git-filter-repo/bullseye-backports
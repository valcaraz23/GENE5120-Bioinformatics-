# GENE5120-Bioinformatics-
# This repository is to track homework and projects in GENE 5120 : Bioinformatics in Python
# We will be mainly using Python.
# Input files may vary.
# Output files would include tables and graphs. 
# adding 
dockerfile
CopyEdit
# Base Image
FROM ubuntu:20.04

# Maintainer Information
MAINTAINER Val valcaraz23@kgi.edu

# Install Dependencies
RUN apt-get update && \
    apt-get install -y python3 python3-pip && \
    pip3 install numpy pandas matplotlib && \
    apt-get clean

# Add Your Project Script
ADD Scripts/your_script.py /usr/local/bin/

# Make Script Executable
RUN chmod +x /usr/local/bin/your_script.py

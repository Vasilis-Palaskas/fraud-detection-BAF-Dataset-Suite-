# fraud-detection-BAF-Da``taset-Suite

How to activate the virtual cloud-hosted environment here: source ~/miniforge3/bin/activate mlops

## .devcontainer folder

1) The **devcontainer.json**
This is the "brain" of the configuration. It tells VS Code (and GitHub) to use your Dockerfile, install extensions, and use the Miniforge "Feature."

2)  The **Dockerfile**
This defines the "box" your code lives in. We start with a slim Python 3.10 image provided by Microsoft.

# Use a specific Python 3.10 version as the base
FROM mcr.microsoft.com/devcontainers/python:3.10-bullseye

# Ensure we are operating as the vscode user for safety
USER vscode

# The Miniforge feature (defined in the JSON) will handle the installation,
# but we ensure the shell is initialized so 'conda' and 'mamba' work immediately.
RUN /opt/conda/bin/conda init bash

After creating both above files, go to Command-prompt and select re-open the container and VS code will automatically find the container related files within the repo and will run it. Ensure first that you have already isntalled extendsion of Dev containers in VS Code.
Miniforge is a minimalist conda isntaller that uses Conda forge as default channel. ideal for creating fast lightweight python environments

## Activation of the environment
 conda activate base
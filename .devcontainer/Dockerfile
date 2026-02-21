# Use a specific Python 3.10 version as the base
FROM mcr.microsoft.com/devcontainers/python:3.10-bullseye

# Ensure we are operating as the vscode user for safety
USER vscode

# The Miniforge feature (defined in the JSON) will handle the installation,
# but we ensure the shell is initialized so 'conda' and 'mamba' work immediately.
#RUN /opt/conda/bin/conda init bash
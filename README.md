# Dockerfile Bug: Missing requirements.txt

This repository demonstrates a common error in Dockerfiles: attempting to copy a file that doesn't exist in the build context.  The `requirements.txt` file is referenced in the `RUN pip3 install -r requirements.txt` command, but it's not included in the Dockerfile's context.

## Bug

The provided `Dockerfile` attempts to install Python packages from `requirements.txt`, but this file is missing, leading to a build failure.

## Solution

The `Dockerfile_fixed` file corrects this by ensuring that `requirements.txt` is copied before installation.  The `requirements.txt` file itself is included in this repo for demonstration.
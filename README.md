# Inotify-User-Instances-Limit-Configurator-deb

**Purpose**: This repository centralizes system configuration files, specifically the `11-max-user-instances.conf` file, and automates the release of a Debian package for software projects.

## Configuration File

**File**: `/etc/sysctl.d/11-max-user-instances.conf`

The configuration file contains:

       fs.inotify.max_user_instances=8192


- **Purpose**: This configuration file is used to set the maximum number of inotify user instances on a Linux system.

## Debian Package Release

We've set up a GitHub Actions workflow that automatically builds and releases a Debian package when a semantic version tag is pushed to the repository. This allows for easy distribution and installation of your software on Debian-based systems.

### Workflow Details

- **Workflow File**: `.github/workflows/release.yml`
- **Trigger**: The workflow is triggered by pushes with tags that start with 'v' (e.g., v1.0.0).
- **Build and Release**: The workflow performs the following steps:

  1. Checks out the code.
  2. Runs the build commands (you can customize this for your software).
  3. Creates a GitHub release with the Debian package as an asset.

### Why This Workflow?

This workflow is beneficial for the following scenarios:

- **System Configuration Management**: You can maintain important system configuration files in version control, allowing for easy tracking and changes over time.

- **Software Packaging**: If you have software projects that need to be distributed as Debian packages, this workflow automates the build and release process, simplifying the installation for users on Debian-based systems.

- **Version Control**: Using semantic versioning and GitHub releases ensures transparency, making it easy for users to install specific software versions and track the project's history.

## Example Use Cases

- **Web Server Configuration**: Manage configuration files for web servers, database servers, or other services deployed on Linux servers.

- **Software Distribution**: Automate the release of software as Debian packages for a more user-friendly installation experience.

- **Collaboration**: Collaborate with a team to collectively manage and maintain system configuration files.

This repository was created using ChatGPT. Feel free to customize the content and workflow to suit your specific needs.

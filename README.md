# Linux Bin Scripts

## Description

This repository contains a collection of general-purpose utility bash scripts. These scripts are designed to automate various routine tasks. They are typically scheduled via cron jobs to ensure consistent and hands-free execution. The goal of this repo is to centralize and version-control personal automation tools for easier maintenance and reuse across systems.

## Tech Stack

![Image Alt](https://skillicons.dev/icons?i=bash)

## Get Started

[In Development]

## List of Scripts

- `process_dir_list`: This script takes two inputs: the `path to another script` and a `file containing a list of directory paths`. It reads each directory path from the list (ignoring empty lines and comments), and for each valid entry, it executes the provided script with the directory path as an argument.

- ### `backup`

  - `commit_and_bundle`: This script accepts a project directory (and optionally, an output directory) as input. It commits any uncommitted changes in the directory, creates a Git bundle file, containing the entire repository history, and moves the bundle to the specified output directory (defaulting to `~/backup`). It is intended to ensure that important system directories are under version control, and bundled into portable .bundle files.

  - `backup`: The purpose of this script is to automate the process of creating backup bundles of specified directories and moving them to an external drive. It first calls the `commit_and_bundle` script to create bundles of directories listed in a file and stores them in the `~/backup` directory. Then, it copies all the generated bundles to an external drive for safe storage.

- ### `clean_temp_dirs`

  - `delete_temp_files`: This script is designed to delete all files within a specified directory while leaving the directory structure intact. It takes a directory path as input, and then removes all files inside that directory. This script helps in cleaning up directories without removing the directories themselves.

  - `clean_temp_dirs`: This script automates the process of cleaning up temporary files in multiple directories. It calls the `delete_temp_files` script to delete files from a list of directories specified in a directory list file. This is useful for managing and cleaning temporary or unnecessary files across multiple locations in one go.

## Author

[Dev J. Shah](https://github.com/busycaesar)

# Github to WordPress.org Deployment Script
We all know releasing plugins can be quite a chore, and deep down we all loathe SVN so here is a neat little script for automating the process as much as possible.

## What this script does
This script will pull down your remote GIT and SVN repositories, tag a release using the branch you specify, and commit everything to WordPress.org.

To use it you must:

1. Host your code on GitHub
2. [Obtain a personal access token](https://github.com/settings/tokens) (keep this private!)
3. Already have a WordPress.org SVN repository setup for your plugin.
4. Have both GIT and SVN setup on your machine and available from the command line.

## Getting started

1. Clone this repository
2. Copy the `parameters.sh.dist` file and name the copy `parameters.sh`
3. Set the `PLUGIN_SLUG` to match the slug of your WordPress.org plugin and PLUGIN_AUTHOR to your WordPress.org username.
4. Set the `GITHUB_REPO_OWNER` to the owner of the repository you wish to deploy. Usually your username.
5. Set the `GITHUB_REPO_NAME` to the name of your GitHub repo.
6. Ensure the release script has execute permissions: `chmod +x ./release`

The script is ready to run.

## Usage

1. Open up terminal and cd to the directory containing the script.
2. Run: `./release`
3. Follow the prompts.

## Demo

Here is a screencast of the process you'll typically see when running the script.

![Demo](demo.gif?raw=true "Demo of the release script")

## Final notes

- This will checkout the remote version of your Github Repo.
- Committing to WordPress.org can take a while for large repos so be patient.
- Tested on Mac and Ubuntu 16.04 only.
- Use at your own risk of course :)

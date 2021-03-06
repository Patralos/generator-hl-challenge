# Hacking-Lab Challenge Generator
This generator uses [Yeoman](https://yeoman.io/) to generate new [Hacking-Lab](https://www.compass-security.com/en/products/hacking-lab/) Challenge Docker containers.

## Installation
1. Install NodeJS and NPM (Live CD: `sudo apt install nodejs npm`)
2. Install yo and our generator: `sudo npm install -g generator-hl-challenge yo`

## Usage
**Note:** The following commands should be run as a user, not as root. If you're using the Live CD switch to the default user by running `su - hacker` before following these steps.

1. Create an empty directory: `git init my-awesome-challenge && cd my-awesome-challenge`
2. Run the generator and answer all questions: `yo hl-challenge`
3. Read the `README.md` file in your new challenge for customization and build instructions

Please leave [feedback](https://github.com/hacking-lab/generator-hl2-challenge/issues) if you run into any problems.

## Development
If you want to develop on the Yeoman generator itself, run `sudo npm link` in this directory. This will symlink this directory so it's available in Yeoman.

### Adding support for a new image
To add support for a new base image, you will have to:

1. Add it to the base images in `index.js`
2. Add `generators/app/templates/{image}.md` with the customization instructions
3. Add `generators/app/templates/{image}/*` with a tiny sample application (optional, don't add root/ to the path)

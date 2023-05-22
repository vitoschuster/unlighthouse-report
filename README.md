# unlighthouse-report

This repository provides a simple setup for generating Lighthouse reports using the `unlighthouse` package. It allows you to easily build static versions of your web application and generate Lighthouse reports to analyze its performance.

## Prerequisites

Before using this repository, ensure that you have the following dependencies installed:

- [Node.js](https://nodejs.org) (version 12 or higher)
- [Yarn](https://yarnpkg.com) (package manager)

## Installation

To get started, follow these steps:

1. Clone this repository to your local machine.
2. Open a terminal and navigate to the cloned repository's directory.
3. Run the following command to install the project dependencies:

   
   `yarn install`
 

## Usage

This repository provides two main scripts that you can use:

### 1. unlighthouse-build

The `unlighthouse-build` script builds a static version of your web application and generates a Lighthouse report. It saves the report for the current month in the `.unlighthouse` directory with a timestamped folder name corresponding to the current date (e.g., `.unlighthouse/2023-05`).

To execute this script, run the following command:

`yarn unlighthouse-build`


This will trigger the build process and generate the Lighthouse report.

### 2. unlighthouse-serve

The `unlighthouse-serve` script serves the previously generated Lighthouse report using the `sirv-cli` package. It allows you to view the report in your browser.

To execute this script, run the following command:


`yarn unlighthouse-serve`

This will start a local server and serve the Lighthouse report for the current MONTH. Open your browser and navigate to the provided URL to view the report.

**Note:** Make sure to run the `unlighthouse-build` script before running `unlighthouse-serve` to generate the report.

**Note:** If you want to run a lighthouse report for another month, swap the `$(date +%Y-%m)"` with the desired month in `package.json > scripts > unlighthouse-serve`


## Configuration
To make changes to the configuration of lighthouse like the site name, number of threads running the program, throttling etc. check the official documentation [unlighthouse.dev](https://unlighthouse.dev)

Current settings can be found in the unlighthouse.config.ts file
# ESS Tasking

Essaly is just a [Taskfile](https://taskfile.dev/) to control the different ESS docker containers.

## Overview

Here is a list of the task commands and their explaination:

| Command           | Execution                                                                        | Description                                                     |
| ----------------- | -------------------------------------------------------------------------------- | --------------------------------------------------------------- |
| network:create    | `task network:create`                                                            | Create a docker network for all ESS containers                  |
| basemap:restart   | `task basemap:restart`                                                           | Restart the ess-basemap container                               |
| overlay:restart   | `task overlay:restart`                                                           | Restart the ess-overlay container                               |
| api:restart       | `task api:restart`                                                               | Restart the ess-api container                                   |
| tilemaker:execute | `TILEMAKER_INPUT=input_path TILEMAKER_OUTPUT=output_path task tilemaker:execute` | Execute the tilemaker container                                 |
| osmosis:execute   | `OSMOSIS_INPUT=input_path OSMOSIS_OUTPUT=output_path task osmosis:execute`       | Execute the osmosis container                                   |
| ess:restart:all     | `task ess:restart:all`                                                             | Restart all ESS containers (ess-basemap, ess-overlay and ess-api) |
| docker:logs       | `task docker:logs`                                                               | Show the logs of all ESS containers                             |

## Setup

Add a `.env` file in the root of the project with the following content:

```bash
BASEMAP_DOCKER_IMAGE=""   # value for the basemap docker image
BASEMAP_DATA_PATH=""      # value for the basemap data path

OVERLAY_DOCKER_IMAGE=""   # value for the overlay docker image
OVERLAY_DATA_PATH=""      # value for the overlay data path

API_DOCKER_IMAGE=""       # value for the api docker image
API_DATA_PATH=""          # value for the api data path
API_ENV_PATH=""           # value for the api env path

TILEMAKER_DOCKER_IMAGE="" # value for the tilemaker docker image
TILEMAKER_DATA_PATH=""    # value for the tilemaker data path

OSMOSIS_DOCKER_IMAGE=""   # value for the osmosis docker image
OSMOSIS_DATA_PATH=""      # value for the osmosis data path
```

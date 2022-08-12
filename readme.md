# Welcome to the Anythink Market repo

To start the app use Docker. It will start both frontend and backend, including all the relevant dependencies, and the db.

Please find more info about each part in the relevant Readme file ([frontend](frontend/readme.md) and [backend](backend/README.md)).

## Development

When implementing a new feature or fixing a bug, please create a new pull request against `main` from a feature/bug branch and add `@vanessa-cooper` as reviewer.

## First setup

- Run a fresh VM running Ubuntu 22.04
- Install
  - docker
  - build-essential
- Clone the repo
- Run `sudo docker-compose up -d`
- On your local machine install `socat` and run:
  ```bash
  socat TCP-LISTEN:3000,reuseaddr,fork TCP4:192.168.122.23:3000 &
  socat TCP-LISTEN:3001,reuseaddr,fork TCP4:192.168.122.23:3001 &
  ```

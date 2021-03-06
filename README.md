# lobby-wall-events-map-app
React web application for lobby wall map and event listing.

## Installation

Clone lobby-wall-events-map-app repo locally.

Unpack node modules via Yarn:

```
$ cd lobby-wall-events-map-app
$ yarn
```

Find .env file in team Google Drive:
```
+-- DME: Web & Interactive
|   +-- Exhibit Interactives
|   |   +-- Lobby Welcome Wall Events App
|   |   |   +-- Technical
```

Copy .env into root of local lobby-wall-events-map-app project

## Testing

Unit and regression snapshot testing using Enzyme and Jest test utilities are
in place with test init script in package.json. (This app was not developed
using test driven development, and the existing tests are fairly trivial.)

```
yarn test
```

## Build Notes

### .env variable for webpack module bundler build
The URL for the events data feed is saved as global EVENTS_API_URL variable
expected by webpack for dev and prod distribution builds. The variable is
saved in local .env file in project root and excluded from git repo.

## Development and Production Builds

Webpack build init scripts in package.json.

```
yarn dev
yarn build
```

## Deploy Notes

The deploy script deletes s3://lobby-wall-events-map.calacademy.org content and copies local dist folder contents to s3://lobby-wall-events-map.calacademy.org.

```
yarn deploy
```

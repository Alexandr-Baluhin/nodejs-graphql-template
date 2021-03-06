[![Maintenance](https://img.shields.io/maintenance/yes/2018.svg)]()
[![PRs Welcome](https://img.shields.io/badge/PRs-welcome-brightgreen.svg?style=flat-square)](http://makeapullrequest.com)
[![Build Status TravisCI](https://travis-ci.org/ctco/nodejs-graphql-template.svg?branch=master)](https://travis-ci.org/ctco/nodejs-graphql-template)
[![Build Status AppVeyor](https://ci.appveyor.com/api/projects/status/wclytcth7faa5na5?svg=true)](https://ci.appveyor.com/project/trioletas/koa-graphql-template)
[![dependencies Status](https://david-dm.org/ctco/nodejs-graphql-template/master/status.svg)](https://david-dm.org/ctco/nodejs-graphql-template/master)
[![devDependencies Status](https://david-dm.org/ctco/nodejs-graphql-template/master/dev-status.svg)](https://david-dm.org/ctco/nodejs-graphql-template/master#info=devDependencies)

# nodejs-graphql-template

Node.js, Koa, GraphQL and TypeScript template project.

Batteries and opinions included :raised_hands:

## Features

- Docker :whale: configuration for production deployment, development and testing
- GraphQL tools:

  - _GraphiQL_
  - _GraphQL Voyager_
  - _GraphQL Playground_
  - _GraphQL IDL_
  - _Apollo Tracing_

- Reference [GraphQL Models and Connectors architecture](https://dev-blog.apollodata.com/how-to-build-graphql-servers-87587591ded5) implementation
- CORS middleware
- [12 Factor Configuration](https://12factor.net/config) with `.env`
- Configurable logging
  - powered by `winston`
- Supercharged Development Mode
  - Incremental TypeScript builds
  - Automatic server restart on changes
  - Linting
- Testing
  - Unit tests
  - Integration tests for GraphQL schema
- Reporting
  - Test result export to JUnit format
  - Coverage result export to Cobertura format

## Required Software

- `node` >= 8.1.4 & `yarn`

or

- `Docker` >= 17.05

## Install

- yarn: `$ yarn`
- Docker: `$ docker-compose up`

## Develop

- yarn: `$ yarn start`
- Docker: `$ docker-compose up --build`

Attention Windows users: when `Docker for Windows` is not an option, install `yarn` and run `$ yarn && yarn docker-mount` beforehand.
## Generate TypeScript types for GraphQL schema and default GraphQL resolvers 

`$ yarn gqlgen`

## Test

> single test run

### Run unit tests

`$ yarn test:unit`

### Run integration tests

`$ yarn test:integration`

### Run all tests

`$ yarn test`

### Run e2e tests

Run the app or point E2E_TEST_URL to a remote instance you want to test against.

`$ yarn test:e2e`

### Generate coverage reports

Set environment variable `CI` to true to generate coverage reports.

In *nix:

`CI=true yarn test`

In Windows:

`set CI=true&&yarn test`

## Build

`$ yarn build` or `$ docker build .`

## Tech Stack

- TypeScript
  - [Home Page](https://www.typescriptlang.org/)

- Koa
  - [GitHub](https://github.com/koajs/koa)

- GraphQL
  - [graphql-tools](https://github.com/apollographql/graphql-tools)
  - [graphql-relay](https://github.com/graphql/graphql-relay-js)
  - [graphql-relay-tools](https://github.com/excitement-engineer/graphql-relay-tools)
  - [graphql-import](https://github.com/prisma/graphql-import)
  - [graphql-tracing](https://github.com/apollographql/apollo-tracing)
  - [apollo-server](https://github.com/apollographql/apollo-server)
  - [graphql-voyager](https://apis.guru/graphql-voyager)
  - [graphql-playground](https://github.com/graphcool/graphql-playground)
  - [graphqlgen](https://github.com/prisma/graphqlgen)

- DataLoader
  - [dataloader](https://github.com/facebook/dataloader)

- Jest
  - [Documentation](https://facebook.github.io/jest/docs/en/getting-started.html)

- winston
  - [GitHub](https://github.com/winstonjs/winston)

- Docker
  - [Home Page](https://www.docker.com)

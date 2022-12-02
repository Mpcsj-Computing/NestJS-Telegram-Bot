<p align="center">
  <a href="http://nestjs.com/" target="blank"><img src="https://nestjs.com/img/logo_text.svg" width="320" alt="Nest Logo" /></a>
  <a href="https://telegram.org" target="blank"><img src="https://i.imgur.com/tDyH4Th.png" width="200" alt="N Logo" /></a>
</p>

[circleci-image]: https://img.shields.io/circleci/build/github/nestjs/nest/master?token=abc123def456
[circleci-url]: https://circleci.com/gh/nestjs/nest

  <p align="center">Simple NestJS telegram Bot</p>
    <p align="center">
<a href="https://www.npmjs.com/~nestjscore" target="_blank"><img src="https://img.shields.io/npm/v/@nestjs/core.svg" alt="NPM Version" /></a>
<a href="https://www.npmjs.com/~nestjscore" target="_blank"><img src="https://img.shields.io/npm/l/@nestjs/core.svg" alt="Package License" /></a>
<a href="https://www.npmjs.com/~nestjscore" target="_blank"><img src="https://img.shields.io/npm/dm/@nestjs/common.svg" alt="NPM Downloads" /></a>
<a href="https://circleci.com/gh/nestjs/nest" target="_blank"><img src="https://img.shields.io/circleci/build/github/nestjs/nest/master" alt="CircleCI" /></a>
<a href="https://coveralls.io/github/nestjs/nest?branch=master" target="_blank"><img src="https://coveralls.io/repos/github/nestjs/nest/badge.svg?branch=master#9" alt="Coverage" /></a>
<a href="https://discord.gg/G7Qnnhy" target="_blank"><img src="https://img.shields.io/badge/discord-online-brightgreen.svg" alt="Discord"/></a>
<a href="https://opencollective.com/nest#backer" target="_blank"><img src="https://opencollective.com/nest/backers/badge.svg" alt="Backers on Open Collective" /></a>
<a href="https://opencollective.com/nest#sponsor" target="_blank"><img src="https://opencollective.com/nest/sponsors/badge.svg" alt="Sponsors on Open Collective" /></a>
  <a href="https://paypal.me/kamilmysliwiec" target="_blank"><img src="https://img.shields.io/badge/Donate-PayPal-ff3f59.svg"/></a>
    <a href="https://opencollective.com/nest#sponsor"  target="_blank"><img src="https://img.shields.io/badge/Support%20us-Open%20Collective-41B883.svg" alt="Support us"></a>
  <a href="https://twitter.com/nestframework" target="_blank"><img src="https://img.shields.io/twitter/follow/nestframework.svg?style=social&label=Follow"></a>
</p>
  <!--[![Backers on Open Collective](https://opencollective.com/nest/backers/badge.svg)](https://opencollective.com/nest#backer)
  [![Sponsors on Open Collective](https://opencollective.com/nest/sponsors/badge.svg)](https://opencollective.com/nest#sponsor)-->

## Description

- To run the project, you must add two environment variables:

  1. `TELEGRAM_TOKEN` -> Your telegram token
  2. `TEST_CHAT_ID` -> A test chat id for your code to send messages

- [BotFather manual for developers](https://core.telegram.org/bots)
- [BotFather contact on Telegram](https://telegram.me/BotFather)
- [NPM Package for Telegram](https://www.npmjs.com/package/node-telegram-bot-api)

## Video fixes

1. You can actually install types for the project by running: `yarn add @types/node-telegram-bot-api --dev`. There are commented lines on the service layer with the typed code
2. You actually must send a message to a `chat_id` rather than a `user_id` on Telegram. However, if you are sending a message to one user directly rather than a group with multiple users, then the `chat_id` is the same as the `user_id` as the example below:

```javascript
  {
  "message_id": 9,
  "from": {
    "id": 123123123, // this is a user id (is the same as the chat id if you are sending a message to one person directly)
    "is_bot": false,
    "first_name": "UserFirstName",
    "last_name": "UserLastName",
    "language_code": "en"
  },
  "chat": {
    "id": 123123123, // this is the one that you actually send a message to, but it is ok to use the previous one if you want to send a message to one person directly
    "first_name": "UserFirstName",
    "last_name": "UserLastName",
    "type": "private"
},
"date": 1669948713,
"text": "Message sent by user on Telegram"
}
```

## Installation

```bash
# Install dependencies
$ yarn
```

## Running the app

```bash
# development
$ yarn start

# watch mode
$ yarn start:dev

# production mode
$ yarn start:prod
```

## Test

```bash
# unit tests
$ yarn test

# e2e tests
$ yarn test:e2e

# test coverage
$ yarn test:cov
```

## Stay in touch

- Website - [https://mpcsj.com](https://mpcsj.com/)

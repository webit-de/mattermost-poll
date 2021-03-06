# Mattermost Poll

Poll Slash Command for Mattermost.

[![Packagist](https://img.shields.io/packagist/v/pixelbrackets/mattermost-poll.svg)](https://packagist.org/packages/pixelbrackets/mattermost-poll/)
[![Mattermost Integration](https://img.shields.io/badge/mattermost-slash_command-blue.svg)](https://about.mattermost.com/community-applications/)

`/poll supper soup salad "taco and burito" burger`

![Screenshot](./docs/images/poll.png)

## Requirements

- PHP
- MySQL

The Mattermost instance calling this service has to be version 4.2 or greater
(provide »Interactive Message Buttons« feature).

## Installation

1. Clone project to desired directory
1. Run `composer install`
1. Edit `.env` file
1. Initialize database
   ```bash
   ./bin/console doctrine:database:create
   ./bin/console doctrine:migrations:migrate
   ```
1. Configure webserver to serve `web` directory
   - Development / Test: Run `php bin/console server:start 127.0.0.1:8000`
   - Production: [Configure webserver for Symfony Apps](https://symfony.com/doc/current/setup/web_server_configuration.html)
     and [export `.env` file](https://stackoverflow.com/questions/19331497/set-environment-variables-from-file/20909045#20909045)
1. Open homepage to see the »Request URL« needed for »Slash Commands«

## Integration

1. Add new »Slash Command« in each Teamspace in Mattermost
1. Use the »Request URL« shown on the homepage of the service

## Usage

- Type the slash command, followed by the poll title, followed by all options
- Separete the title and each option with spaces
- use quotes to include spaces in a string

Create a poll with a title and four options
```
/poll supper soup salad "taco and burito" burger
```

## Source

https://gitlab.com/pixelbrackets/mattermost-poll/

## License

GNU General Public License version 2 or later

The GNU General Public License can be found at http://www.gnu.org/copyleft/gpl.html.

## Author

Dan Untenzu (<mail@pixelbrackets.de> / [@pixelbrackets](https://github.com/pixelbrackets))

## Changelog

[./CHANGELOG.md](./CHANGELOG.md)

## Contribution

This script is Open Source, so please use, patch, extend or fork it.

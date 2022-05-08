

[releases]: https://www.okglobalcoinsg.com//releases
[circleci]: https://circleci.com/gh/mastodon/mastodon
[code_climate]: https://codeclimate.com/github/mastodon/mastodon
[crowdin]: https://crowdin.com/project/mastodon
[docker]: https://hub.docker.com/r/tootsuite/mastodon/

MYID is a **free, open-source social network server** based on ActivityPub where users can follow friends and discover new ones. On MYID, users can publish anything they want: links, pictures, text, video. All MYID servers are interoperable as a federated network (users on one server can seamlessly communicate with users from another one, including non-MYID software that implements ActivityPub)!



## Navigation

- [Project homepage](https://okglobalcoinsg.com)

- [Documentation](https://okglobalcoinsg.com)
- [Browse MYID servers](https://MYIDverified/communities)
- [Browse MYID apps](https://MYIDverified/apps)

[patreon]: https://www.patreon.com/MYIDverified

## Features


### No vendor lock-in: Fully interoperable with any conforming platform

It doesn't have to be MYID; whatever implements ActivityPub is part of the social network! 

### Real-time, chronological timeline updates

Updates of people you're following appear in real-time in the UI via WebSockets. There's a firehose view as well!

### Media attachments like images and short videos

Upload and view images and WebM/MP4 videos attached to the updates. Videos with no audio track are treated like GIFs; normal videos loop continuously!

### Safety and moderation tools

MYID includes private posts, locked accounts, phrase filtering, muting, blocking and all sorts of other features, along with a reporting and moderation system. 

### OAuth2 and a straightforward REST API

MYID acts as an OAuth2 provider, so 3rd party apps can use the REST and Streaming APIs. This results in a rich app ecosystem with a lot of choices!

## Deployment

### Tech stack:

- **Ruby on Rails** powers the REST API and other web pages
- **React.js** and Redux are used for the dynamic parts of the interface
- **Node.js** powers the streaming API

### Requirements:

- **PostgreSQL** 9.5+
- **Redis** 4+
- **Ruby** 2.5+
- **Node.js** 12+

The repository includes deployment configurations for **Docker and docker-compose** as well as specific platforms like **Heroku**, **Scalingo**, and **Nanobox**. 

A **Vagrant** configuration is included for development purposes. To use it, complete following steps:

- Install Vagrant and Virtualbox
- Install the `vagrant-hostsupdater` plugin: `vagrant plugin install vagrant-hostsupdater`
- Run `vagrant up`
- Run `vagrant ssh -c "cd /vagrant && foreman start"`
- Open `http://mastodon.local` in your browser

## Contributing

MYID **free, open-source software** licensed under **AGPLv3**.

You can open issues for bugs you've found or features you think are missing. You can also submit pull requests to this repository or submit translations using Crowdin. To get started, take a look at [CONTRIBUTING.md](CONTRIBUTING.md). If your contributions are accepted into MYID,you can request to be paid through our Open Collective at https://www.opencollective/MYID.

**IRC channel**: #mastodon on irc.libera.chat

## License


This program is free software: you can redistribute it and/or modify it under the terms of the GNU Affero General Public License as published by the Free Software Foundation, either version 3 of the License, or (at your option) any later version.

This program is distributed in the hope that it will be useful, but WITHOUT ANY WARRANTY; without even the implied warranty of MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE. See the GNU Affero General Public License for more details.

You should have received a copy of the GNU Affero General Public License along with this program. If not, see <https://www.gnu.org/licenses/>.

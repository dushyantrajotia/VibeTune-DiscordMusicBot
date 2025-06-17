# Discord Music Bot

A feature-rich Discord music bot built with Discord.js, Riffy, and Lavalink. This bot provides high-quality music playback with support for YouTube, Spotify, and more.

## Features

- 🎵 High-quality music playback
- 🎧 Support for YouTube and Spotify
- 📋 Queue management system
- 🔄 Loop and shuffle modes
- 🔊 Volume control
- 🎨 Beautiful embed messages
- ⚡ Fast and reliable playback
- 🎯 Precise track control

## Commands

| Command | Description | Usage |
|---------|-------------|--------|
| `!play <query>` | Play a song or playlist | `!play Never Gonna Give You Up` |
| `!pause` | Pause the current track | `!pause` |
| `!resume` | Resume the current track | `!resume` |
| `!skip` | Skip the current track | `!skip` |
| `!stop` | Stop playback and clear queue | `!stop` |
| `!queue` | Show the current queue | `!queue` |
| `!nowplaying` | Show current track info | `!nowplaying` |
| `!volume <0-100>` | Adjust player volume | `!volume 50` |
| `!shuffle` | Shuffle the current queue | `!shuffle` |
| `!loop` | Toggle queue loop mode | `!loop` |
| `!remove <position>` | Remove a track from queue | `!remove 1` |
| `!clear` | Clear the current queue | `!clear` |
| `!status` | Show player status | `!status` |
| `!help` | Show this help message | `!help` |

## Screenshots

### Now Playing
![Now Playing](https://i.imgur.com/PMmebc2.png)

### Queue List
![Help Menu](https://i.imgur.com/n7uBEvU.png)

### Player Status
![Player Status](https://i.imgur.com/0JhhPo3.png)

## Prerequisites

- Node.js 16.9.0 or higher
- Java 11 or higher (for Lavalink)
- A Discord Bot Token
- Spotify API credentials (optional, for Spotify support)

## Installation

1. Clone the repository:
```bash
git clone https://github.com/friday2su/music-bot.git
cd music-bot
```

2. Install dependencies:
```bash
npm install
```

3. Download and set up Lavalink:
   - Download the latest Lavalink.jar from [GitHub](https://github.com/freyacodes/Lavalink/releases)
   - Create an `application.yml` file in the same directory as Lavalink.jar
   - Add the following configuration:
```yaml
server:
  port: 2333
  address: 127.0.0.1
spring:
  main:
    banner-mode: log
lavalink:
  server:
    password: "youshallnotpass"
    sources:
      youtube: true
      bandcamp: true
      soundcloud: true
      twitch: true
      vimeo: true
      http: true
    bufferDurationMs: 400
    youtubePlaylistLoadLimit: 6
    playerUpdateInterval: 5
    youtubeSearchEnabled: true
    soundcloudSearchEnabled: true
```

4. Configure the bot:
   - Copy `config.example.js` to `config.js`
   - Fill in your bot token and other settings:
```javascript
module.exports = {
    prefix: '!',
    nodes: [{
        host: "localhost",
        password: "youshallnotpass",
        port: 2333,
        secure: false,
        name: "Main Node"
    }],
    spotify: {
        clientId: "YOUR_SPOTIFY_CLIENT_ID",
        clientSecret: "YOUR_SPOTIFY_CLIENT_SECRET"
    },
    botToken: "YOUR_BOT_TOKEN",
    embedColor: "#FF0000"
};
```

5. Start Lavalink:
```bash
java -jar Lavalink.jar
```

6. Start the bot:
```bash
npm start
```

## Support

If you encounter any issues or have questions, please:
1. Check the [Issues](https://github.com/friday2su/music-bot/issues) page
2. Join our [Discord Server](https://discord.gg/EWr3GgP6fe)
3. Create a new issue if needed

## Contributing

Contributions are welcome! Please feel free to submit a Pull Request.

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## Credits

- [Discord.js](https://discord.js.org/)
- [Riffy](https://github.com/riffy-team/riffy)
- [Lavalink](https://github.com/freyacodes/Lavalink)
- [Spotify API](https://developer.spotify.com/)

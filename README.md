# RandomBACAPChallenges

A Minecraft plugin that adds random achievement challenges from the BlazeandCave's Advancement Pack (BACAP). Perfect for adding variety and goals to your survival gameplay!

## Features

- **Random Challenges**: Get random advancement challenges from BACAP
- **Global Challenges**: Server-wide challenges for multiplayer fun
- **BACAP Coop Support**: Works seamlessly with BACAP's built-in coop mode
- **Built-in Timer**: An optinal Timer to track time played
- **Component Tracking**: View detailed progress with sidebar and GUI displays
- **Multi-language**: Full support for English and German
- **Category Colors**: Color-coded challenges by advancement category
- **Flexible Filtering**: Exclude categories, specific achievements, or use regex patterns

## Requirements

- Minecraft Server 1.21.8 (Paper/Spigot)
- [BlazeandCave's Advancement Pack](https://modrinth.com/datapack/blazeandcaves-advancements-pack) datapack
- Java 17+
- A Texture Pack that disableds the Bossbar, I used [Invisible Boss Bars](https://modrinth.com/resourcepack/invisible-bars)

## Installation

1. Download the latest release
2. Place the `.jar` file in your server's `plugins` folder
3. Install BACAP datapack in your world's `datapacks` folder
4. Restart your server
5. Configure the plugin in `plugins/RandomBACAPChallenges/config.yml`

## Commands

### Main Commands
- `/challenge start` - Start a new personal challenge
- `/challenge next` - Skip to the next challenge
- `/challenge stop` - Stop current challenge
- `/challenge status` - Show current challenge status

### Global Challenges
- `/challenge global start` - Start a server-wide challenge
- `/challenge global next` - Skip to next global challenge
- `/challenge global stop` - Stop global challenge
- `/challenge global skip` - Vote to skip current global challenge

### Timer
- `/timer start` - Start personal timer
- `/timer stop` - Stop timer
- `/timer status` - Show timer status
- `/timer reset` - Reset timer

### Components
- `/challenge components true/false` - Enable/disable sidebar component tracking
- `/challenge components gui` - Open component tracking GUI

## Configuration

The plugin automatically creates a `config.yml` with extensive customization options:

```yaml
# Language settings
language: en  # or 'de' for German

# Filter which challenges appear
filter:
  only_categories: []  # If set, only these categories will be used
  exclude_categories:  # Categories to exclude
    - statistics
  exclude_ids: []      # Specific advancement IDs to exclude
  exclude_prefixes: [] # Exclude by ID prefix
  exclude_regex: []    # Exclude using regex patterns

```

## BACAP Coop Mode Integration

When you activate the coop mode in the BACAP datapack, this plugin works perfectly with it:

- **Global Challenges**: Perfect for coop play since all players share achievements
- **Personal Challenges**: Still work individually even in coop mode
- **Seamless Integration**: No additional configuration needed


## Troubleshooting

### Common Issues

**Plugin says "BACAP datapack not found"**
- Ensure BACAP is installed in `world/datapacks/`
- Check that the datapack folder contains "blazeandcave" or "bacap" in the name

**No challenges available after filtering**
- Check your filter settings in `config.yml`
- Verify that your filters aren't too restrictive

**Timer not working correctly**
- Try `/timer reset` to fix timer state issues
- Check server logs for any error messages


## Permissions

- `randombacap.use` - Use challenge commands (default: true)
- `randombacap.timer` - Use timer commands (default: true)



## Support

- **Issues**: This is my first Plugin so please report bugs or request features on the [GitHub Issues page](


## License

This project is licensed under the MIT License - see the LICENSE file for details.

## Credits

- **Cavinator1** for the amazing advancement pack
- **Minecraft Community** for feedback and testing

---

*Made with ❤️ for the Minecraft community*

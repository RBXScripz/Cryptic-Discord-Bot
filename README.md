# Discord Moderation Bot

A comprehensive Discord bot with moderation tools, entertainment features, and an economy system.

## Features

### Moderation
- Warning system
- Auto-moderation (spam, caps, links, invites)
- Banned words filter
- Kick/Ban commands
- Message purging
- Logging system

### Entertainment
- Giveaways with flexible duration formats (e.g., "1 minute", "1 hour", "1 day")
- 8ball command
- Rock, Paper, Scissors
- Random jokes
- Inspirational quotes

### Economy
- Virtual currency system
- Work command
- Gambling games (coinflip, slots)
- Payment system between users
- Economy leaderboard

### Role Management
- Role creation/deletion
- Role assignment
- Permission checks

## Setup Instructions

1. Clone or download this repository
2. Install Python 3.11 or higher
3. Install dependencies:
   ```bash
   pip install -r requirements.txt
   ```
4. Create a `.env` file in the root directory with your Discord bot token:
   ```
   DISCORD_TOKEN=your_bot_token_here
   ```
5. Run the bot:
   ```bash
   python main.py
   ```

## Configuration

Edit `config.py` to customize:
- Command prefix
- Economy settings (cooldowns, amounts)
- Moderation settings (max warnings, mute role)

## Project Structure

```
├── cogs/
│   ├── economy.py      # Economy system
│   ├── entertainment.py # Fun commands
│   ├── logs.py         # Logging system
│   ├── moderation.py   # Moderation commands
│   └── roles.py        # Role management
├── utils/
│   ├── logger.py       # Logging utility
│   └── json_manager.py # JSON data management
├── data/               # JSON storage
├── logs/              # Log files
├── config.py          # Bot configuration
├── main.py            # Bot entry point
└── requirements.txt   # Dependencies
```

## Commands

All commands use slash command format (`/`):

### Moderation
- `/warn <user> [reason]` - Warn a user
- `/kick <user> [reason]` - Kick a user
- `/ban <user> [reason]` - Ban a user
- `/clear <amount>` - Clear messages
- `/automod enable/disable` - Toggle auto-moderation

### Entertainment
- `/giveaway <prize> <duration> [winners]` - Start a giveaway
- `/8ball <question>` - Ask the magic 8-ball
- `/rps <choice>` - Play rock, paper, scissors
- `/joke` - Get a random joke
- `/quote` - Get an inspirational quote

### Economy
- `/balance` - Check your balance
- `/work` - Earn coins
- `/coinflip <amount>` - Gamble with coins
- `/slots <amount>` - Play slot machine
- `/pay <user> <amount>` - Send coins to another user
- `/leaderboard` - View richest users

### Roles
- `/role add <user> <role>` - Add role to user
- `/role remove <user> <role>` - Remove role from user
- `/role create <name>` - Create new role
- `/role delete <role>` - Delete role

## License

This project is licensed under the MIT License.

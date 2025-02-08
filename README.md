# Maestro Mystery Box Bot

## Overview
The Maestro Mystery Box Bot is a Telegram bot that allows users to claim daily prizes through randomly generated links. The bot manages a prize pool, tracks winners, and ensures fair distribution of rewards.

## Features
- Automatically generates and distributes prize links daily.
- Ensures a maximum number of winners per day.
- Tracks claimed prizes and prevents duplicate claims.
- Allows admin to manually send prize links.
- Provides commands for managing winners and resetting the prize pool.
- Logs bot activity for monitoring and debugging.

## Requirements
- Python 3.8+
- Telegram Bot API
- Required libraries:
  - `python-telegram-bot`
  - `pytz`
  - `secrets`
  - `random`
  - `logging`

## Installation
1. Clone the repository:
   ```bash
   git clone https://github.com/your-repo/maestro-mystery-box-bot.git
   ```
2. Install required dependencies:
   ```bash
   pip install -r requirements.txt
   ```
3. Set up your bot token in the script:
   ```python
   BOT_TOKEN = "your-telegram-bot-token"
   ```

## Usage
### Starting the Bot
Run the bot using:
```bash
python bot.py
```

### Available Commands
| Command | Description |
|---------|-------------|
| `/start` | Initializes the bot (admin only). |
| `/start_mmb` | Starts sending daily prize links (admin only). |
| `/stop_mmb` | Stops the bot from sending links (admin only). |
| `/send_mmb` | Manually sends a prize link (admin only). |
| `/winners_mmb` | Displays the list of current winners (admin only). |
| `/reset_mmb` | Resets all winners and the prize pool (admin only). |
| `/restart_mmb` | Restarts the bot (admin only). |
| `/help` | Displays the list of available commands. |
| `/test_mmb` | Shows bot status (admin only). |

## Prize Distribution
- The bot generates a unique token for each prize link.
- Users can claim a prize by clicking the generated link.
- A maximum of 10 winners per day is enforced.
- Prizes are randomly selected from a predefined list.

## Admin Controls
- Only the admin (specified by `ADMIN_ID`) can start, stop, or reset the bot.
- The admin can manually send a prize link if needed.

## Logging
The bot logs its activity, including:
- Prize distribution.
- Winner claims.
- Errors and exceptions.

## Notes
- Ensure that the bot is added to the target Telegram group.
- Modify `ADMIN_ID` to match the Telegram user ID of the administrator.
- Update the `available_prizes` list in the script as needed.

## License
This project is open-source. Feel free to modify and improve it!

## Contact
For support or questions, contact @CrypticKimo on Telegram.


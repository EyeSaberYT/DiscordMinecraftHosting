# Discord Minecraft Hosting Request Bot

A Discord bot that allows users to submit requests for free Minecraft server hosting using slash commands, with support for multiple servers and player slots allocation.

## Features

- Users can request free Minecraft hosting through a modal form using `/request` command
- Request form includes both server count and player slots specification
- Admins can review, approve, or deny requests
- Automatic tracking of server allocations per user
- Manual allocation updates with `/update` command
- Check current allocations with `/check` command
- Automatic notifications to users when their request is processed

## Setup

1. Clone this repository
2. Install dependencies with `npm install`
3. Create a `.env` file with your Discord bot token and client ID:
   ```
   DISCORD_TOKEN=your_discord_bot_token_here
   CLIENT_ID=your_application_client_id_here
   ```
4. Deploy slash commands with `npm run deploy`
5. Start the bot with `npm start`

## Usage

### For Users
- Type `/request` in any channel to get a button for requesting hosting
- Fill out the form with your server details, including:
  - Number of servers needed
  - Number of player slots needed per server
- You'll receive a DM when your request is approved or denied

### For Admins
- Review requests in the #hosting-requests channel
- Approve or deny requests with the buttons
- Update allocations manually with `/update @user servers slots`
- Check current allocations with `/check @user`

## Allocation System

The bot automatically tracks server allocations for each user in a JSON file. When a request is approved, the allocation is automatically updated. Admins can also manually update allocations using the `/update` command.

## Troubleshooting

If you encounter errors:

1. Make sure your bot has the correct permissions in the server
2. Check that your `.env` file contains the correct token and client ID
3. Ensure you've deployed the commands with `npm run deploy` before starting the bot
4. Check the console for specific error messages

## Requirements

- Node.js v16.9.0 or higher
- Discord.js v14

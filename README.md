
# AutoSpinLoofi


## Requirements

- Node.js 14.0.0 or higher
- Valid Stork Oracle account

## Installation

1. Clone the repository:
```
git clone https://github.com/airdropinsiders/Stork-Auto-Bot.git
```

2. Navigate to the project directory:
```
cd Stork-Auto-Bot
```

3. Install dependencies:
```
npm install
```

4. Configure your credentials (see Configuration section below)

## Configuration

### Easy Setup with account.js

The bot now uses a account.js file for credentials. 

1. Edit the generated `accounts.js` file with your credentials:
```javascript
export const accounts = [
  { username: "email1", password: "pass1" },
  { username: "email2", password: "pass2" }
];
```

2. Replace `username` and `password` with your Stork Oracle account credentials.
just add new line if you wanna run many accounts

3. Run the bot :
```
node index.js
```

### Optional: Proxy Configuration

To use proxy servers for distribution of requests:

1. Create a `proxies.txt` file in the project root
2. Add one proxy per line in any of these formats:
   - HTTP proxies: `http://user:pass@host:port`
   - SOCKS proxies: `socks5://user:pass@host:port`

## Usage

Start the bot with:
```
node index.js
```

The bot will:
1. Authenticate using your credentials from account.js
2. Fetch signed price data at regular intervals
3. Validate each data point
4. Submit validation results to Stork Oracle
5. Display your current statistics

## Advanced Configuration Options

In your `config.json` file, you can adjust:

- `stork.intervalSeconds`: How often the validation process runs in seconds (default: 5)
- `threads.maxWorkers`: Number of concurrent validation workers (default: 1)

## Troubleshooting

- If you see authentication errors, check that your username and password in config.json are correct
- If the bot fails to start, ensure your config.json file is properly formatted JSON
- If you see token-related errors after successful authentication, the tokens.json file may be corrupted - delete it and let the bot regenerate it
- For connection issues, check your internet connection and verify the Stork Oracle API is accessible
- If using proxies, check that your proxies.txt is properly formatted and proxies are operational

## Disclaimer

This bot is provided for educational purposes only. Use at your own risk. The authors are not responsible for any consequences that may arise from using this bot, including but not limited to account termination or loss of rewards.

## License

MIT License

## Contributing

Contributions are welcome! Please feel free to submit a Pull Request.

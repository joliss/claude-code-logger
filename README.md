# Claude Code API Logger

A simple tool to log API calls made by the Claude Code CLI to Anthropic's API.

## Disclaimer

**FOR RESEARCH PURPOSES ONLY**

This tool is provided strictly for research and educational purposes only. By using this software, you agree to the following:

1. The author makes no warranties or representations of any kind concerning this software and accepts no liability for its use.
2. The author assumes no responsibility whatsoever for any consequences arising from the use of this tool.
3. Users are solely responsible for ensuring their use of this tool complies with all applicable laws, regulations, and Anthropic's terms of service.
4. This tool is not officially affiliated with, authorized, maintained, sponsored, or endorsed by Anthropic or any of its affiliates.

Use at your own risk.

This project itself was developed with [Claude Code](https://claude.ai/code).

## Installation

### Global Installation (recommended)

```bash
npm install -g .
```

This will make the `claude-log` command available globally.

### Local Installation

```bash
npm install .
```

## Usage

```bash
claude-log [options] [claude options]
```

All arguments after the options are passed directly to the Claude CLI.

### Options

- `--log_dir=DIR`: Directory to save logs (default: ~/.claude_logs)
- `--save-responses`: Also save response data (default: off)
- `--print`: Show debug messages (default: off)

### Examples

```bash
# Basic usage - run Claude with API logging
claude-log

# Run Claude with a prompt
claude-log -p "What is Rust and why do people care?"

# Save both requests and responses
claude-log --save-responses

# Specify a custom log directory
claude-log --log_dir=/path/to/logs
```

## Setting up an alias

For even easier usage, you can set up a shell alias:

### Bash/ZSH

Add to your `.bashrc` or `.zshrc`:

```bash
alias claude='claude-log'
```

### Fish shell

```fish
alias claude='claude-log'
funcsave claude
```

This lets you use `claude` as normal, but with all API calls logged.

## Log Files

Logs are stored in `~/.claude_logs` by default, organized by timestamp.

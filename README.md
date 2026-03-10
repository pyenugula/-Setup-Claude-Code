Claude Code + Ollama Integration (Local Models)
This guide explains how to install Ollama, pull the gpt-oss model, install Claude Code, and run it locally.
Step 1: Install Ollama on macOS
Run the installation script:
curl -fsSL https://ollama.com/install.sh | sh
Expected output:
Stopping running Ollama instance...
Removing existing Ollama installation...
Downloading Ollama for macOS... 100%
Installing Ollama to /Applications...
Starting Ollama...
Install complete. You can now run 'ollama'.
Verify the installation:
ollama --version
⚠ Warning about connecting to a running instance is normal on first run.

Step 2: Pull the GPT-OSS Model
Use Ollama to pull the model locally:
ollama pull gpt-oss:20b
Sample output:
pulling manifest
pulling e7b273f96360: 100% ▏█████████ 13 GB
pulling fa6710a93d78: 100% ▏███████ 7.2 KB
...
verifying sha256 digest
writing manifest
success

Step 3: Install Claude Code
Run the official installation script:
curl -fsSL https://claude.ai/install.sh | bash
Installation summary:
Setting up Claude Code...
✔ Claude Code successfully installed!
Version: 2.1.52
Location: ~/.local/bin/claude
Next: Run 'claude --help' to get started
Important: Add Claude to your PATH:
echo 'export PATH="$HOME/.local/bin:$PATH"' >> ~/.zshrc
source ~/.zshrc

Step 4: Run Claude with Ollama
Launch Claude using the local GPT-OSS model:
ollama launch claude --model gpt-oss:20b
You are now ready to use Claude Code locally with the gpt-oss 20B model!
✅ Notes
Make sure Ollama is installed and running before launching Claude.
Local models like gpt-oss:20b require sufficient disk space (~13 GB) and memory.
Add ~/.local/bin to PATH to avoid command not found errors.

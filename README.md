Step 1: Install Ollama on macOS
Run the installation script:

curl -fsSL https://ollama.com/install.sh | sh

Stopping running Ollama instance...
Removing existing Ollama installation...
Downloading Ollama for macOS... 100%
Installing Ollama to /Applications...
Starting Ollama...
Install complete. You can now run 'ollama'.

ollama --version

Step 2: Pull the GPT-OSS Model
Use Ollama to pull the model locally:

ollama pull gpt-oss:20b

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

imstallation summary :

Setting up Claude Code...
✔ Claude Code successfully installed!
Version: 2.1.52
Location: ~/.local/bin/claude
Next: Run 'claude --help' to get started

echo 'export PATH="$HOME/.local/bin:$PATH"' >> ~/.zshrc
source ~/.zshrc

Step 4: Run Claude with Ollama
Launch Claude using the local GPT-OSS model:

ollama launch claude --model gpt-oss:20b

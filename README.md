# Setup-Claude-Code
Claude Code integration with Ollama and launching it using local models like gpt-oss


Step1: Install ollama in macos

curl -fsSL https://ollama.com/install.sh | sh

 ~   main ● ?  curl -fsSL https://ollama.com/install.sh | sh                                                                            
>>> Stopping running Ollama instance...
>>> Removing existing Ollama installation...
>>> Downloading Ollama for macOS...
######################################################################## 100.0%
>>> Installing Ollama to /Applications...
>>> Starting Ollama...
>>> Install complete. You can now run 'ollama'.

 ~   main ● ?  ollama --version                                                                                                        
Warning: could not connect to a running Ollama instance
Warning: client version is 0.17.0


step2: Pull the model 

ollama pull gpt-oss:20b 

ollama pull gpt-oss:20b                                                                                                     ✔  10484  08:57:23 
pulling manifest 
pulling e7b273f96360: 100% ▕███████████████████████████████████████████████████████████████████████████████████████████████████████▏  13 GB                         
pulling fa6710a93d78: 100% ▕███████████████████████████████████████████████████████████████████████████████████████████████████████▏ 7.2 KB                         
pulling f60356777647: 100% ▕███████████████████████████████████████████████████████████████████████████████████████████████████████▏  11 KB                         
pulling d8ba2f9a17b3: 100% ▕███████████████████████████████████████████████████████████████████████████████████████████████████████▏   18 B                         
pulling 776beb3adb23: 100% ▕███████████████████████████████████████████████████████████████████████████████████████████████████████▏  489 B                         
verifying sha256 digest 
writing manifest 
success 


step3: Intall Claude

curl -fsSL https://claude.ai/install.sh | bash

curl -fsSL https://claude.ai/install.sh | bash                                                                              ✔  10486  09:06:20 
Setting up Claude Code...

✔ Claude Code successfully installed!        
                                                                         
  Version: 2.1.52
                                                                            
  Location: ~/.local/bin/claude


  Next: Run claude --help to get started

⚠ Setup notes:
  • Native installation exists but ~/.local/bin is not in your PATH. Run:

  echo 'export PATH="$HOME/.local/bin:$PATH"' >> ~/.zshrc && source ~/.zshrc


✅ Installation complete!


step4: Run Claude with ollama

ollama launch claude --model gpt-oss:20b

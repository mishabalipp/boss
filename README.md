import os
import subprocess

# Set up API key
os.environ["OPENAI_API_KEY"] = "your_api_key_here"

# Install Garak if not installed
try:
    import garak
except ImportError:
    subprocess.run(["pip", "install", "garak"])

# Run Garak against a model
subprocess.run(["garak", "openai:gpt-3.5-turbo"])

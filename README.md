import os
import random
import datetime

# List of random commit messages
messages = [
    "Updating progress 🚀",
    "Working on something cool 💡",
    "Keeping the streak alive 🔥",
    "Small improvement 🛠",
    "Daily update 📅",
    "Refactoring code ✨",
    "Pushing some changes 💻",
    "Maintenance update 🔧",
    "Code tweak ⚡",
    "New idea implemented 💭",
    "Optimizing performance 🚄",
    "Fixing minor issues 🐛",
    "Polishing code ✨",
    "Testing new features 🧪",
    "Improving stability 🔒"
]

# Pick a random message
msg = random.choice(messages)

# Append to log file
with open("activity_log.txt", "a", encoding="utf-8") as f:
    f.write(f"{datetime.datetime.now()}: {msg}\n")

# Run git commands
os.system("git add activity_log.txt")
os.system(f'git commit -m "{msg}"')
os.system("git push")

print(f"✅ Commit pushed with message: {msg}")

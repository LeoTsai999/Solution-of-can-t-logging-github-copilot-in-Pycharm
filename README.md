# Solution-of-can-t-logging-github-copilot-in-Pycharm

The author is using a MacBook Air M1 (2020) with macOS Sequoia.
When attempting to install GitHub Copilot in PyCharm, the following error occurred:

"""
The login to GitHub failed. Reason: Error: EACCES: permission denied, mkdir '/Users/tsaizixiang/.config/github-copilot', request id: 6, error code: 1001
"""

Problem Analysis:

The issue arises because Copilot does not have sufficient permissions to create a required folder.

Solution:

Run the following commands sequentially in the terminal:

"""
sudo mkdir -p /Users/tsaizixiang/.config/github-copilot 
sudo chmod -R 700 /Users/tsaizixiang/.config/github-copilot 
sudo chown -R tsaizixiang /Users/tsaizixiang/.config/github-copilot 
"""

After completing these steps, try logging into Copilot again, and it should work properly.

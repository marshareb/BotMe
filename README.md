# BotMe
A simple module for making and using bots on GroupMe with Python.

# How to use
If you have not made a bot yet, start by using bot = Manager(GROUPME_KEY) and then use the create_bot command with
the group name and the bot name you want. If you already have a bot for that group, Manager will select that bot instead.
After creating a bot, there are three core commands -- bot.post_message, bot.retrieve_message(), and bot.post_picture().
The names are pretty self explanatory. In order to use bot.post_picture(), make sure you have the image saved in the
folder with the bot code.


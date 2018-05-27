# BotMe
A simple module for making and using bots on GroupMe with Python.

# How to install

You can now install BotMe by running

```
pip install BotMe
```

# How to use

First, import BotMe by running
```
import BotMe.main as Bot
```

## Initializing the Bot

In order to initialize the bot, you run
```
bot = Bot.Manager('GROUPME_KEY_HERE')
```

In order to find your GroupMe Key, go to https://dev.groupme.com/ and sign in.
In the top right, there should be a tab title 'Access Token.' Press this, and your
token will pop up.

## Creating a Bot

In order to create a bot, you run
```
bot.create_bot('BOT_NAME', 'GROUP_NAME')
```

So, for example, if I wanted to make a bot named Test in the group
groupTest, I would run

```
bot.create_bot('Test', 'GroupTest')
```

If there is already a bot in the group, it will select the bot instead
of making a new one.

## Starting a Bot

If you already have a bot made, you can access it by running

```
bot.start_bot('BOT_NAME')
```

## Posting a Message

With the bot now made, you can post a message with it by running

```
bot.post_message('MESSAGE TEXT HERE')
```

## Retrieving a Message

If you want to retrieve a message, you would run

```
bot.retrieve_message()
```

Retrieving a message returns a tuple of information of the form (nickname, message).
So, if you wanted to see the nickname of the person who posted the most recent message, you would run

```
bot.retrieve_message()[0]
```

and if you wanted to see the message itself, you would run

```
bot.retrieve_message()[1]
```

## Posting a Picture

With the picture in the same directory, to post an image all you have to do is run

```
bot.post_picture('picture_name', 'message')
```

The message portion of this function is optional. If your image is not in the same directory,
replace 'picture_name' with a path to the picture itself.

## Retrieving Members

With the bot started, you can also see who is in the group. To do so, simply cal

```
bot.retrieve_members()
```

A list with the nicknames of all the members will be returned.

## Example

For a good example of BotMe in action, check out my Latex Bot for GroupMe at
https://github.com/marshareb/latex_bot
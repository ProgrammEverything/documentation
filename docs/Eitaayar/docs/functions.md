---
layout: default
title: "Functions"
parent: "EitaaYar"
nav_order: 3
---
## Functions
(All of the arguments are flags for the EitaaYar API)
- SendMessage: Send a message to the EitaaYar API by the arguments
- ASendMessage: asynchronously Send a message using aiohttp (Needs a ClientSession)
- SendFile: Send a file using the requests package
- ASendFile: asynchronously Send a file using the aiohttp package
- GetMe: Get information about the bot
- GetJSON: Process a JSON object to send a message or file
```python
[
    {
        "type":"MSG", #Type of the message(IMG,MSG) for the according function
        "args":{      #Arguments of the function type
            "text":"Hello, World!" #Hello world message
        }
    }, 'Message_Title'] #Title of the message
```
This sends a message to the eitaayar API with the text: 
Title: Message_Title \
Hello, World! \
As you can see the Message_Title the second item of the list is our title. It will add a "TITLE: ...\n" to the top of the text and then add the other text.
Notice that the message is inside a list of two, this is because you only send 1 message at a time in this function.
Example code: \
```python
import EitaaAPI
session = EitaaAPI.Session("YOUR_API_KEY", "YOUR_CHAT_ID")
session.SendMessage("Example Message")
```
The SendMessage function has other flags such as disable_notification which is a flag for the EitaaAPI
#### Original documentation from [Repo](https://github.com/ProgrammEverything/EitaaAPI/blob/main/README.md) <a>(README.md)</a>
---
icon: message-bot
---

# APIMyLlama Commands

### Commands



These are the commands you can use in the APIMyLlama application

```
generatekey
```

This command will generate a key using Cryptography and save it to the local database.

```
listkey
```

This command will list all API Keys in the database.

```
removekey <API_KEY>
```

This command will remove any key from the database.

```
addkey <API_KEY>
```

You can add custom keys if wanted. (DO with CAUTION as it may be unsafe)

```
changeport <SERVER_PORT>
```

You can change the servers port in realtime without having to restart the application.

```
changeollamaurl <YOUR_OLLAMA_SERVER_URL>
```

You can change the Ollama Server url if you have a custom one set. By default it is "[http://localhost:11434](http://localhost:11434/)".

```
addwebhook <YOUR_WEBHOOK>
```

You can add webhooks for alerts when a new request is made. EX. Discord Webhook

```
listwebhooks
```

This command will list all the webhooks you have attached to your system.

```
deletewebhook <ID_OF_WEBHOOK_IN_DATABASE>
```

This command can be used to remove a webhook in your system. You can get the ID of the webhook using the 'listwebhooks' command.

```
ratelimit <API_KEY> <RATE_LIMIT>
```

This command allows you to change the ratelimit on a key. By default it is 10. The rate limit is by minute. So for example the default allows 10 requests to the API per minute.

```
deactivatekey <API_KEY>
```

Allows you to deactivate an API key. This will make the key useless untill it is activated.

```
activatekey <API_KEY>
```

Activates a API key that has been deactivated in the past.

```
addkeydescription <API_KEY>
```

This command lets you add a description to a key to help you decipher what key does what.

```
listkeydescription <API_KEY>
```

This command lists the description of that key if it has a description.

```
generatekeys <number>
```

Quickly generate multiple new API keys.

```
regeneratekey <API_KEY>
```

Regenerate any specified API key without affecting other details.

```
activateallkeys
```

Activate all your API keys with a single command.

```
deactivateallkeys
```

Deactivate all your API keys with a single command.

```
getkeyinfo <API_KEY>
```

Retrieve detailed information about a specific API key.

```
listactivekeys
```

Easily list all active API keys.

```
listinactivekeys
```

Easily list all inactive API keys.

\

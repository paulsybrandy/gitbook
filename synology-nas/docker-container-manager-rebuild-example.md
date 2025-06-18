---
description: >-
  Frequently used set of commands to stop, delete, and rebuild a Docker
  container on my Synology NAS.
---

# Docker (Container Manager) rebuild example

```bash
sudo docker stop ai-assistant
sudo docker rm ai-assistant
sudo docker build -t ai-assistant .
sudo docker run -d \
  --name ai-assistant \
  -p 8080:5000 \
  -v $(pwd)/credentials.json:/app/credentials.json:ro \
  -v $(pwd)/token.json:/app/token.json:rw \
  --restart unless-stopped \
  ai-assistant
```

{% hint style="warning" %}
**Note**: The first command may need to be separated from the code block as a whole because it will ask for the root password, which, if the whole code block is copied and pasted, will put the second line in automatically as the root password.
{% endhint %}

docker# Jenkins

## 1. ssh access :

```bash
docker exec -it -u root jenkins bash
chown jenkins:jenkins /tmp/remote-key
exit

docker exec -it jenkins bash
# auto login without asking the pwd
ssh -i /tmp/remote-key remote_user@remote_host
```

## 2. fix mac ssh issue

```bash
generate ssh from mac
ssh-keygen -t rsa -m PEM -f remote-key
```
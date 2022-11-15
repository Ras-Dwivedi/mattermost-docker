https://mattermost.com/deploy/

```
git clone https://github.com/mattermost/docker && cd docker
cp env.example .env
DOMAIN=mm.example.com
mkdir -p ./volumes/app/mattermost/{config,data,logs,plugins,client/plugins,bleve-indexes} && sudo chown -R 2000:2000 ./volumes/app/mattermost
sudo docker-compose -f docker-compose.yml -f docker-compose.without-nginx.yml up -d
```

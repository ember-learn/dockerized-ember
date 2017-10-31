# Docker Image for emberjs.com development

### Setup with docker-compose

```yml
# docker-compose.yml
version: '2'
services:
  guides:
    image: emberjs/website-dev
    command: bundle exec middleman
    ports:
      - "4567:4567"
    volumes:
      - .:/src
```


```bash
# In a terminal:
docker-compose build
docker-compose up
```

Then you can navigate to http://localhost:4567 in your browser to view the website project served via middleman.

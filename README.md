# tell-me-a-joke-rasa-intro

```sh
 docker run -v $(pwd):/app rasa/rasa:3.6.0-full init --no-prompt
 docker build . -t ehz-rasa-sdk:0.1
 docker network create my-project
 docker run -it -v $(pwd):/app -p 5005:5005 --net my-project rasa/rasa:3.6.0-full interactive
 docker run -v $(pwd):/app rasa/rasa:3.6.0-full train
 docker ps
 docker stop action-server
 docker rm action-server
 docker run -d -v $(pwd)/actions:/app/actions --net my-project --name action-server ehz-rasa-sdk:0.1
 docker run -it -v $(pwd):/app -p 5005:5005 --net my-project rasa/rasa:3.6.0-full shell
```

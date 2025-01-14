### DOCKER BUILD, TAG AND PUSH

```sh
cd /Users/epabishai/apps/artofthepossible/customers/pnc/whale-of-a-time
docker build -t demonstrationorg/bank-demo-whale-of-a-time:v1.0 .
docker tag demonstrationorg/bank-demo-whale-of-a-time:v1.0 demonstrationorg/bank-demo-whale-of-a-time:v1.0
docker push demonstrationorg/bank-demo-whale-of-a-time:v1.0
docker compose up -d

or
docker buildx build --builder cloud-demonstrationorg-default -t demonstrationorg/bank-whale-of-a-time:v1.0 .
or

docker build -t demonstrationorg/bank-demo-whale-of-a-time:v1.0 . && \
docker push demonstrationorg/bank-demo-whale-of-a-time:v1.0 && \
docker compose up --build

```
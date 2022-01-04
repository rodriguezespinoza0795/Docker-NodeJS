<!-- Build image -->
docker build --tag node-docker .
<!-- Run in detached mode -->
docker run -d -p 8000:8000 node-docker
<!-- Use Compose to develop locally -->
docker-compose -f docker-compose.dev.yml up --build
<!-- Use Compose to develop locally and run tests -->
docker-compose -f docker-compose.dev.yml run notes npm run test
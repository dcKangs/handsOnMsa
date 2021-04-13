# docker build
docker build -t product-service .
docker build -t review-service .
docker build -t recommendation-service .
docker build -t product-composite-service .

# docker test
docker run -it -d --name product-service -p 8080:8080 -e "SPRING_PROFILES_ACTIVE=docker" product-service

# docker compose
docker-compose up


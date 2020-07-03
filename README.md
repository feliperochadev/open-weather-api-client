# open-weather-api-client
Java Rest Client for https://openweathermap.org/
* There are 3 cities for the get weather endpoint:
* Berlin
* Paris
* London
* You can change them on application.yml config

# Running project locally in Docker
* Build Docker image: `docker build -t open-weather-api-client .`
* Run image: `docker run -p 8080:8080 -e JAVA_XMS='256m' -e JAVA_XMX='256m' -e JAVA_PERM='128m' --name openweatherapiclient open-weather-api-client:latest`

# Api Doc
* access {service.url}/swagger-ui.html

# cURL requests
* get weather:
`curl -X GET \
  http://localhost:8080/weather/Berlin`
* get weather forecast for 5 days:
`curl -X GET \
  http://localhost:8080/weather/rome/forecast`
* get weather info for the 3 cities:
`curl -X GET \
  http://localhost:8080/weather/cities`

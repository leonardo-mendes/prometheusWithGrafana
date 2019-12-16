 ### Prometheus application
 
 Run the application
   
 ```
 ./gradlew clean bootRun 
 ``` 
 
 Its's necessary a prometheus image.
 
 ```
docker pull prom/prometheus 
 ``` 
 
 We should configure a prometheus.yml to set up on prometheus docker image.
   
 ```
docker run -p 9090:9090 -v yourPath/prometheus.yml prom/prometheus 
 ``` 
 
 After that, we should to run Grafana.
 
  ```
 docker run -d --name=grafana -p 3000:3000 grafana/grafana
  ``` 
 
 Will be necessary configure the database custom on Grafana, we can use localhost:9000 (Local Prometheus).

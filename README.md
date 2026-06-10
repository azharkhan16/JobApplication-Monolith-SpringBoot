=================== Job Functionalities & APIs ===========================
1) findAll() => GET -> http://localhost:8080/jobs 
2) createJob() => POST -> http://localhost:8080/jobs
3) getJobById() => GET -> http://localhost:8080/jobs/{jobId}
4) deleteJob() => DELETE -> http://localhost:8080/jobs/{jobId}
5) updateJob() => PUT -> http://localhost:8080/jobs/{JobId}

================== Company Functionalities & APIs ========================
1) getAllCompanies() => GET -> http://localhost:8080/companies
2) addCompany() => POST -> http://localhost:8080/companies
3) getCompanyById() => GET -> http://localhost:8080/companies/{companyId}
4) deleteCompany() => DELETE -> http://localhost:8080/companies/{companyId}
5) updateCompany() => PUT -> http://localhost:8080/companies/{companyId}

=============================== Review Functionalities & APIs ===============================
1) getAllReviews() => GET -> http://localhost:8080/companies/{companyId}/reviews
2) addReview() => POST -> http://localhost:8080/companies/{companyId}/reviews
3) getReview() => GET -> http://localhost:8080/companies/{companyId}/reviews/{reviewId}
4) deleteReview() => DELETE -> http://localhost:8080/companies/{companyId}/reviews/{reviewId}
5) updateReview() => PUT -> http://localhost:8080/companies/{companyId}/reviews/{reviewId}


====================== Monitoring with Spring Boot Actuator =====================

Added Spring Boot Actuator to enable actuator endpoints, health monitoring and
manage the application 

### Actuator Endpoints
1) http://localhost:8080/actuator/health -> Application health status
2) http://localhost:8080/actuator/info -> Application information
3) http://localhost:8080/actuator/metrics -> Application metrics
4) http://localhost:8080/actuator/metrics/{requiredMetricName} -> check metrics with name
5) http://localhost:8080/actuator/env -> Environment properties
6) http://localhost:8080/actuator/mappings -> Available API endpoints

### Configurations added in application.properties
management.endpoints.web.exposure.include=*
management.endpoint.health.show-details=always

### info configurations
management.info.env.enabled=true
info.app.name=JobApplication
info.app.description=Job app built by codeX-Azhar
info.app.version=1.0.0

### graceful shutdown configuration
management.endpoint.shutdown.enabled=true
server.shutdown=graceful

### Change Log Level at Runtime
1) POST -> http://localhost:8080/actuator/loggers/com.azharx.jobapplication  <-app name
2) Body -> JSON
3) {
   "configuredLevel": "DEBUG"
   }
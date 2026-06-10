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
# Job Ad Analyzer
A website where users can submit job ad descriptions to get help analyzing key subjects, and generate tailored CVs or cover letters based on the job ad analysis and user-submitted work experience and education.

## Project Overview
This project provides a website where users can upload job descriptions from job ads to get help from a Large Language Model (LLM) in analyzing the most important subjects mentioned. The importance of each subject is evaluated on a scale of 1 to 10. 

Users can then add their relevant experience for each subject, and generate tailored CVs or cover letters as PDF documents based on that information. 

The system is designed to be fast and resource efficient, as similar job ads are stored and can be reused by other users, avoiding the need to repeatedly generate the same analysis.

## Microservices Architecture
This project follows a microservices architecture where each service is responsible for a distinct part of the system. The services communicate with each other to perform various tasks related to the job analysis, storage, and CV/cover letter generation.

The system currently consists of the following services:
- **[Frontend Service](https://github.com/gyuudon3187/job-application-manager-frontend)**: Handles user interactions including registration, login, job description submission, relevant skill management and CV/cover letter generation.
- **[Authentication Service](https://github.com/DavidFB94/job-application-manager-backend)**: Manages user authentication, including login and registration.
- **[Job Service](https://github.com/gyuudon3187/job-service)**: Coordinates data flow between two databases for job ads and user skillsets (Qdrant for job info, Postgres for skillsets).
- **[Job Embedding Service](https://github.com/gyuudon3187/job-embedding-service)**: Generates embeddings for job descriptions and compares new submissions to existing jobs.
- **(Planned) CV Generation Service**: Will create personalized CVs and cover letters based on user-submitted information.

## Getting Started
WIP. See the microservices' respective repository for instructions on how to run them separately.

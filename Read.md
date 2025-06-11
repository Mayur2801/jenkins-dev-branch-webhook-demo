# Jenkins Dev Branch Webhook Demo

This repository demonstrates how to configure Jenkins to trigger builds via GitHub webhook, 
running the pipeline only when commits are pushed to the `development` branch.

## Setup Instructions

1. Fork or clone this repository.
2. In Jenkins, create a pipeline job pointing to this repo, set branch to `development`.
3. Configure a GitHub webhook to point to your Jenkins server:
   - Payload URL: `http://your-jenkins-host:8080/github-webhook/`
   - Content type: `application/json`
   - Trigger: Just the push event
4. Commit and push changes to the `development` branch to trigger builds.

---

## Project Structure

- `Jenkinsfile`: Pipeline definition for Jenkins
- `src/main.java`: Placeholder source code


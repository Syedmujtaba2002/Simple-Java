# 🚀 Task 8 – Run a Simple Java Maven Build Job in Jenkins

## 📌 Objective
The objective of this task was to learn how to integrate **Maven** with **Jenkins** by building a simple Java project.  
This was my first hands-on CI/CD pipeline step using Jenkins.

---

## 🛠 Steps I Performed

1. **Set up Jenkins**
   - Installed and ran Jenkins inside a Docker container.
   - Unlocked Jenkins using the initial admin password and installed suggested plugins.
   - Configured an admin user to access Jenkins dashboard.

2. **Configured Tools**
   - Added Maven in Jenkins (Manage Jenkins → Tools → Maven Installations).
   - Selected “Install automatically” so Jenkins downloads Maven inside the container.

3. **Prepared the Java Project**
   - Created a simple Java HelloWorld application with a `pom.xml`.
   - Pushed the project to GitHub for Jenkins to access.

4. **Created Jenkins Freestyle Job**
   - Configured Git as the Source Code Management and linked my GitHub repository.
   - Added a build step: *Invoke top-level Maven targets* with the goal `clean package`.
   - Configured post-build actions to archive the JAR artifact.

5. **Triggered the Build**
   - Ran the Jenkins job manually from the dashboard.
   - Jenkins pulled the project from GitHub, executed Maven, and packaged the application.
   - Verified the **Console Output** ended with `BUILD SUCCESS`.

6. **Verified Artifacts**
   - Jenkins generated the JAR file inside the `target` directory.
   - The artifact was archived and available for download from Jenkins.


## 🎯 Key Learnings
- How to configure and use Jenkins for continuous integration.
- Integration of Maven build tool with Jenkins jobs.
- Understanding Jenkins build logs and console output.
- How to manage build artifacts in Jenkins.

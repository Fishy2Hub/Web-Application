# Web-Application
Lab 1: Building & Breaking a Web App Stack

What I Did

For this lab, I moved away from just writing code in a single file and focused on how real-world applications are actually deployed. I built a multi-page web app using Flask and MySQL, but the real challenge was getting them to talk to each other inside Docker containers.

Key Things I Learned

1. Docker isn't just for show
Before this, I thought of a website as just "files on a computer." By using Docker Compose, I learned how to orchestrate a "stack." I realized that keeping the web server and the database in separate containers is better for security and scaling—something I know is huge in enterprise consulting.

2. Infrastructure as Code
I used a Dockerfile to set up my environment. This was a "lightbulb moment" for me because I realized that if I give this file to anyone else, the app will run exactly the same way on their machine as it did on mine. No more "it worked for me but not for you" bugs.

3. The "Trust Boundary" Realization
Using Burp Suite to intercept my own traffic was eye-opening. I saw how easy it is to change a POST request before it hits the server. It taught me that the frontend can’t be trusted. Now, I always assume that any data coming from a user’s browser could be malicious, so I focus on strong server-side validation.

My Tools

Backend: Flask (Python)
Data: MySQL
Containers: Docker & Docker Compose
Testing: Burp Suite & Nmap

Success Metrics:
- Got the Flask app and MySQL DB communicating perfectly on a private Docker network.
- Proved data persistence: even if the container restarts, the database keeps the info.
- Successfully intercepted and modified traffic to test how the app handles tampered data.


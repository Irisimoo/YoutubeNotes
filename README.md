# Inspiration
As students, we often use videos as study aids to help us learn content. We noticed several instances in our lives where we wanted to send science lectures and videos to friends with comments for studying purposes, but felt it was very inconvenient to send a video then message the timestamp with everything there is multiple times for multiple points in the video. So, we decided to design a user-friendly web application that allows students to take notes with corresponding time stamps and share the entire video with the timestamp.

# What it does
YoutubeNotes is a website for taking, summarizing and storing time-stamped video notes for Youtube videos. It allows users to create an account and login, then paste video links into a search bar. Then, the video is displayed with an area to take notes beside it. Notes can be taken at specific timestamps of the video that are flagged and marked on a progress bar. Users can then access previous notes at any time, and share the notes with others.

# How we built it
For the frontend, we designed the UI using Photoshop and built it with HTML, CSS, and JavaScript. Key elements include the YouTube iframe for video playback and a content-editable div for the note-taking area. The synced timeline below the video is created using two div elements with solid background colors, and JavaScript is used to render the note markers based on the timestamps. We also perform client-side YouTube URL validation by checking the video’s thumbnail size to confirm if the video exists and then store the video ID in localStorage to be used as the iframe source.

For the backend, we used Spring Boot to develop a REST API that communicates with the frontend via REST controllers. The application runs on an embedded Tomcat server, packaged with Spring Boot. We chose Spring Boot due to its easy configuration, versatility, and the team's familiarity with Java. Spring Security was implemented to safeguard the application. We used Thymeleaf for server-side rendering and integrated it with our Spring Boot Web Application. Notes and user data are stored in a MySQL database, which is managed by the backend. The backend accesses and updates the database through the Spring Boot service layer. JSON Web Tokens (JWT) are used to authenticate users and secure API endpoints.

# Demo
Here is a link to a demo of our project: https://youtu.be/LlYtPAtZeV4

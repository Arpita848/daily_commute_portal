# daily_commute_portal
Daily Commute Portal



🚗 Overview

The Daily Commute Portal is a web application designed to help users manage their daily commute efficiently. It allows users to:

Plan routes between two locations.

View mapped routes using OpenStreetMap.

Track their commute history (future enhancement).

Estimate fares and check live traffic conditions (optional features).

This project uses Node.js, Express.js, and Leaflet.js for map rendering, combined with OpenStreetMap for free, reliable mapping services without billing.

⚙️ Project Setup Instructions

1. Clone the Repository

Clone the project to your local system using:

git clone <repository-link>
cd daily-commute-portal

2. Install Dependencies

Run the following command to install the required dependencies:

npm install

3. Create .env File

Create a .env file in the root folder and add the following content:

PORT=3000

Since we're using OpenStreetMap, no API key is required.

4. Start the Server

Start the application with the command:

npm start

5. Access the Portal

Open your browser and visit:

http://localhost:3000

📋 API Endpoints and Functionalities

GET /

Serves the homepage displaying the web interface.

POST /api/route

Accepts origin and destination as JSON data in the request body.

Fetches route data from OpenStreetMap's Nominatim API.

Returns the starting and ending coordinates.

Sample Request Body:

{
    "origin": "Bhubaneswar",
    "destination": "Cuttack"
}

Sample Response:

{
    "start": { "lat": "20.2961", "lon": "85.8245" },
    "end": { "lat": "20.4634", "lon": "85.8821" }
}

🚧 Challenges Faced and Solutions Applied

🔹 Challenge 1: Google Maps API Billing Issue

Problem: Google Maps API required billing setup for routing.

Solution: Switched to OpenStreetMap + Leaflet.js, which provides a free alternative with no billing required.

🔹 Challenge 2: "Route Not Found" Error

Problem: The system failed to find certain routes, especially for less-known locations.

Solution: Improved error handling for invalid locations by validating responses from the Nominatim API.

🔹 Challenge 3: Deployment Issues

Problem: The application showed errors during deployment on cloud platforms.

Solution: Resolved issues by:

Ensuring dependencies were correctly installed.

Running npm cache clean --force before deployment.

🚀 Deployment Instructions

Recommended Platforms for Deployment

For easy and free deployment, consider these platforms:

Render (Best for Node.js apps)

Vercel (Ideal for frontend + serverless functions)

Railway (Perfect for full-stack apps)

Deployment Steps

Create an account on your chosen platform.

Connect your GitHub repository.

Add the .env file in the deployment environment.

Deploy the application.

Once deployed, your URL will look like this:

https://daily-commute-portal.onrender.com

📈 Future Enhancements

Implement route optimization for faster travel paths.

Add fare estimation based on distance and transport modes.

Introduce live traffic updates for real-time navigation.

Improve UI/UX with additional map controls and a user dashboard.

🤝 Contributing

Contributions are welcome! If you'd like to improve this project:

Fork the repository.

Create a new branch (git checkout -b feature-name).

Commit your changes (git commit -m "Add feature").

Push to your branch (git push origin feature-name).

Open a pull request.

📄 License

This project is licensed under the MIT License.

If you encounter issues or need further assistance, feel free to ask. 🚀


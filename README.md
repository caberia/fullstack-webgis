# WebGIS Final Assignment: Full Stack Geospatial API

## Project Description
This project is a Full Stack WebGIS application designed to manage geospatial data (points of interest) in Ankara. It allows users to store, visualize, filter, and analyze spatial data using a NoSQL database and a modern REST API.

## Implemented Modules
I have selected and implemented the following modules for the final assessment:

### 1. Compulsory (10%)
- Source code managed on GitHub Classroom with regular commits.
- Comprehensive `README.md` report.

### 2. NoSQL Database (25%)
- **Implementation:** MongoDB (Atlas Cloud).
- **Justification:** Used a document-oriented database to store GeoJSON objects efficiently, allowing for flexible schema design compared to relational tables.

### 3. API Development (25%)
- **Implementation:** Node.js & Express.
- **Endpoints:**
  - `GET /api/points` (Retrieve spatial data)
  - `POST /api/points` (Create spatial feature)
  - `PUT /api/points/:id` (Update attributes)
  - `DELETE /api/points/:id` (Remove feature)

### 4. CRUD Operations (15%) + Filtering
- **Create:** Users can add points via the sidebar form.
- **Read:** Points are displayed on a Leaflet map and a responsive data table.
- **Update/Delete:** Users can remove points directly from the UI.
- **Filtering:** Real-time search bar filters both the map markers and the table rows instantly.

### 5. Performance Monitoring (25%)
- **Mechanism:** Implemented a **2dsphere** geospatial index on the `location` field in MongoDB to optimize spatial queries.

### 6. Performance Testing (25%)
- **Tool:** Artillery.io
- **Experiment:** Load testing with 1500 requests simulating a ramp-up from 5 to 20 concurrent users.
- **Results:** The API sustained the load with 100% success rate and ~100ms average response time.
- **Graph:** (See Performance Graph below)

## Visuals
### Performance Test Result
![Performance Graph](performance-graph.png)

## Architecture
- **Frontend:** HTML, CSS, Leaflet.js
- **Backend:** Node.js, Express.js
- **Database:** MongoDB
- **Testing:** Artillery

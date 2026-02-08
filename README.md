📄 Enterprise AI Search
Enterprise AI Search is a full-stack document search application that allows users to upload documents (PDF, text, etc.), index them into Elasticsearch, and search their content using a web UI.
The project uses Spring Boot + Elasticsearch for the backend and React (Vite) for the frontend.

🚀 Features
📂 Upload files (PDF, TXT) via UI or Postman
🔍 Full-text search powered by Elasticsearch
📄 View indexed document content in the UI
⚡ Fast search results
🧠 Apache Tika for document text extraction
🌐 Modern React UI (Vite)

🛠️ Tech Stack
Backend
Java 17+
Spring Boot
Elasticsearch 8.x
Apache Tika
Docker (for Elasticsearch)

Frontend
React
Vite
HTML / CSS

⚙️ Prerequisites
Make sure you have the following installed:
Java 17 or later
Maven
Node.js (18+ recommended)
Docker

🐳 Start Elasticsearch (Required)
Run Elasticsearch using Docker:

docker run -d --name elasticsearch \
  -p 9200:9200 \
  -e discovery.type=single-node \
  -e xpack.security.enabled=false \
  docker.elastic.co/elasticsearch/elasticsearch:8.11.0


Verify:
http://localhost:9200

▶️ Run Backend (Spring Boot)
From the backend root directory:
mvn spring-boot:run

Backend runs on:
http://localhost:8080

▶️ Run Frontend (React)
From the frontend directory:
npm install
npx vite --host


Frontend runs on:
http://localhost:5173

📤 Upload Document
Using UI
Open http://localhost:5173
Choose a file
Click Upload

Using Postman
POST http://localhost:8080/api/upload
Body → form-data
Key: file
Type: File

🔍 Search Documents
Using UI
Type keyword in search bar
Click Search
Matching documents appear below
UI shows “Searching…” forever

✔ Backend or Elasticsearch is not running
📌 Future Improvements
Open PDF on click
Highlight matched text
Pagination
Authentication
File preview
Delete/update documents

👨‍💻 Author
Ashutosh Kumar Chaubey
Enterprise AI Search Project

⭐ If you like this project
Give it a ⭐ on GitHub!

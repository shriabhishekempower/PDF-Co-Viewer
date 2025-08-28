# PDF Co-Viewer
https://studio--jag-springboard-test.us-central1.hosted.app/
## Overview

The **PDF Co-Viewer** is a collaborative PDF viewing platform that allows multiple users to view and navigate a PDF document in real-time. Users can view the same page, sync their page navigation, and collaborate efficiently. The application is powered by **Socket.IO** for real-time communication, **Express** for the server-side setup, and **PDF.js** for rendering PDFs in the browser.

The application also supports **basic navigation** features like "Next" and "Previous" page navigation, and displays the **current page number** to all users.

## Features

- **Real-Time Collaboration**: Multiple users can view the same page of the PDF document at the same time.
- **Page Navigation**: Users can navigate through the PDF document by going to the next or previous page.
- **User Interface**: A simple and clean UI that displays the PDF and navigation buttons for user interaction.
- **Real-Time Sync**: When one user changes the page, the others see the same page instantly.
- **Dynamic PDF Rendering**: The PDF is rendered dynamically using **PDF.js** library.

## Tech Stack

- **Frontend**: HTML, CSS, JavaScript (with PDF.js)
- **Backend**: Node.js, Express.js
- **Real-Time Communication**: Socket.IO
- **Deployment**: Vercel (for frontend) and Node.js server

## Presenter's Screen
<img width="1532" alt="Screenshot 2024-11-13 at 11 00 02 AM" src="https://github.com/user-attachments/assets/41945e78-5b80-450c-9a7d-af98143f441a">

## Viewers Screen
<img width="1532" alt="Screenshot 2024-11-13 at 11 00 34 AM" src="https://github.com/user-attachments/assets/c8072e7a-18ad-41c0-ae8d-9e01b334f6f4">

### Prerequisites

- Node.js and npm installed on your machine.
- A GitHub account for version control (if deploying on GitHub).
- A Vercel account (for deploying the frontend).

- How It Works

Frontend (Client-Side)
The frontend is a web application that renders a PDF using the PDF.js library. It includes:
Page Navigation Buttons: "Previous" and "Next" buttons to allow users to navigate through the PDF pages.
Page Display: A span element that shows the current page number.
Real-Time Sync with Socket.IO: When a user navigates to a new page, an event is emitted to inform other users of the page change. The frontend also listens for page change events from other users and updates the view accordingly to ensure everyone is viewing the same page.

Backend (Server-Side)
The backend is built using Express.js and Socket.IO. It includes:
Express Server: Serves the HTML and JavaScript files for the frontend and manages incoming requests.
Socket.IO for Real-Time Events: Listens for events from clients when they change the page and broadcasts the new page number to all other connected clients to keep the views in sync.

### Steps to Run Locally

1. **Clone the repository**:

   ```bash
   git clone https://github.com/shriabhishekk/PDF-Co-Viewer.git
   cd PDF-Co-Viewer

  




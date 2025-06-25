# Data Compression & Decompression Portal Setup Guide

This document provides detailed instructions for setting up and running the Data Compression & Decompression Portal project.

## Prerequisites

Before you begin, ensure you have the following installed on your system:

- Node.js (v14.x or later)
- npm (v6.x or later)
- Git

## Getting Started

Follow these steps to set up and run the project:

### 1. Clone the Repository

```bash
git clone https://github.com/your-username/data-compression-portal.git
cd data-compression-portal
```

### 2. Install Dependencies

The project consists of three main parts: the root project, the backend server, and the frontend client. You need to install dependencies for all of them.

#### Option 1: Install All Dependencies at Once

From the root directory, run:

```bash
npm run install-all
```

#### Option 2: Install Dependencies Separately

From the root directory:

```bash
# Install root dependencies
npm install

# Install server dependencies
cd server
npm install
cd ..

# Install client dependencies
cd client
npm install
cd ..
```

### 3. Configure Environment Variables (Optional)

If needed, create `.env` files in the server and client directories.

#### Server (.env in server directory)

```
PORT=3001
```

#### Client (.env in client directory)

```
REACT_APP_API_URL=http://localhost:3001/api
```

### 4. Start the Application

#### Development Mode

Start both the server and client in development mode with one command from the root directory:

```bash
npm start
```

This will start:
- The backend server at http://localhost:3001
- The frontend client at http://localhost:3000

#### Start Server and Client Separately

If you prefer to start them separately:

```bash
# Start the server
cd server
npm start
```

In a new terminal:

```bash
# Start the client
cd client
npm start
```

### 5. Build for Production

To build the client for production:

```bash
cd client
npm run build
```

This will create a production-ready build in the `client/build` directory.

## Project Structure

The project follows a standard full-stack application structure:

```
data-compression-portal/
├── client/                 # Frontend React application
│   ├── public/             # Static files
│   └── src/                # React source files
├── server/                 # Backend Node.js/Express application
│   ├── algorithms/         # Compression algorithm implementations
│   ├── controllers/        # Route controllers
│   ├── middleware/         # Custom middleware
│   ├── routes/             # API routes
│   └── server.js           # Server entry point
└── package.json            # Root package.json for scripts
```

## Available Scripts

In the root directory, you can run:

- `npm start`: Start both server and client in development mode
- `npm run server`: Start only the server
- `npm run client`: Start only the client
- `npm run install-all`: Install dependencies for server, client, and root
- `npm run build`: Build the client for production

## Usage

1. Open your browser and navigate to http://localhost:3000
2. Select the mode (Compress or Decompress)
3. Upload a file
4. If compressing, select a compression algorithm
5. Process the file and view the results
6. Download the processed file

## Troubleshooting

### API Connection Issues

If the client cannot connect to the server:

1. Check that both the client and server are running
2. Ensure the `REACT_APP_API_URL` is set correctly
3. Check for any CORS issues in the server console

### File Upload Issues

If file uploads fail:

1. Check the file size (max 20MB)
2. Ensure the uploads directory exists and has proper permissions
3. Check server console for specific error messages

### Missing Dependencies

If you encounter missing dependency errors:

```bash
# Reinstall dependencies
npm run install-all
```

## License

MIT

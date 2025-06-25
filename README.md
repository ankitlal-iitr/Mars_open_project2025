# Data Compression & Decompression Portal

A web application that allows users to upload files and apply various data compression algorithms (Huffman coding, Run-Length Encoding, LZ77) to reduce file size, as well as decompress previously compressed files.

## Features

- **File Upload**: Users can upload any file (text, image, binary).
- **Multiple Compression Algorithms**: Support for popular algorithms like Huffman Coding, Run-Length Encoding (RLE), LZ77.
- **Compression & Decompression**: Users can compress or decompress files using the chosen algorithm.
- **Compression Statistics**: Display compression ratio, original size, compressed size, and processing time.
- **Download Processed Files**: Allow users to download the compressed or decompressed files.
- **Algorithm Explanation**: Brief descriptions of the chosen compression algorithms.
- **Error Handling**: Proper feedback for unsupported files or decompression errors.
- **Responsive UI**: Intuitive frontend with React for easy file management and status updates.

## Tech Stack

### Frontend
- **Framework**: React.js
- **Styling**: Tailwind CSS
- **File Handling**: JavaScript FileReader API
- **Visualization**: Chart.js (for compression statistics)

### Backend
- **Runtime**: Node.js
- **Framework**: Express.js
- **Compression Algorithms**: Custom JavaScript modules implementing Huffman, RLE, and LZ77
- **File Handling**: multer (for file uploads), fs module (for file processing)

## Setup Instructions

### Prerequisites
- Node.js (v14.x or later)
- npm (v6.x or later)

### Installation

1. Clone the repository
```bash
git clone https://github.com/your-username/data-compression-portal.git
cd data-compression-portal
```

2. Install backend dependencies
```bash
cd server
npm install
cd ..
```

3. Install frontend dependencies
```bash
cd client
npm install
cd ..
```

### Running the Application

1. Start the backend server
```bash
cd server
npm start
```

2. Start the frontend application (in a new terminal)
```bash
cd client
npm start
```

3. Access the application at http://localhost:3000

## Project Structure

```
data-compression-portal/
├── client/                 # Frontend React application
│   ├── public/             # Static files
│   ├── src/                # React source files
│   │   ├── components/     # Reusable components
│   │   ├── pages/          # Page components
│   │   ├── utils/          # Utility functions
│   │   └── ...
│   └── ...
├── server/                 # Backend Node.js/Express application
│   ├── algorithms/         # Compression algorithms implementations
│   ├── controllers/        # Route controllers
│   ├── middleware/         # Custom middleware
│   ├── routes/             # API routes
│   ├── utils/              # Utility functions
│   └── server.js           # Server entry point
└── ...
```

## License

MIT

## Author

Ankit Lal

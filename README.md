# Dockerized Todo Application - IBM Cloud Deployment

This is a containerized Todo application built with React and Context API, developed during IBM Project Based Experimental Learning. The application is containerized using Docker and deployed on IBM Cloud Container Registry.

## Features

- Add, edit, and delete tasks
- Persistent storage using localStorage
- Containerized using Docker
- Deployed on IBM Cloud
- Responsive design with modern UI

## Local Development

### Prerequisites
- Node.js (v20 or higher)
- npm or yarn
- Docker

### Installation

1. Clone the repository:
```bash
git clone https://github.com/shubham-kumr/todo-app.git
cd todo-app
```

2. Install dependencies:
```bash
npm install
```

3. Run locally:
```bash
npm run dev
```

## Docker Setup

### Build Docker Image
```bash
docker build -t shubham-todo-app .
```

### Run Docker Container
```bash
docker run -d -p 3000:80 shubham-todo-app
```

The application will be available at `http://localhost:3000`

## IBM Cloud Deployment

The application is deployed on IBM Cloud using the following steps:

1. Create IBM Cloud Container Registry namespace:
```bash
ibmcloud cr namespace-add shubham-namespace
```

2. Tag the Docker image:
```bash
docker tag shubham-todo-app icr.io/shubham-namespace/todo-app:v1
```

3. Push to IBM Cloud Container Registry:
```bash
docker push icr.io/shubham-namespace/todo-app:v1
```

## Technologies Used

- React.js
- Context API for state management
- Docker for containerization
- Nginx as web server
- IBM Cloud Container Registry
- Vite for build tool
- Tailwind CSS for styling

## Project Structure

```
todo-app/
├── src/
│   ├── components/
│   ├── contexts/
│   ├── App.jsx
│   └── main.jsx
├── Dockerfile
├── package.json
└── README.md
```


## License

This project is licensed under the [MIT License](https://opensource.org/licenses/MIT).

## Acknowledgments

- IBM Project Based Experimental Learning Program
- Docker Documentation
- IBM Cloud Documentation

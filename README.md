# Projeto DIO 01 - Docker compose
## Learning Project: Docker and Docker Compose with Apache HTTP Server

This project aims to provide a practical introduction to Docker and Docker Compose by setting up a simple web server using the Apache HTTP Server to serve an HTML page.

## Technologies Used

- **Docker**: A containerization platform that allows you to package and run applications in isolation.
- **Docker Compose**: A tool for defining and running multi-container applications.
- **Apache HTTP Server**: A robust and widely-used web server.

## Prerequisites

Before you begin, ensure you have the following installed on your machine:

- [Docker](https://www.docker.com/get-started) (version 20.10 or higher)
- [Docker Compose](https://docs.docker.com/compose/install/) (version 1.27 or higher)

## Project Structure

```bash
my-project/
├── docker-compose.yml
├── html
    └── index.html
```

- `docker-compose.yml`: Configuration file for Docker Compose.
- `Dockerfile`: File for building the Apache container image.
- `index.html`: Simple HTML page that will be served by Apache.

## How to Run the Project

1. **Clone the repository**:

  ```bash
   git clone https://github.com/yourusername/docker-apache-project.git
   cd docker-apache-project
  ```

2. **Build and start the containers**:

```bash
docker-compose up --build
```

3. **Access the application**:

Open your browser and go to `http://localhost:5000`. You should see the `HTML` page served by `Apache`.

## Customizing the Page

You can customize the HTML page by editing the `index.html` file. Feel free to add your own content!

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>My Simple Page</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            line-height: 1.6;
            margin: 0;
            padding: 0;
        }
        header {
            background: #4CAF50;
            color: white;
            padding: 10px 0;
            text-align: center;
        }
        nav ul {
            list-style-type: none;
            padding: 0;
        }
        nav ul li {
            display: inline;
            margin: 0 15px;
        }
        nav ul li a {
            color: white;
            text-decoration: none;
        }
        main {
            padding: 20px;
        }
        section {
            margin: 20px 0;
        }
        footer {
            background: #333;
            color: white;
            text-align: center;
            padding: 10px 0;
            position: relative;
            bottom: 0;
            width: 100%;
        }
    </style>
</head>
<body>
    <header>
        <h1>Welcome to My Simple Page</h1>
        <nav>
            <ul>
                <li><a href="#about">About</a></li>
                <li><a href="#services">Services</a></li>
                <li><a href="#contact">Contact</a></li>
            </ul>
        </nav>
    </header>

    <main>
        <section id="about">
            <h2>About</h2>
            <p>This is a simple static webpage created as an example using HTML.</p>
        </section>

        <section id="services">
            <h2>Services</h2>
            <p>We offer a variety of services to help you succeed online.</p>
        </section>

        <section id="contact">
            <h2>Contact</h2>
            <p>Feel free to reach out via email: <a href="mailto:example@example.com">example@example.com</a>.</p>
        </section>
    </main>

    <footer>
        <p>&copy; 2024 My Simple Page</p>
    </footer>
</body>
</html>

```

### Useful Commands

- To stop the containers:

```bash
docker-compose down
```

- To view the logs:

```bash
docker-compose logs
```

## Contributing

Feel free to contribute to this project! You can make suggestions or improvements by forking the repository and submitting a pull request.

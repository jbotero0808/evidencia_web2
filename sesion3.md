<!-- No borrar o modificar -->
[Inicio](./index.md)

## Sesión 3 

# Actividad: Sitio Web de películas utilizando React Bootstrap.

Los componentes esenciales para exhibir una lista de películas utilizando las tecnologías React y Bootstrap son los que se detallan a continuación. Realiza la ampliación y la expansión de esta implementación mediante la inclusión de películas adicionales, así como la integración de componentes específicos de React Bootstrap, como una barra de navegación (navbar), para lograr una experiencia más completa y enriquecedora.

## MovieCard.jsx

```javascript
    import React from 'react'
    import { Card } from "react-bootstrap";

    export default function MovieCard({ title, description, imageUrl }) {
        return (
            <Card>
                <Card.Img variant="top" src={imageUrl} />
                <Card.Body>
                    <Card.Title>{title}</Card.Title>
                    <Card.Text>{description}</Card.Text>
                </Card.Body>
            </Card>
        )
    }
``` 

## MovieList.jsx

```javascript
    import React from "react";
    import MovieCard from "./MovieCard";
    import { Container, Row, Col } from "react-bootstrap";

    const movies = [
    {
        title: "Pelicula 1",
        description: "Descripción de la película 1.",
        imageUrl: "https://via.placeholder.com/150",
    },
    {
        title: "Pelicula 2",
        description: "Descripción de la película 2.",
        imageUrl: "https://via.placeholder.com/150",
    },
    // ... Agrega más películas aquí
    ];

    const MovieList = () => {
    return (
        <Container>
        <Row>
            {movies.map((movie, index) => (
            <Col key={index} xs={12} md={4}>
                <MovieCard
                title={movie.title}
                description={movie.description}
                imageUrl={movie.imageUrl}
                />
            </Col>
            ))}
        </Row>
        </Container>
    );
    };
    export default MovieList;
``` 

## App.jsx

```javascript
    import './App.css'
    import MovieList from './Components/MovieList'

    function App() {
    return (
        <>
        <div>
            <header>
            <h1>Películas</h1>
            </header>
            <main>
            <MovieList />
            </main>
        </div>
        </>
    )
    }
    export default App
``` 

# Solución
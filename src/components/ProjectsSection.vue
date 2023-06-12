<template>
    <section class="projects-section">
      <h2 class="text-center">Mis Proyectos</h2>
      <div class="row justify-content-center">
        <div class="col-md-6 col-lg-4">
          <div class="project-card project-card-tall">
            <img :src="projects[0].image" alt="Project Image" class="img-fluid">
            <h3>{{ projects[0].title }}</h3>
            <p>{{ projects[0].description }}</p>
            <a :href="projects[0].link" class="btn btn-primary">Ver más</a>
          </div>
        </div>
        <div class="col-md-6 col-lg-4">
          <div class="project-card project-card-tall">
            <img :src="projects[1].image" alt="Project Image" class="img-fluid">
            <h3>{{ projects[1].title }}</h3>
            <p>{{ projects[1].description }}</p>
            <a :href="projects[1].link" class="btn btn-primary">Ver más</a>
          </div>
        </div>
        <div class="col-lg-4">
          <div class="project-card project-card-wide">
            <img :src="projects[2].image" alt="Project Image" class="img-fluid">
            <h3>{{ projects[2].title }}</h3>
            <p>{{ projects[2].description }}</p>
            <a :href="projects[2].link" class="btn btn-primary">Ver más</a>
          </div>
        </div>
      </div>
    </section>
  </template>
  
  <script>
  export default {
    name: 'ProjectsSection',
    data() {
      return {
        projects: [
          {
            title: 'Proyecto 1',
            description: 'Descripción del Proyecto 1',
            image: 'project1.jpg',
            link: 'https://www.example.com/proyecto1',
          },
          {
            title: 'Proyecto 2',
            description: 'Descripción del Proyecto 2',
            image: 'project2.jpg',
            link: 'https://www.example.com/proyecto2',
          },
          {
            title: 'Proyecto 3',
            description: 'Descripción del Proyecto 3',
            image: 'project3.jpg',
            link: 'https://www.example.com/proyecto3',
          },
        ],
      };
    },
  };
  </script>
  
  <style scoped>
  .projects-section {
    padding: 80px 0;
  }
  
  .row.justify-content-center {
    gap: 20px;
  }
  
  .project-card {
    margin-bottom: 30px;
    padding: 20px;
    border: 1px solid #ccc;
    border-radius: 5px;
    text-align: center;
    display: flex;
    flex-direction: column;
    align-items: center;
  }
  
  .project-card-tall {
    height: 400px;
  }
  
  .project-card-wide {
    height: 400px;
    width: 100%;
  }
  
  .project-card img {
    margin-bottom: 20px;
  }
  </style>
  
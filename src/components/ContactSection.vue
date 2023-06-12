<template>
    <section class="contact-section">
      <div class="container">
        <div class="row">
          <div class="col-md-6">
            <div class="contact-info">
              <h2>Contacto</h2>
              <ul class="list-inline">
                <li>
                  <i class="fa fa-envelope"></i>
                  geronimovenzi@live.com.ar
                </li>
                <li>
                  <i class="fa fa-phone"></i>
                  +54 2284-229818
                </li>
                <li class="social-icons">
                    <a href="#"><i class="fab fa-linkedin"></i></a>
                    <a href="#"><i class="fab fa-github"></i></a>
                    <a href="#"><i class="fab fa-instagram"></i></a>
                </li>
              </ul>
            </div>
          </div>
          <div class="col-md-6">
            <div class="contact-form">
              <h2>Formulario de Contacto</h2>
              <form @submit.prevent="sendEmail">
                <div class="form-group">
                  <label for="nombre">Nombre</label>
                  <input type="text" class="form-control" id="nombre" v-model="nombre" placeholder="Ingrese su nombre">
                </div>
                <div class="form-group">
                  <label for="email">Email</label>
                  <input type="email" class="form-control" id="email" v-model="email" placeholder="Ingrese su email">
                </div>
                <div class="form-group">
                  <label for="telefono">Teléfono</label>
                  <input type="text" class="form-control" id="telefono" v-model="telefono" placeholder="Ingrese su teléfono">
                </div>
                <div class="form-group">
                  <label for="mensaje">Mensaje</label>
                  <textarea class="form-control" id="mensaje" v-model="mensaje" rows="3" placeholder="Ingrese su mensaje"></textarea>
                </div>
                <button type="submit" class="btn btn-primary">Enviar</button>
              </form>
            </div>
          </div>
        </div>
      </div>
    </section>
  </template>
  
  <script>
  export default {
    name: 'ContactSection',
    data() {
      return {
        nombre: '',
        email: '',
        telefono: '',
        mensaje: ''
      };
    },
    methods: {
      sendEmail() {
        const subject = 'Formulario de contacto';
        const body = `Nombre: ${this.nombre}\nEmail: ${this.email}\nTeléfono: ${this.telefono}\nMensaje: ${this.mensaje}`;
        const mailtoLink = `mailto:gerovenzi@gmail.com?subject=${encodeURIComponent(subject)}&body=${encodeURIComponent(body)}`;
        window.location.href = mailtoLink;
      }
    }
  };
  </script>
  
  <style scoped>
  .contact-section {
    padding: 80px 0;
    background-color: #f9f9f9;
  }
  
  .contact-info,
  .contact-form {
    height: 100%;
    padding: 30px;
    background-color: #f3f3f3;
    border: 1px solid #ccc;
    border-radius: 5px;
    display: flex;
    flex-direction: column;
    justify-content: center;
  }
  
  .contact-info h2,
  .contact-form h2 {
    font-size: 24px;
    font-weight: bold;
    margin-bottom: 20px;
  }
  
  .contact-info ul li {
    margin-bottom: 10px;
  }
  
  .contact-info .social-icons {
    display: flex;
    justify-content: center;
  }
  
  .contact-info .social-icons a {
    margin-right: 10px;
  }
  
  .contact-form .form-group {
    margin-bottom: 20px;
  }
  
  .contact-form .form-group label {
    display: block;
    font-weight: 600;
    margin-bottom: 5px;
  }
  
  .contact-form .btn-primary {
    background-color: #007bff;
    border-color: #007bff;
    transition: background-color 0.3s ease;
  }
  
  .contact-form .btn-primary:hover {
    background-color: #0056b3;
  }
  </style>
  
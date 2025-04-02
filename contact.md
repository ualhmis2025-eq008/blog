---
layout: page
title: "Contacto"
permalink: /contacto/
---

<style>
  @keyframes fadeIn {
    from { opacity: 0; transform: translateY(20px); }
    to { opacity: 1; transform: translateY(0); }
  }
  
  .contact-container {
    max-width: 600px;
    margin: 2rem auto;
    padding: 2.5rem;
    border-radius: 16px;
    background: linear-gradient(145deg, #ffffff, #f5f7fa);
    box-shadow: 0 10px 30px rgba(0, 0, 0, 0.08);
    animation: fadeIn 0.6s ease-out forwards;
    border: 1px solid rgba(255, 255, 255, 0.3);
  }
  
  .contact-title {
    text-align: center;
    margin-bottom: 2rem;
    color: #2c3e50;
    font-size: 2.2rem;
    background: linear-gradient(90deg, #3498db, #9b59b6);
    -webkit-background-clip: text;
    background-clip: text;
    color: transparent;
    position: relative;
  }
  
  .contact-title:after {
    content: "";
    display: block;
    width: 80px;
    height: 4px;
    background: linear-gradient(90deg, #3498db, #9b59b6);
    margin: 10px auto 0;
    border-radius: 2px;
  }
  
  .form-group {
    margin-bottom: 1.5rem;
    position: relative;
  }
  
  .form-label {
    display: block;
    margin-bottom: 0.5rem;
    color: #34495e;
    font-weight: 500;
    font-size: 0.95rem;
  }
  
  .form-input {
    width: 100%;
    padding: 12px 15px;
    border: 2px solid #e0e6ed;
    border-radius: 8px;
    font-size: 1rem;
    transition: all 0.3s ease;
    background-color: #f8fafc;
  }
  
  .form-input:focus {
    border-color: #3498db;
    box-shadow: 0 0 0 3px rgba(52, 152, 219, 0.2);
    outline: none;
    background-color: #fff;
  }
  
  textarea.form-input {
    min-height: 150px;
    resize: vertical;
  }
  
  .submit-btn {
    width: 100%;
    padding: 14px;
    background: linear-gradient(135deg, #3498db, #9b59b6);
    color: white;
    border: none;
    border-radius: 8px;
    font-size: 1rem;
    font-weight: 600;
    cursor: pointer;
    transition: all 0.3s ease;
    box-shadow: 0 4px 6px rgba(52, 152, 219, 0.2);
  }
  
  .submit-btn:hover {
    transform: translateY(-2px);
    box-shadow: 0 6px 12px rgba(52, 152, 219, 0.3);
  }
  
  .submit-btn:active {
    transform: translateY(0);
  }
  
  .form-group:hover .form-label {
    color: #3498db;
  }
  
  @media (max-width: 768px) {
    .contact-container {
      padding: 1.5rem;
      margin: 1rem;
    }
  }
</style>

<div class="contact-container">
  <h2 class="contact-title">📬 Contáctanos</h2>
  
  <form action="https://formspree.io/f/meoaqpdz" method="POST">
    <div class="form-group">
      <label for="name" class="form-label">Nombre completo</label>
      <input type="text" id="name" name="name" class="form-input" required placeholder="Tu nombre">
    </div>
    
    <div class="form-group">
      <label for="email" class="form-label">Correo electrónico</label>
      <input type="email" id="email" name="email" class="form-input" required placeholder="tu@email.com">
    </div>
    
    <div class="form-group">
      <label for="asunto" class="form-label">Asunto</label>
      <input type="text" id="asunto" name="asunto" class="form-input" required placeholder="¿Sobre qué quieres hablar?">
    </div>
    
    <div class="form-group">
      <label for="message" class="form-label">Mensaje</label>
      <textarea id="message" name="message" class="form-input" required placeholder="Escribe tu mensaje aquí..."></textarea>
    </div>
    
    <button type="submit" class="submit-btn">
      <span>Enviar mensaje</span>
      <svg xmlns="http://www.w3.org/2000/svg" width="20" height="20" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" style="vertical-align: middle; margin-left: 8px;">
        <line x1="22" y1="2" x2="11" y2="13"></line>
        <polygon points="22 2 15 22 11 13 2 9 22 2"></polygon>
      </svg>
    </button>
  </form>
</div>

<script>
  // Efecto de aparición escalonada para los elementos del formulario
  document.addEventListener('DOMContentLoaded', function() {
    const formGroups = document.querySelectorAll('.form-group');
    
    formGroups.forEach((group, index) => {
      group.style.opacity = '0';
      group.style.transform = 'translateY(20px)';
      group.style.transition = `all 0.5s ease ${index * 0.1}s`;
      
      setTimeout(() => {
        group.style.opacity = '1';
        group.style.transform = 'translateY(0)';
      }, 100);
    });
  });
</script>
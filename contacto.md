---
layout: default
---
<div class="col-lg-8 mx-auto">
<h2>Contacto</h2>

<p class="lead">Si deseas ponerte en contacto con nosotros, por favor, rellena el siguiente formulario. Estaremos encantados de atenderte.</p>

<div id="thank-you-message" class="collapse" role="alert"></div>
<div id="error-message" class="alert alert-danger collapse" role="alert">Ha ocurrido un error al enviar el mensaje. Por favor, inténtalo de nuevo.</div>

<form id="contact-form" class="card p-4 p-md-5 shadow-sm border-0 rounded-4">
  <div class="mb-3">
    <label for="nombre" class="form-label">Nombre y apellidos</label>
    <input name="nombre" type="text" class="form-control" id="nombre" placeholder="Nombre y apellidos" required>
  </div>
  <div class="mb-3">
    <label for="email" class="form-label">Correo electrónico</label>
    <input name="email" id="email" type="email" class="form-control" placeholder="Tu correo electrónico" required>
  </div>
  <div class="mb-4">
    <label for="libre" class="form-label">Mensaje</label>
    <textarea name="message" class="form-control" id="libre" placeholder="¿Alguna duda en particular?" rows="5" required></textarea>
  </div>
  <div class="d-grid">
    <button id="submit-btn" type="submit" class="btn btn-primary btn-lg">Enviar</button>
  </div>
</form>

<script src="https://cdn.jsdelivr.net/npm/@emailjs/browser@4/dist/email.min.js"></script>
<script>
(function () {
  emailjs.init({ publicKey: '52HcKHByl7j4-hQbC' });

  document.getElementById('contact-form').addEventListener('submit', function (e) {
    e.preventDefault();

    var btn     = document.getElementById('submit-btn');
    var thankYou = document.getElementById('thank-you-message');
    var errorMsg = document.getElementById('error-message');

    btn.disabled    = true;
    btn.textContent = 'Enviando…';
    errorMsg.className = 'alert alert-danger collapse';

    emailjs.sendForm('service_ubbvmae', 'template_n7msv2q', this)
      .then(function () {
        thankYou.className   = 'alert alert-success';
        thankYou.innerHTML   = '<strong>¡Muchas gracias!</strong> Has enviado correctamente la información.';
        document.getElementById('contact-form').style.display = 'none';
      })
      .catch(function () {
        errorMsg.className = 'alert alert-danger';
        btn.disabled       = false;
        btn.textContent    = 'Enviar';
      });
  });
}());
</script>
</div>

---
layout: default
---
<div class="col-lg-8 mx-auto">
<h2>Contacto</h2>

<p class="lead">
Si deseas ponerte en contacto con nosotros, por favor, rellena el siguiente formulario. Estaremos encantados de atenderte.</p>

<div id="thank-you-message" class="collapse" role="alert">
  <strong>¡Muchas gracias!</strong> Has enviado correctamente la información.
</div>

<form action="https://getsimpleform.com/messages?form_api_token=783b6c9bb4e486be36be5ff73fc3803f" method="post" class="card p-4 shadow-sm border-0 rounded-4">
<input type="hidden" name="redirect_to" value='{{ site.url }}{{ page.url }}#thank-you'/>

<!-- Text input-->
<div class="form-group">
<label for="nombre">Nombre y apellidos</label>
<input name="nombre" type="text" class="form-control" id="nombre" placeholder="Nombre y apellidos" required data-validation-required-message="Por favor, escribe tu nombre.">
</div>
<div class="form-group">
<label for="email">Correo electrónico</label>
<input name="email" id="email" type="email" class="form-control" placeholder="Tu correo electrónico" required data-validation-required-message="Escriba una dirección de correo válida.">
</div>
<div class="form-group">
<label for="libre">Mensaje</label>
<textarea name="message" class="form-control" id="libre" placeholder="¿Alguna duda en particular?" rows="5" required></textarea>
</div>
<button id="button" class="btn btn-primary btn-lg btn-block mb-3">Enviar</button>
</form>
</div>

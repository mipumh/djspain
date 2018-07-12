---
layout: default
---
<h2>Añadir a la lista</h2>

<p class="lead">
Si quieres añadir a alguien a la lista, por favor, rellena el siguiente formulario. Las propuestas se analizarán y se subirán en bloque cada cierto tiempo.</p>

<div id="thank-you-message" class="collapse" role="alert">
  <strong>¡Muchas gracias!</strong> Has enviado correctamente la información.
</div>

<form action="https://getsimpleform.com/messages?form_api_token=783b6c9bb4e486be36be5ff73fc3803f" method="post">
<input type="hidden" name="redirect_to" value='http://mip.umh.es/djspain{{ page.url }}#thank-you'/>

<!-- Text input-->
<div class="form-group">
<input name="Formulario Periodistas de Datos" type="text" class="form-control" id="nombre" placeholder="Nombre y apellidos" required data-validation-required-message="Por favor, escribe tu nombre.">
</div>
<div class="form-group">
<input name="email" id="email" type="email" class="form-control" placeholder="email@correo.com" required data-validation-required-message="Escriba una dirección de correo válida.">
</div>
<div class="form-group">
<input name="alias" id="twitter" type="text" class="form-control" placeholder="Enlace a perfil en Twitter">
</div>
<!-- Text
<div class="form-group">
<select class="form-control" name="modalidad">
<option selected>Elige modalidad</option>
<option value="presencial" id="presencial">Presencial</option>
<option value="online" id="online">Online</option>
</select>
</div>
input-->                          
<div class="form-group">
<textarea name="message" class="libre" id="libre" type="text" class="form-control" placeholder="¿Por qué crees que debemos añadirle?" rows="3"></textarea>
</div>
<button id="button" class="btn btn-primary btn-lg btn-block mb-3">Enviar</button>
</form>
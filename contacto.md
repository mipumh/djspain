---
layout: default
---
<h2>Contacto</h2>

<p class="lead">
Estaremos encantados de atenderte si tienes alguna pregunta. Si deseas aparecer en la lista, por favor, rellena el formulario indicado. Aquí puedes ponerte en contacto con nosotros para todo lo demás.</p>

<div id="thank-you-message" class="collapse" role="alert">
  <strong>¡Muchas gracias!</strong> Has enviado correctamente la información.
</div>

<form action="https://getsimpleform.com/messages?form_api_token=783b6c9bb4e486be36be5ff73fc3803f" method="post">
<input type="hidden" name="redirect_to" value='{{ site.baseurl }}{{ page.url }}#thank-you'/>

<!-- Text input-->
<div class="form-group">
<input name="Formulario Periodistas de Datos" type="text" class="form-control" id="nombre" placeholder="Nombre y apellidos" required data-validation-required-message="Por favor, escribe tu nombre.">
</div>
<div class="form-group">
<input name="email" id="email" type="email" class="form-control" placeholder="email@correo.com" required data-validation-required-message="Escriba una dirección de correo válida.">
</div>
<div class="form-group">
<input name="telefono" id="movil" type="text" class="form-control" placeholder="Nº teléfono">
</div>
<div class="form-group">
<input name="ciudad" id="ciudad" type="text" class="form-control" placeholder="Ciudad (País)">
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
<textarea name="message" class="libre" id="libre" type="text" class="form-control" placeholder="¿Alguna duda en particular?" rows="3"></textarea>
</div>
<button id="button" class="btn btn-primary btn-lg btn-block mb-3">Enviar</button>
</form>
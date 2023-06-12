---
layout: default
---
<div class="my-3 p-3">

      <h4 class="border-bottom border-gray pb-2 mt-3">Profesionales en #redacción</h4>
      
      <div class="col-lg-12 mx-auto pb-3" id="search-demo-container">
            <div class="filter-parent" id="search">
            <label for="filter-by"></label>
            <input type="text" placeholder="Buscar periodistas" id="search-input" class="form-control input-lg" tabindex="1">
            </div>
        </div>
        <div class="col col-lg-12 col-sm-12">
            <p class="small text-light"><a href="{{ site.baseurl }}/redaccion.html">#redacción</a> | <a href="/academia.html"> #academia</a> | <a href="/proyectos.html">#proyectos</a> | <a href="/desarrollo.html">#desarrollo</a> | <a href="/visualizacion.html">#visualización</a> | <a href="/verificacion.html">#verificación</a> | <a href="/transparencia.html">#transparencia</a> | <a href="/investigacion.html">#investigación</a> | <a href="/analisis.html">#análisis</a></p>
        </div>

      <div class="list-group mb-3" id="results-container"></div>  

      <div class="list-group mb-3">
        {% for journos in site.data.journos %}
            {% if journos.tag_1 == "Redacción" or journos.tag_2 == "Redacción" %}

          <a class="list-group-item list-group-item-action d-flex align-items-center" href="#" data-toggle="modal" data-target="#{{ journos.nombre }}">
            <img id="{{ journos.modal }}" src="https://unavatar.io/twitter/{{ journos.alias }}" alt="{{ journos.nombre }}" width="32" height="32" class="rounded me-2" loading="lazy">
            <span>
              <strong>{{ journos.nombre }}</strong> @{{ journos.alias }}
            </span>
          </a>
            {% endif %}
          {% endfor %}
      </div>

    {% for journos in site.data.journos %}
            {% if journos.tag_1 == "Redacción" or journos.tag_2 == "Redacción" %}

      <!-- Modal -->
      <div class="modal fade" id="{{ journos.nombre }}" tabindex="-1" role="dialog" aria-labelledby="{{ journos.nombre }}Title" aria-hidden="true">
        <div class="modal-dialog modal-dialog-centered" role="document">
          <div class="modal-content">
            <div class="modal-header">
              <h5 class="modal-title" id="{{ journos.nombre }}Label">{{ journos.nombre }}</h5>
              <button type="button" class="close" data-dismiss="modal" aria-label="Close">
                <span aria-hidden="true">&times;</span>
              </button>
            </div>
            <div class="modal-body">
            <div class="media">
            <img class="align-self-start mr-3 rounded mb-4" src="https://unavatar.io/twitter/{{ journos.alias }}" alt="{{ journos.nombre }}" width="72" height="72">
            <div class="media-body">
            <a style="text-decoration:none" href="{{ journos.twitter }}" target="_blank"><h5 class="mt-0 mb-1 text-primary">@{{ journos.alias }}</h5></a>
            <p>{{ journos.perfil }}</p>
            <p class="text-success"><i class="fas fa-map-marker-alt"></i> {{ journos.ciudad }}{% if journos.pais %} ({{ journos.pais }}){% endif %}</p>
            {% if journos.web %}<p><i class="fas fa-link"></i> <a class="text-secondary" href="{{ journos.web }}" target="_blank">Sitio web</a></p>{% endif %}
            {% if journos.medio %}<p><i class="far fa-building"></i> {{ journos.medio }}</p>{% endif %}
            <p><i class="fas fa-tag"></i> {% if journos.tag_1 %} <a href="/{{ journos.tag_1 | downcase | replace: 'ó', 'o' | replace: 'á', 'a' }}.html" class="btn btn-outline-secondary btn-sm">{{ journos.tag_1 }}</a> {% endif %} {% if journos.tag_2 %} <a href="/{{ journos.tag_2 | downcase | replace: 'ó', 'o' | replace: 'á', 'a' }}.html" class="btn btn-outline-secondary btn-sm">{{ journos.tag_2 }}</a> {% endif %}</p>
            </div>
          </div>
          </div>
            <div class="modal-footer">
              <button type="button" class="btn btn-secondary" data-dismiss="modal">Cerrar</button>
            </div>
          </div>
        </div>
      </div>
        {% endif %}
    {% endfor %}

</div>

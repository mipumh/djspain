---
layout: default
---
<div class="my-3 p-3 bg-white rounded box-shadow">
        <div id="results-container"></div>  

        <h6 class="border-bottom border-gray pb-2 mb-0">Profesionales en #investigación</h6>

    {% for journos in site.data.journos %}
	
	  {% if journos.tag_1 and journos.tag_2 == "Investigación" %}

    <!-- Link trigger modal -->
        <div class="media text-muted pt-3 border-bottom border-gray">
        <a href="#" data-toggle="modal" data-target="#{{ journos.nombre }}">
          <img id="{{ journos.modal }}" src="{{ journos.pic }}" alt="{{ journos.nombre }}" class="mr-2 rounded" width="48" height="48">
            </a>  
          <div class="media-body pb-3 mb-0">
            <div class="d-flex justify-content-between align-items-center w-100">
              <a style="text-decoration:none" href="#" data-toggle="modal" data-target="#{{ journos.nombre }}"><strong class="text-gray-dark">{{ journos.nombre }}</strong></a>
            </div>
            <a class="text-secondary" href="{{ journos.twitter }}" target="_blank"><span class="d-block">@{{ journos.alias }}</span></a>
          </div>
        </div>

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
            <img class="align-self-start mr-3 rounded mb-4" src="{{ journos.pic }}" alt="{{ journos.nombre }}" width="72" height="72">
            <div class="media-body">
            <a style="text-decoration:none" href="https://twitter.com/{{ journos.alias }}" target="_blank"><h5 class="mt-0 mb-1 text-primary">@{{ journos.alias }}</h5></a>
            <p>{{ journos.perfil }}</p>
            <p class="text-success"><i class="fas fa-map-marker-alt"></i> {{ journos.ciudad }}{% if journos.pais %} ({{ journos.pais }}){% endif %}</p>
            {% if journos.web %}<p><i class="fas fa-link"></i> <a class="text-secondary" href="{{ journos.web }}" target="_blank">Sitio web</a></p>{% endif %}
            {% if journos.medio %}<p><i class="far fa-building"></i> {{ journos.medio }}</p>{% endif %}
            <p><i class="fas fa-tag"></i> {% if journos.tag_1 %} <button type="button" class="btn btn-outline-secondary btn-sm" disabled>{{ journos.tag_1 }}</button> {% endif %} {% if journos.tag_2 %} <button type="button" class="btn btn-outline-secondary btn-sm" disabled>{{ journos.tag_2 }}</button> {% endif %}</p>
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

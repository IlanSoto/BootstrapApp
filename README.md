# BootstrapApp

Este proyecto Angular utiliza Bootstrap para proporcionar una interfaz de usuario responsiva y Angular Animations para mejorar la interacción del usuario.

## Instalación de Bootstrap

1. **Instalar Bootstrap**: Usa npm para instalar Bootstrap en tu proyecto:

    ```bash
    npm install bootstrap
    ```

2. **Configurar Bootstrap en Angular**: Agrega Bootstrap a la configuración de estilos en el archivo `angular.json`:

    ```json
    "styles": [
      "src/styles.css",
      "node_modules/bootstrap/dist/css/bootstrap.min.css"
    ]
    ```

## Uso de Componentes de Bootstrap

Para utilizar los componentes de Bootstrap, agrega el HTML correspondiente a tu archivo de plantilla. Aquí hay un ejemplo de una tarjeta de Bootstrap con tamaño reducido y un botón para mostrar/ocultar la tarjeta:

### `src/app/app.component.html`

```html
<div class="container mt-5">
  <div class="text-center mb-4">
    <!-- Botón de Mostrar/Ocultar -->
    <button (click)="show = !show" class="btn btn-secondary">
      {{ show ? 'Ocultar Tarjeta' : 'Mostrar Tarjeta' }}
    </button>
  </div>

  <!-- Tarjeta con animación -->
  <div *ngIf="show" @fadeInOut class="card-container">
    <div class="row justify-content-center">
      <div class="col-md-6 col-lg-4">
        <div class="card">
          <img src="https://via.placeholder.com/150" class="card-img-top" alt="...">
          <div class="card-body">
            <h5 class="card-title">Título de la Tarjeta</h5>
            <p class="card-text">Algunos textos rápidos para construir el contenido de la tarjeta y hacer que el contenido se vea un poco más extenso.</p>
            <a href="#" class="btn btn-primary">Ir a algún lugar</a>
          </div>
        </div>
      </div>
    </div>
  </div>
</div>


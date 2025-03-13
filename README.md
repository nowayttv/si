<!DOCTYPE html>
<html>
  <head>
    <!-- Compatibilité mobile -->
    <meta name="viewport" content="width=device-width,initial-scale=1">
    <!-- Chargement des libraire externe -->
    <script src="https://cdnjs.cloudflare.com/ajax/libs/jquery/3.7.1/jquery.min.js"></script>
    <script src="https://aframe.io/releases/1.5.0/aframe.min.js"></script>
    <script src="./js/modules/template.js"></script>
  </head>

  <body>
    <!-- composant utiliser pour crée une scene sur A-FRAME  -->
    <!-- Le composant raycaster et cursor sert pour la gestion click -->
    <a-scene cursor="rayOrigin: mouse; fuse: false" raycaster="objects: .raycastable">
        <!-- Script vide, utiliser pour le chargement de scene -->
        <script id="NA" type="text/html"></script>
        <!-- composant utiliser pour gerer la camera -->
        <a-entity id="cur_camera" camera="active: true" position="0 0 0" look-controls animation__1= "property: camera.far; to: 100 ; dur: 500; easing: linear; startEvents: start_trans" animation__2= "property: camera.far; from: 100; to: 1000; dur: 500; easing: linear; startEvents: end_trans">  </a-entity>
        <!-- Initialisation de la "scène" utiliser, composant customizer -->
        <a-entity id="MainScene" scene-init template="src: #NA" />
      </a-scene>
  </body>

  <!-- Chargement de l'index en JavaScript -->
  <script src="./index.js"></script>
</html>

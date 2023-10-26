# Enunciado Proyecto 2.2

El Proyecto 2.2 se centra en la implementación de tres aspectos fundamentales en la aplicación móvil PichangApp: Georeferenciación, Imágenes y Social Media. Estos componentes son esenciales para enriquecer la experiencia de los usuarios al crear y administrar partidos de fútbol informales. Se espera que este proyecto sea una extensión natural del trabajo previo, permitiendo la incorporación de estas nuevas funcionalidades en el repositorio existente de la aplicación, que ha sido desarrollada con React Native y Expo. El objetivo principal es lograr una integración eficiente y efectiva de estas características en la aplicación móvil existente.

## Georeferenciación:
Para la georeferenciación, se recomienda explorar las siguientes referencias:
- Documentación de Expo sobre Georeferenciación: [Expo Geolocation](https://docs.expo.dev/versions/latest/sdk/location/)
- React Native Maps en GitHub: [react-native-maps](https://github.com/react-native-maps/react-native-maps). Se recomienda utilizar la versión "^1.7.1" o superior de react-native-maps.

## Expo Camera:
En esta entrega, es fundamental el manejo de imágenes. Es necesario la capacidad de tomar o subir fotos relacionadas al lugar del partido de fútbol (pichanga). Por esta razón, se recomienda encarecidamente el uso de [expo-camera](https://docs.expo.dev/versions/latest/sdk/camera/), una librería que permite a los usuarios tomar fotos con sus dispositivos móviles, almacenarlas y, si es necesario, enviarlas.

## Google Login:
Una parte crucial de este proyecto es la capacidad de gestionar usuarios a través de Google. En esta ocasión, se permitirá a los usuarios iniciar sesión y acceder a todos los datos de sus cuentas sin problemas. Para una mejor comprensión, se recomienda seguir una guía de cómo implementar este tipo de inicio de sesión ([GUÍA](https://docs.google.com/document/d/1-kn-e2g1AiKyYPMcCifUSO_YpCu8dQ4D6lE-WEgTDi8/edit?usp=sharing)).

## API Key:
Para esta entrega y para evitar futuras inconsistencias, es obligatorio incluir un archivo env en el proyecto que acepte la API key necesaria para el mapa que se utilizará. Por lo tanto, es importante indicar la ubicación específica donde debe ubicarse el archivo env y cualquier derivación en su nombre. Además, es crucial explicar el nombre de las variables que contendrá (por ejemplo, dentro del archivo utilizado, se debe incluir una variable llamada GOOGLE_APIKEY que contendrá la clave correspondiente).

1. [1.0] Integración de Geolocalización
   - Evaluar la capacidad de la aplicación para obtener la ubicación actual del usuario utilizando la API de georeferenciación de Expo.

2. [1.0] Visualización de Mapas
   - Evaluar la implementación de mapas interactivos que muestren las ubicaciones de los partidos de fútbol y permitan a los usuarios buscar partidos cercanos.

3. [1.0] Adjuntar Imágenes a Ubicaciones
   - Evaluar la capacidad de los usuarios para adjuntar imágenes a las ubicaciones de los partidos de fútbol al crear una pichanga. Las imágenes deben ser relevantes y mejorar la descripción visual de las ubicaciones. Se recomienda la capacidad de utilizar expo-camera para tomar fotos del lugar y utilizar una función de carga de archivos.

4. [2.0] Integración de Inicio de Sesión con Google
   - Evaluar la capacidad de los usuarios para iniciar sesión utilizando sus cuentas de Google. La integración debe ser fluida y segura.

5. [1.0] Integración General
   - Evaluar la integración de los tres componentes (Georeferenciación, Imágenes y Social Media) en la aplicación. La aplicación debe funcionar sin problemas y proporcionar una experiencia positiva al usuario.

## Endpoints API

Estos son los endpoints actuales de la API que deben ser gestionados:

1. **Login**
   - **Endpoint:** `POST https://pichang-app-e6269910e1a5.herokuapp.com/api/v1/login`
   - **Parámetros:**
     - `email`: String (Correo electrónico del usuario)
     - `password`: String (Contraseña del usuario)

2. **Registro de Usuario**
   - **Endpoint:** `POST https://pichang-app-e6269910e1a5.herokuapp.com/api/v1/signup`
   - **Parámetros:**
     - `email`: String (Correo electrónico del usuario)
     - `password`: String (Contraseña del usuario)
     - `name`: String (Nombre del usuario)
     - `category`: String (Categoría del usuario)

3. **Pichangas**
   - **Endpoint:** 
     - `POST https://pichang-app-e6269910e1a5.herokuapp.com/api/v1/pichangas`
     - `GET https://pichang-app-e6269910e1a5.herokuapp.com/api/v1/pichangas/:id` (Para obtener detalles de una pichanga específica)
     - `PUT https://pichang-app-e6269910e1a5.herokuapp.com/api/v1/pichangas/:id` (Para actualizar detalles de una pichanga específica)
     - `DELETE https://pichang-app-e6269910e1a5.herokuapp.com/api/v1/pichangas/:id` (Para eliminar una pichanga específica)
   - **Parámetros (POST):**
     - `home_team_id`: int (ID del equipo local)
     - `visitor_team_id`: int (ID del equipo visitante)
     - `location_id`: int (ID de la ubicación del partido)
     - `instructions`: Texto (Instrucciones para el partido)
     - `game_date`: datetime (Fecha y hora del partido)
     - `results`: String (Resultado del partido)

4. **Ubicaciones**
   - **Endpoint:** 
     - `POST https://pichang-app-e6269910e1a5.herokuapp.com/api/v1/locations`
     - `GET https://pichang-app-e6269910e1a5.herokuapp.com/api/v1/locations/:id` (Para obtener detalles de una ubicación específica)
     - `PUT https://pichang-app-e6269910e1a5.herokuapp.com/api/v1/locations/:id` (Para actualizar detalles de una ubicación específica)
     - `DELETE https://pichang-app-e6269910e1a5.herokuapp.com/api/v1/locations/:id` (Para eliminar una ubicación específica)

5. **Usuarios**
    - **Endpoint:** 
        - `GET https://pichang-app-e6269910e1a5.herokuapp.com/api/v1/users` (Para obtener detalles de usuarios)
        - `POST https://pichang-app-e6269910e1a5.herokuapp.com/api/v1/google` (Para login con google)
        - - **Parámetros:**
          - `google_token`: String

## Modo de trabajo y próximas evaluaciones

La tarea deberá ser entregada por cada grupo a su repositorio Git hasta el viernes 6 de noviembre de 2023 a las 23:59 hrs.
La entrega 2.3 consistirá en completar la funcionalidad que haya quedado faltante en el presente enunciado, y la fecha de entrega será 15 de noviembre de 2023.

Las demostraciones finales del proyecto 2 serán agendadas durante la semana del 20/11.

## Indicaciones a los ayudantes

Añadir a esta sección indicaciones que puedan facilitar a los ayudantes la evaluación de la tarea.

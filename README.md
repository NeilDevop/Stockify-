---

# Stockify - Inventory Management Software

**Stockify** es un sistema integral de gestión de inventario diseñado para optimizar el control de existencias, mejorar la precisión y facilitar la toma de decisiones. Con una interfaz intuitiva y herramientas avanzadas, **Stockify** permite a las empresas gestionar su inventario en tiempo real, asignar recursos de manera eficiente y generar informes detallados.

## Tabla de Contenidos
- [Características](#características)
- [Instalación](#instalación)
- [Configuración](#configuración)
- [Uso](#uso)
- [Tecnologías](#tecnologías)
- [Contribuciones](#contribuciones)
- [Licencia](#licencia)
- [Contacto](#contacto)

## Características

- **Seguimiento de inventario en tiempo real**: Monitorea los niveles de stock en tiempo real, garantizando información actualizada sobre la disponibilidad de productos.
- **Bloqueo de recursos**: Impide que múltiples usuarios accedan a la misma herramienta o recurso simultáneamente, asegurando que solo un usuario pueda utilizarlo a la vez.
- **Análisis e informes avanzados**: Genera informes detallados para optimizar los niveles de inventario y mejorar la toma de decisiones.
- **Roles de usuario**: Perfiles de administrador con acceso completo y usuarios generales con permisos limitados.
- **Escalabilidad**: Adecuado para empresas de cualquier tamaño.
- **Interfaz de usuario intuitiva**: Diseño simple y fácil de usar.

## Instalación

Para instalar **Stockify** localmente, sigue estos pasos:

1. **Clona el repositorio**:
   ```bash
   git clone https://github.com/yourusername/stockify.git
   cd stockify
   ```

2. **Frontend (Next.js)**:
   - Dirígete a la carpeta `frontend`:
     ```bash
     cd frontend
     ```
   - Instala las dependencias:
     ```bash
     npm install
     ```
   - Ejecuta la aplicación de frontend:
     ```bash
     npm run dev
     ```
   La aplicación estará disponible en `http://localhost:3000`.

3. **Backend (Django)**:
   - Dirígete a la carpeta `backend`:
     ```bash
     cd backend
     ```
   - Instala un entorno virtual y activa el entorno (opcional pero recomendado):
     ```bash
     python -m venv env
     source env/bin/activate  # Para Linux/Mac
     .\env\Scripts\activate  # Para Windows
     ```
   - Instala las dependencias:
     ```bash
     pip install -r requirements.txt
     ```
   - Realiza las migraciones:
     ```bash
     python manage.py migrate
     ```
   - Ejecuta el servidor de desarrollo de Django:
     ```bash
     python manage.py runserver
     ```
   La API estará disponible en `http://localhost:8000`.

4. **Configuración de Firebase**:
   - Para habilitar el uso de Firebase (almacenamiento o autenticación), asegúrate de configurar el proyecto en Firebase Console y descargar el archivo `firebase-config.json`.
   - Integra el archivo en el directorio adecuado y asegúrate de que las variables de entorno correctas estén configuradas en tu proyecto.

## Configuración

Asegúrate de configurar las variables de entorno necesarias tanto para el frontend como para el backend. Aquí tienes un ejemplo de configuración en el archivo `.env`:

### Para el Backend (Django):

```env
DB_HOST=localhost
DB_USER=root
DB_PASSWORD=yourpassword
DB_NAME=stockify_db
SECRET_KEY=your_secret_key
DEBUG=True
```

### Para el Frontend (Next.js):

```env
NEXT_PUBLIC_FIREBASE_API_KEY=your_firebase_api_key
NEXT_PUBLIC_FIREBASE_AUTH_DOMAIN=your_firebase_auth_domain
NEXT_PUBLIC_FIREBASE_PROJECT_ID=your_firebase_project_id
```

Asegúrate de incluir tus credenciales de Firebase y cualquier otra clave API necesaria.

## Uso

Una vez que ambas partes de la aplicación estén en funcionamiento:

1. **Login/Registro**: Los usuarios podrán registrarse y autenticarse utilizando el sistema de roles basado en Firebase.
2. **Gestión de inventario**: Los administradores pueden agregar, eliminar y actualizar los ítems en el inventario.
3. **Asignación de herramientas**: Los usuarios pueden tomar herramientas, y el sistema las marcará como en uso, impidiendo que otros usuarios accedan a ellas hasta que se liberen.
4. **Generación de informes**: El administrador puede generar informes personalizados sobre el uso y los niveles de inventario.

## Tecnologías

- **Frontend**: Next.js (React)
- **Backend**: Django (Python)
- **Base de datos**: PostgreSQL / MySQL / SQLite 
- **Autenticación y Almacenamiento**: Firebase
  
## Contribuciones

Si deseas contribuir al proyecto, sigue estos pasos:

1. Haz un fork del repositorio.
2. Crea una nueva rama (`git checkout -b feature-branch`).
3. Realiza tus cambios y haz commit (`git commit -m 'Añadir nueva funcionalidad'`).
4. Sube los cambios a tu rama (`git push origin feature-branch`).
5. Abre un pull request.

Asegúrate de seguir nuestras [guías de contribución](CONTRIBUTING.md) y [código de conducta](CODE_OF_CONDUCT.md).

## Licencia

Este proyecto está bajo la licencia MIT. Consulta el archivo [LICENSE](LICENSE) para más detalles.

## Contacto

Si tienes preguntas o necesitas asistencia, no dudes en contactarnos:

# Keep Streamlit App Alive

Este repositorio contiene un GitHub Action diseñado para mantener activa una aplicación alojada en Streamlit Sharing. El GitHub Action hace una solicitud HTTP a la aplicación cada semana para prevenir que la aplicación entre en hibernación y reduzca tiempos de espera en el primer acceso después de periodos de inactividad.

## Funcionamiento

El GitHub Action está programado para ejecutarse automáticamente cada domingo a las 3:00 AM UTC. Utiliza `curl` para hacer una solicitud GET a la URL de la aplicación de Streamlit. Si necesitas ajustar el horario de ejecución o la URL, puedes modificar el archivo `main.yml` en el directorio `.github/workflows`.

## Configuración

Para utilizar este script en tu propia aplicación de Streamlit, sigue estos pasos:

1. **Fork o clona este repositorio**: Puedes hacer un 'fork' de este repositorio o clonarlo directamente a tu cuenta de GitHub.
2. **Modifica el archivo `main.yml`**: Actualiza la URL en el archivo `main.yml` para apuntar a tu aplicación de Streamlit.
3. **Configura los GitHub Actions en tu repositorio**: Asegúrate de que GitHub Actions esté habilitado en tu repositorio.
4. **Verifica las ejecuciones**: Ve a la pestaña 'Actions' de tu repositorio para verificar que el workflow se ejecute según lo programado. 


Please add it in capacitor.config.json or run
npx cap init

You must install it in your project first, e.g. w/ 
npm install @capacitor/ios

npx cap add ios

Si encuentras el error "The workspace named 'App' does not contain a scheme named 'App'", sigue estos pasos:

1. Abre Xcode y carga el proyecto desde la carpeta `ios/App`.
2. Ve a `Product` > `Scheme` > `Manage Schemes...`.
3. Asegúrate de que el esquema `App` esté presente y marcado.
4. Si no está presente, crea un nuevo esquema y asegúrate de que esté seleccionado.


## Sincronizar proyectos LicWeb con LicApp (iOS y Android)

Para sincronizar los proyectos de LicWeb con LicApp, sigue estos pasos:

1. **Abrir el proyecto de LicPortalWebUsuario**:
   - Navega a la carpeta del proyecto LicPortalWebUsuario y ábrelo.

2. **Crear el build de producción del proyecto LicPortalWebUsuario**:
   - Ejecuta el siguiente comando en la terminal:
     ```sh
     npm run build:prod
     ```

3. **Copiar el contenido del build**:
   - Una vez completado el build, copia todo el contenido de la carpeta `dist/sige`.

4. **Abrir el proyecto LicAppIOSMovil**:
   - Navega a la carpeta del proyecto LicAppIOSMovil y ábrelo.

5. **Borrar el contenido de la carpeta [www]**:
   - Elimina todo el contenido que está dentro de la carpeta [www].

6. **Pegar el contenido copiado en la carpeta [www]**:
   - Pega todo el contenido copiado de `dist/sige` dentro de la carpeta [www].

7. **Sincronizar el proyecto con Capacitor**:
   - Ejecuta el siguiente comando en la terminal dentro del proyecto LicAppIOSMovil:
     ```sh
     npx capacitor sync
     ```
   - Este comando sincronizará todo el contenido copiado en la carpeta [www] y lo transformará en código para los proyectos de iOS en Xcode y Android Studio.

8. **Abrir el proyecto en Xcode o Android Studio**:
   - Abre el proyecto en Xcode para iOS con el comando 
   ```sh
     npx capacitor open ios
     ```
    o en Android Studio para Android con el comando
    ```sh
     npx capacitor open android
     ```
    y verifica que todo esté funcionando correctamente.

9. **Crear Apps release**:
  1. 
  Siguiendo estos pasos, podrás sincronizar los proyectos de LicWeb con LicApp para iOS y Android de manera efectiva.

  ## Pasos para crear una App release para Android

  1. **Sincroniza los cambios en el proyecto de Android**:
    ```sh
    npx cap sync android
    ```

  2. **Abre el proyecto en Android Studio**:
    ```sh
    npx cap open android
    ```

  3. **Configura el SDK y dependencias**:
    - Asegúrate de que el SDK de Android esté correctamente configurado y que todas las dependencias estén actualizadas en Android Studio.

  4. **Actualiza la versión de la app**:
    - Modifica los valores de `versionCode` y `versionName` en el archivo `build.gradle` del módulo de la aplicación (normalmente ubicado en `android/app/build.gradle`).

  5. **Genera el APK o App Bundle firmado**:
    - En Android Studio, ve a **Build > Generate Signed Bundle / APK** y sigue los pasos del asistente para crear tu release.


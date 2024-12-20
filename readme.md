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
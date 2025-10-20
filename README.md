# MiApp (Ionic + Angular) - APK con Icono y Splash personalizados
https://capacitorjs.com/docs/getting-started#where-to-go-next
<img width="674" height="706" alt="image" src="https://github.com/user-attachments/assets/eb020a86-de44-47b2-9444-be2e133c8869" />

## Resumen
Proyecto móvil creado con Ionic + Angular y Capacitor. Este repo incluye los pasos para generar iconos y splash personalizados, sincronizar con Capacitor y construir la app Android.

## Requisitos
- Node.js, npm
- Ionic CLI (`npm i -g @ionic/cli`)
- cordova-res (`npm i -g cordova-res`) 
- Android Studio y Android SDK (incluye ADB)
- Java JDK (para gradle/keytool)
  
##Instalación de Capacitor

1. Crear nueva aplicación Capacitor
npm init @capacitor/app@latest

2. Añadir Capacitor a tu app web existente
Instala dependencias:
npm i @capacitor/core
npm i -D @capacitor/cli
<img width="526" height="502" alt="image" src="https://github.com/user-attachments/assets/ed406807-4c76-429b-955c-b4b080576f46" />

Inicializa configuración de Capacitor:
npx cap init
Te pedirá nombre de la app y ID del paquete.
<img width="693" height="329" alt="image" src="https://github.com/user-attachments/assets/4cafa8f7-1d62-42c8-b51f-47a246724172" />

3. Añadir plataformas nativas
npm i @capacitor/android @capacitor/ios
npx cap add android
npx cap add ios
<img width="700" height="361" alt="image" src="https://github.com/user-attachments/assets/faa72322-814b-4f8e-81f7-22b5bb45782f" />

#4. Sincronizar tu app web con nativo
npx cap sync
<img width="664" height="289" alt="image" src="https://github.com/user-attachments/assets/11108ee6-daac-40ee-a330-991e8fca54f0" />

##Configuración de Icono y Splash

Para listar iconos y splash generados:
<img width="691" height="574" alt="image" src="https://github.com/user-attachments/assets/5ca89569-5054-44b6-9c4d-4d008a627645" />

Listar iconos generados en PowerShell:
dir .\android\app\src\main\res\mipmap-* | select Name
<img width="665" height="216" alt="image" src="https://github.com/user-attachments/assets/3d5f4291-6d35-4822-a039-fe90545a8376" />

Ver/Editar AndroidManifest.xml:
Get-Content .\android\app\src\main\AndroidManifest.xml
<img width="707" height="486" alt="image" src="https://github.com/user-attachments/assets/ff94d37d-31e5-415c-abba-868244be5140" />

##Ejecutar la app
ionic build
npx cap copy android
npx cap sync android
npx cap open android 
<img width="700" height="404" alt="image" src="https://github.com/user-attachments/assets/aa61fd6f-4b20-40c4-87aa-3d0fd5cc62e1" />

# CapacitorElectronApp
This is how you create Ionic+Capacitor+Angular+Electron App

## 1. Create a blank project Project
```
ionic start YourProjectName blank --type=angular
```
## 2. Go inside the folder and add capacitor dependencies
```
npm install --save @capacitor/core @capacitor/cli
```
## 3. Initiate Capacitor
```
npx cap init
```
## 4. Build ionic once so we can have capacitor www folder
```
ionic build
```
## 5. Add Electron
```
npx cap add electron
```
## 6. Change base href in `src/index.html`
So instead of `<base href="/" />` it should be <base href="./" />

## 7. Build ionic again
```
build ionic
```
Repeat from this step to step 9 if you do any change in your codes

## 8. Copy Ionic/Angular/Capacitor files to Electron
```
npx cap copy
```
## 9. Run Electron
```
npx cap open electron
```

## Bonus: You can also add following command in package.json file to combine above three commands to one
```
"electron": "ionic build && npx cap copy && npx cap open electron"
```
So you can run following one command only
```
npm run electron
```   

# CapacitorElectronApp

## 1. Create Project
```
ionic start ProjectName blank --type=angular
```
## 2. Go inside the folder and add capacitor dependencies
```
npm install --save @capacitor/core @capacitor/cli
```
## 3. Initiate Capacitor
```
npx cap init
```
## 4. Build ionic so we can have capacitor www folder
```
ionic build
```
## 5. Add Electron
```
npx cap add electron
```
## 6. Change base href in `src/index.html`

## 7. Build ionic
Repeat from this step if you do any change using command `ionic build`
## 8. Copy Ionic/Angular/Capacitor files to Electron
```
npx cap copy
```
## 9. Run Electron
```
npx cap open electron
```

## You can add following command in package.json file to combine above three commands to one
```
"electron": "ionic build && npx cap copy && npx cap open electron"
```

So you can run following one command only
```
npm run electron
```   
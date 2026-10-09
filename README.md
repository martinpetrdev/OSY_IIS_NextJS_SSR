# NextJS SSR na IIS webserveru

- Nainstalovat nodejs (.msi)
- Nainstalovat [IISNode](https://github.com/Azure/iisnode/releases/download/v0.2.26/iisnode-full-v0.2.26-x64.msi) a [URLRewrite](https://download.microsoft.com/download/1/2/8/128E2E22-C1B9-44A4-BE2A-5859ED1D4592/rewrite_amd64_en-US.msi)
- Spustit v CMD:
```bat
%windir%\system32\inetsrv\appcmd unlock config -section:system.webServer/handlers
%windir%\system32\inetsrv\appcmd unlock config -section:system.webServer/modules
```
- Vytvořit klasický IIS web (žádná změna konfigurace navíc není třeba)
- Naklonovat přes git/stáhnout zip a rozbalit do složky IIS webu
- Ve složce IIS webu spustit:
```bat
npm install
npm run build
```
- Restartovat IIS web

Updating to 4.0.0
Updating to 4 is as easy as updating your Angular dependencies to the latest version, and double checking if you want animations. This will work for most use cases.

On Linux/Mac: 
npm install @angular/{common,compiler,compiler-cli,core,forms,http,platform-browser,platform-browser-dynamic,platform-server,router,animations}@latest typescript@latest --save 
On Windows:
npm install @angular/common@latest @angular/compiler@latest @angular/compiler-cli@latest @angular/core@latest @angular/forms@latest @angular/http@latest @angular/platform-browser@latest @angular/platform-browser-dynamic@latest @angular/platform-server@latest @angular/router@latest @angular/animations@latest typescript@latest --save
Then run whatever ng serve or npm start command you normally use, and everything should work.
If you rely on Animations, import the new BrowserAnimationsModule from @angular/platform-browser/animations in your root NgModule. Without this, your code will compile and run, but animations will trigger an error. Imports from @angular/core were deprecated, use imports from the new package import { trigger, state, style, transition, animate } from '@angular/animations';.
We are beginning work on an interactive Angular Update Guide if you would like to see more information about making any needed changes to your application.
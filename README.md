# Deploy to Firebase hosting

## Deploy at local

<details>
<summary>Install Angular CLI</summary>

``` PowerShell
npm install -g @angular/cli

added 209 packages, and audited 210 packages in 32s

25 packages are looking for funding
  run `npm fund` for details

found 0 vulnerabilities
```

</details>

<details>
<summary>Compiling src</summary>

``` PowerShell
npm install
npm WARN deprecated request@2.88.2: request has been deprecated, see https://github.com/request/request/issues/3142
npm WARN deprecated har-validator@5.1.5: this library is no longer supported
npm WARN deprecated uuid@3.4.0: Please upgrade  to version 7 or higher.  Older versions may use Math.random() in certain circumstances, which is known to be problematic.  See https://v8.dev/blog/math-random for details.
npm WARN deprecated protractor@7.0.0: We have news to share - Protractor is deprecated and will reach end-of-life by Summer 2023. To learn more and find out about other options please refer to this post on the Angular blog. Thank you for using and contributing to Protractor. https://goo.gle/state-of-e2e-in-angular

added 1126 packages, and audited 1127 packages in 1m

122 packages are looking for funding
  run `npm fund` for details

found 0 vulnerabilities
PS C:\Users\nagar\Development\Nodejs\Angular\angular-tutorial> ng serve
Your global Angular CLI version (14.2.1) is greater than your local version (14.0.7). The local Angular CLI version is used.

To disable this warning use "ng config -g cli.warnings.versionMismatch false".
? Would you like to share anonymous usage data about this project with the Angular Team at
Google under Google’s Privacy Policy at https://policies.google.com/privacy. For more
details and how to change this setting, see https://angular.io/analytics. No
Global setting: not set
Local setting: disabled
Effective status: disabled
✔ Browser application bundle generation complete.

Initial Chunk Files   | Names         |  Raw Size
vendor.js             | vendor        |   2.47 MB |
polyfills.js          | polyfills     | 320.03 kB |
styles.css, styles.js | styles        | 213.95 kB |
main.js               | main          |  39.26 kB |
runtime.js            | runtime       |   6.53 kB |

                      | Initial Total |   3.04 MB

Build at: 2022-09-04T05:26:28.877Z - Hash: 0e0e3a979fce0735 - Time: 20108ms

** Angular Live Development Server is listening on localhost:4200, open your browser on http://localhost:4200/ **


√ Compiled successfully.
✔ Browser application bundle generation complete.

5 unchanged chunks

Build at: 2022-09-04T05:26:29.664Z - Hash: 0e0e3a979fce0735 - Time: 551ms

√ Compiled successfully.
```

</details>

## Deploy to Firebase

<details>
<summary>Build</summary>

``` PowerShell
ng build
Your global Angular CLI version (14.2.1) is greater than your local version (14.0.7). The local Angular CLI version is used.

To disable this warning use "ng config -g cli.warnings.versionMismatch false".
✔ Browser application bundle generation complete.
✔ Copying assets complete.
⠋ Generating index html...1 rules skipped due to selector errors:
  router-outlet+* -> Cannot read properties of undefined (reading 'type')
✔ Index html generation complete.

Initial Chunk Files           | Names         |  Raw Size | Estimated Transfer Size
main.2ce0f8130e8e1c44.js      | main          | 253.43 kB |                66.37 kB
polyfills.0f055e06614789ce.js | polyfills     |  33.09 kB |                10.69 kB
styles.510afded6253d1c1.css   | styles        |   1.33 kB |               440 bytes
runtime.04bc5d4d57ef41c6.js   | runtime       |   1.06 kB |               598 bytes

                              | Initial Total | 288.91 kB |                78.07 kB

Build at: 2022-09-04T05:52:29.884Z - Hash: 7d245e5a1b92f7d8 - Time: 25901ms
```

</details>

<details>
<summary>Install firebase-tools</summary>

``` PowerShell
npm install -g firebase-tools
npm WARN deprecated har-validator@5.1.3: this library is no longer supported
npm WARN deprecated debug@4.1.1: Debug versions >=3.2.0 <3.2.7 || >=4 <4.3.1 have a low-severity ReDos regression when used in a Node.js environment. It is recommended you upgrade to 3.2.7 or 4.3.1. (https://github.com/visionmedia/debug/issues/797)
npm WARN deprecated uuid@3.4.0: Please upgrade  to version 7 or higher.  Older versions may use Math.random() in certain circumstances, which is known to be problematic.  See https://v8.dev/blog/math-random for details.
npm WARN deprecated request@2.88.2: request has been deprecated, see https://github.com/request/request/issues/3142

added 706 packages, and audited 707 packages in 2m

39 packages are looking for funding
  run `npm fund` for details

19 vulnerabilities (13 moderate, 6 high)

To address issues that do not require attention, run:
  npm audit fix

To address all issues (including breaking changes), run:
  npm audit fix --force

Run `npm audit` for details.
PS C:\Users\nagar\Development\Nodejs\Angular\angular-tutorial> npm audit fix --force
npm WARN using --force Recommended protections disabled.

removed 1 package, and audited 1127 packages in 3s

122 packages are looking for funding
  run `npm fund` for details

found 0 vulnerabilities
```

</details>

<details>
<summary>Firebase login</summary>

``` PowerShell
firebase login
i  Firebase optionally collects CLI and Emulator Suite usage and error reporting information to help improve our products. Data is collected in accordance with Google's privacy policy (https://policies.google.com/privacy) and is not used to identify you.

? Allow Firebase to collect CLI and Emulator Suite usage and error reporting information? Yes
i  To change your data collection preference at any time, run `firebase logout` and log in again.

Visit this URL on this device to log in:
https://accounts.google.com/xxx/

Waiting for authentication...

+  Success! Logged in as emailaddress@gmail.com
```

</details>

<details>
<summary>Firebase init</summary>

``` PowerSehll
firebase init

     ######## #### ########  ######## ########     ###     ######  ########
     ##        ##  ##     ## ##       ##     ##  ##   ##  ##       ##
     ######    ##  ########  ######   ########  #########  ######  ######
     ##        ##  ##    ##  ##       ##     ## ##     ##       ## ##
     ##       #### ##     ## ######## ########  ##     ##  ######  ########

You're about to initialize a Firebase project in this directory:

  C:\Users\nagar\Development\Nodejs\Angular\angular-tutorial\dist

? Are you ready to proceed? Yes
? Which Firebase features do you want to set up for this directory? Press Space to select features, then Enter to confirm your choices. Hosting: Configure files for Firebase Hosting and (optionally) set up GitHub Action deploys

=== Project Setup

First, let's associate this project directory with a Firebase project.
You can create multiple project aliases by running firebase use --add,
but for now we'll just set up a default project.

? Please select an option: Use an existing project
? Select a default Firebase project for this directory: my-first-firebase-8c604 (My First Firebase)
i  Using project my-first-firebase-8c604 (My First Firebase)

=== Hosting Setup

Your public directory is the folder (relative to your project directory) that
will contain Hosting assets to be uploaded with firebase deploy. If you
have a build process for your assets, use your build's output directory.

? What do you want to use as your public directory? public
? Configure as a single-page app (rewrite all urls to /index.html)? No
? Set up automatic builds and deploys with GitHub? No
+  Wrote public/404.html
+  Wrote public/index.html

i  Writing configuration info to firebase.json...
i  Writing project information to .firebaserc...
i  Writing gitignore file to .gitignore...

+  Firebase initialization complete!
```

</details>

<details>
<summary>cd dist</summary>

``` PowerShell
cd dist
```

</details>


<details>
<summary>Deploy</summary>

``` PowerSehll
firebase deploy

=== Deploying to 'my-first-firebase-8c604'...

i  deploying hosting
i  hosting[my-first-firebase-8c604]: beginning deploy...
i  hosting[my-first-firebase-8c604]: found 2 files in public
+  hosting[my-first-firebase-8c604]: file upload complete
i  hosting[my-first-firebase-8c604]: finalizing version...
+  hosting[my-first-firebase-8c604]: version finalized
i  hosting[my-first-firebase-8c604]: releasing new version...
+  hosting[my-first-firebase-8c604]: release complete

+  Deploy complete!

Project Console: https://console.firebase.google.com/project/my-first-firebase-8c604/overview
Hosting URL: https://my-first-firebase-8c604.web.app
```

</details>

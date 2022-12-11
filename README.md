<p align="center"> <img src="https://upload.wikimedia.org/wikipedia/commons/thumb/d/db/Npm-logo.svg/540px-Npm-logo.svg.png?20140904162625"> </p>

<h1 align="center">Npm 101</h1>

<br>

<p align="center">How to Update <b><i>Npm Packages</i></b> Safely With <b><i>Npm Check Updates</i></b></p>
<h1 align="center">
  
  ![image](https://user-images.githubusercontent.com/43164261/204070600-98d0ca44-9911-4a23-b54b-0c0e94f6bcec.png)
  
</h1>

### 1. Install NPM Check Updates.

  It’s often best to just install NPM check updates globally.
  ```bash
  npm install -g npm-check-updates
  ```
### 2. Run NPM Check Updates.

  If installed globaly:
  ```bash
  ncu
  ```
  OR:
  
  ```bash
  npx ncu
  ```
  
  Example output:
  ```bash
  [====================] 15/15 100%

  @ckeditor/ckeditor5-build-classic   ^29.0.0  →   ^35.3.2
  alpinejs                             ^2.7.3  →   ^3.10.5
  axios                               ^0.21.4  →    ^1.2.0
  datatables.net                     ^1.10.25  →   ^1.13.1
  datatables.net-dt                  ^1.10.25  →   ^1.13.1
  jquery-ui                           ^1.12.1  →   ^1.13.2
  notyf                                ^3.9.0  →   ^3.10.0
  postcss                             ^8.3.11  →   ^8.4.19
  postcss-import                      ^14.0.2  →   ^15.0.0
  postcss-nested                       ^5.0.6  →    ^6.0.0
  ```
  
   
### 3. Update Patches.

  First, I update all patches. Assuming the package maintainers are following semantic versioning, this shouldn’t break anything.
  ```bash
  npx ncu -u -t patch
  ```
  Run ``npm i``, ensure everything is still working, and commit the changes (so I can revert if necessary).
  
### 4. Update Minor Versions.

  Next, I update all minor updates. Again, assuming the package maintainers are following semantic versioning, this shouldn’t break anything.
  ```bash
  npx ncu -u -t minor
  ```
<h1 align="center">
  
  ![image](https://letscodepare.com/assets/images/npm-resolving-eacces-permissions-denied/i-dont-know.gif)
  
</h1>


# JellySkin-J0nan:
### A modification of JellySkin by @prayag17

![NPM_version](https://img.shields.io/npm/v/jellyskin-j0nan/latest?style=for-the-badge)
  
# Usage :information_source: :
- To use the JellySkin theme copy the line below into "Dashboard -> General -> Custom CSS" and click save, it will apply immediately server-wide to all users on top of any theme they may be using. To remove the theme, clear the "Custom CSS" field and then click save. <b>NOTE: Theme may not work when using Nginx Reverse Proxy. Scroll down below to learn how to fix this.

  ```css
  @import url("https://cdn.jsdelivr.net/npm/jellyskin-j0nan@latest/dist/main.css");
  ```

- To enable Logos add this to custom css:
  ```css
  @import url("https://cdn.jsdelivr.net/npm/jellyskin-j0nan@latest/dist/logo.css");
  ```
  
- You can also use Jellyfin-Skin-Manager-Plugin : https://github.com/danieladov/jellyfin-plugin-skin-manager

# Addons :electric_plug: :
- ## Improve Performance:
    If you fix performace issues like stutter while normally browsing jellyfin while use JellySkin, try adding this to custom css to fix the issue:
    
    ```css
    @import url("https://cdn.jsdelivr.net/npm/jellyskin-j0nan@latest/dist/addons/improvePerformance.css")
    ```
    
    :warning: This removes the background blur from dialogs, gradient scroll in and out "bars" and animated mesh gradient from login page (replaced by normal gradient animation)
    
- ## Compact Poster:
    Want to use compact posters instead of normal cards, add this to you custom css:
    
    ```css
    @import url("https://cdn.jsdelivr.net/npm/jellyskin-j0nan@latest/dist/addons/compactPosters.css");
    ```
    
    Example:\
    ![image](https://user-images.githubusercontent.com/55829513/200132447-5307c19f-97e5-4022-ab42-c5b8bf632d6b.png)

- ## Using/Changing default gradient accent:
    If you want want to change the default jellyfin gradient accent to some other preset gradient use:
    
    - ### Mauve
      ```css
      @import url("https://cdn.jsdelivr.net/npm/jellyskin-j0nan@latest/dist/addons/gradients/mauve.css");
      ```
      Example:\
      ![image](https://user-images.githubusercontent.com/55829513/200132732-d188392a-5642-47f7-bb62-f204a85d992e.png)

    - ### NightSky
      ```css
      @import url("https://cdn.jsdelivr.net/npm/jellyskin-j0nan@latest/dist/addons/gradients/nightSky.css");
      ```
      Example:\
      ![image](https://user-images.githubusercontent.com/55829513/200132808-5b02c8e9-29c1-4a6b-ad3c-514588cf717a.png)

    - ### Sea
      ```css
      @import url("https://cdn.jsdelivr.net/npm/jellyskin-j0nan@latest/dist/addons/gradients/sea.css");
      ```
      Example:\
      ![image](https://user-images.githubusercontent.com/55829513/200132840-984deaf3-c228-4092-be8f-44c325d57782.png)
      
    - ### Custom:
      If you need to add your own gradient use:
      ```css
      :root {
        --accent1-light: YOUR ACCENT COLOR 1(LIGHTER SHADE);
        --accent1-dark: YOUR ACCENT COLOR 1(DARKER SHADE);
        --accent1-light-opacity1: YOUR ACCENT COLOR 1(WITH OPACITY 0.4);
        --accent2-light: YOUR ACCENT COLOR 2(LIGHTER SHADE);
        --accent2-dark: YOUR ACCENT COLOR 2(DARKER SHADE);
      }
      ```

# Screenshot :framed_picture: :
- ### Login Page:
    ![loginPage](https://user-images.githubusercontent.com/55829513/200134094-9bafba9d-4cfa-48c3-bbf4-e01bc21ecdd1.png)

- ### Home Screen:
    ![Home Screen](https://user-images.githubusercontent.com/55829513/200134098-6463a6e7-95bb-4af6-a451-b6ac5ef7abad.png)

- ### Library View:
    ![LibView](https://user-images.githubusercontent.com/55829513/200133209-413d6e6c-3569-4aaf-9db7-f576c141f519.png)
    
- ### Title Screen:
    ![TitleView](https://user-images.githubusercontent.com/55829513/200133240-075f604d-ae7f-48cb-9a42-445d8f3ef427.png)

- ### Episode View:
    ![EpisodeView](https://user-images.githubusercontent.com/55829513/200133258-4eabfc3d-475f-4b42-a496-bc2de60c11a5.png)

- ### Settings:
    ![SettingsView](https://user-images.githubusercontent.com/55829513/200133273-3ff7ba73-bad2-4f7c-88b1-e8298d246587.png)

- ### Dashboard:
    ![DashboardView](https://user-images.githubusercontent.com/55829513/200133302-5d7e7ac1-201b-4cb4-a839-ee53c5c6a6f2.png)

- ### Dialog:
    ![DialogView](https://user-images.githubusercontent.com/55829513/200133331-ee7838d0-6318-4175-b969-c06647bf65a0.png)

# Common Problem Fixes :question: :
- ### Unable to see blured background in Firefox:
  Deaktiviert From version 70: this feature is behind the `layout.css.backdrop-filter.enabled` preference (needs to be set to true) and the `gfx.webrender.all`  preference (needs to be set to true).
  To change preferences in Firefox, visit about:config
  
- ### Logos are not visible even with `logo.css`:
  - Get Fanart Plugin, Dashboard -> Plugin -> Catalog
  - Enable Fanart as a metadata provider for your libraries in the library settings, Dashboard -> Library -> Click on 3 dots on your Library -> Manage Library -> Scroll to find Metadata provider and enable Fanart in all of them.
  - Rescan your drive and also enable `Replace Metadata` and scan

- ### Background not visible:
  - Go to Seetiing -> Display -> and enable `Backdrops` option

- ### How to report a Bug or request a Feature?
  - Go to https://github.com/J0nan/JellySkin/issues
  - Click on `New Issue` button
  - Select the appropriate template

- ### How to contribute:
  - Fork this repository.
  - Add your patch/feature
  - Create a pull request and thats it

# Developers

Remember to change the version in the [package.json](package.json) file.

```
npm install
```

```
npm run build
```

```
npm publish
```

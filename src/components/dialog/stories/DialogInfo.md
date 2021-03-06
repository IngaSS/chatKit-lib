
### Instalation
```
 $ npm i --save Sova-Chat-Kit
```
### Quik start
  In your App.js file:
  ```
  import {CkComponents} from 'Sova-Chat-Kit'
  ...
  <CkComponents.Badge />
  ...
  ```
### Component Props
```
{
  /**
 * Should component use ckStore as storage
 @default true
* / 
  ckStore?: boolean
 }
```
### Configuration
   Component get configuration info from storage. Badge touch 4 global keys from store: 
   - UIManagment - control UI
   - Settings - control media info
   - Styles - control styles packets
   - Languages - controls Languages packets
##### UIManagment
 Props from ```UIManagment```:
  ```
  {
  /**
 * Should component show title
  @default true
* / 
  "showTitle": boolean,
  /**
 * Should component show avatar
 @default false
* / 
  "showAvatar": boolean
  }
  ```
##### Settings
Props from ```Settings```:
  ```
  {
  /**
 * Path to the image which will be shown as avatar
  @default ''
* / 
  "avatar": string,
  }
  ```
##### Styles
Props from ```Styles```:
  ```
  {
       /**
 * Styles for main container
  @default {}
* / 
      "mainContainer": object,
      /**
 * Styles for avatar container container
  @default {}
* / 
      "avatarContainer": object,
      /**
 * Styles for tag <img/>
  @default  {
        "width": "70px",
        "height": "70px"
      }
* / 
      "image": object,
      /**
 * Styles for title container
  @default  {
        "padding": "10px",
        "width": "100px",
        "borderRadius": "10px",
        "fontSize": "24px",
        "backgroundColor": "#4a76a8",
        "color": "white",
        "textAlign": "center"
      }
* / 
      "titleContainer": object,
  }
  ```
  Writing css properties in ```kebab-case``` like regular css, you write them in ```camelCase```
  
##### Languages
Props from ```Languages```:
  ```
  {
  /**
 * Text in Title
  @default Chat Kit
* / 
 "title": string,
  }
  ```
  ### Customization
  To custom Badge component, you should use ckAPIMethods, which will allow you to change values in ckStore
  ##### UIManagment
  
  ```
  ckAPIMethods.uiManagment('setUpBadge', { showAvatar: [value], showTitle: [value] })
  ```
  ##### Settings 
   ```
  ckAPIMethods.settings('changeAvatar', [path])
  ```
  ##### Styles
   ```
  ckAPIMethods.styles('changeBadge', {
    themeName: [theme name, wich styles you want to change],
    data: {
      [mainContainer styles],
      [avatarContainer styles],
      [image styles],
      [titleContainer styles] 
    },
  })
  ```
  ##### Languages
   ```
  ckAPIMethods.languages('changeBadge', {
  language: [language name, wich packet you want to change],
    data: {
       [text title]
    }, 
  })
  ```
  
  
  
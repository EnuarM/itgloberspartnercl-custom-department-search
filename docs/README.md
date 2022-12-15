# CUSTOM DEPARTMENT SEARCH  

This component allows users makes custom searchs by department. The select input contains all store departments. On the search bar you can type the product you are looking for and make a search in department previously selected.

![preview](./custom-search.png)

## Configuration 
### **Step 1** -  Basic setup

Access the VTEX IO [basic setup guide](https://vtex.io/docs/getting-started/build-stores-with-store-framework/1) and follow all the given steps. 

By the end of the setup, you should have the VTEX command line interface (Toolbelt) installed along with a developer workspace you can work in.

---
### **Step 2** - Cloning the repository

[Clone](https://help.github.com/en/github/creating-cloning-and-archiving-repositories/cloning-a-repository) this repository to your local files to be able to effectively start working on it.

Then, access the repository's directory using your terminal. 

---

### **Step 3** - Link this repository to your current project

Then time has come to upload all the changes you made in your local files to the platform. For that, use the `vtex link` command. 

If the process runs without any errors, the following message will be displayed: `App linked successfully`. Then, run the `vtex browse` command to open a browser window having your linked store in it.

This will enable you to see the applied changes in real time, through the account and workspace in which you are working.

---

### **Step 4** - Adding the app on your project

1. Adding the app as a theme dependency in the `manifest.json` file;
```json
  "dependencies": {
    "itgloberspartnercl.custom-department-search": "0.x"
  }
```
2. Declaring the app's main block in a given theme template or inside another block from the theme.

```json
{
  "header": {
    "blocks": ["header-layout.desktop", "header-layout.mobile"]
  },
  "header.full": {
    "blocks": ["header-layout.desktop", "header-layout.mobile"]
  },

  "header-layout.desktop": {
    "children": [
      "custom-department-search"
    ]
  } 
}
```
### **Step 5** -  Installing required apps

In order to use Store Framework and work on your store theme, it is needed to have both `vtex.store-sitemap` and `vtex.store` installed.

Run  `vtex list`  and check whether those apps are already installed. 

If they aren't, run the following command to install them: 

`vtex install vtex.store-sitemap vtex.store -f`

---
### **Step 6** -  Check the app is connected

By running `vtex list`,  you can verify if the app is linked. On your Linked Apps you must have 

```json
itgloberspartnercl.custom-department-search    0.0.1
```

---
## Customization

`No CSS Handles are available yet for the app customization.`

<!-- DOCS-IGNORE:start -->

## Contributors ✨

Thanks goes to these wonderful people:
1. Enuar Montaña

---- 

Check out some documentation models that are already live: 
- [SearchBar](https://developers.vtex.com/vtex-developer-docs/docs/vtex-store-components-searchbar)


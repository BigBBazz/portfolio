# Personal Website

- Aim
- Design Phase
- Data

### Aim

The aim of this project was to build a personal website that could display my projects and resume. The website design should also allow the easy addition of new features such as a blog.

### Design Phase

The client side was made with React with client side routing using React-Router. This choice was made because React-Router has powerful features that allows the easy implementation of new features such as a peronal blog. For more information on React-Router see the technical docs or go to the React-Router website.

## Routes

The route structure of the website consists of a "root" route from which all subsequent routes a decented from. The root route has an index route which acts as a default route. This displays information when the user is at the "parent" rout without and children routes rendered.

- root
- about
- contact
- portfolio

The index route contains the information that is displayed when the user lands on the home page of the website. 

The "about" route contains more detailed information about myself and my career.

The contact route contains information on how to get in touch with me. It has a build in email request form.

The portfolio route contains the data on each project.

## Styling

Styling is done with scss. All scss files a organised within a single folder called "styles". Within the "style" folder there is a single file called "main.scss" and three folders called abstracts, compononts, and routes. Each folder containes a file called "_global.scss" which imports all other scss files within that folder. For example, the components folder contains a scss file for each component, these files are all imported into the "_global.scss" file for that folder. In turn, all the "_global.scss" files are imported into the "main.scss" file. This file is imported into the "App.js" file with applies all the styles to the project.

### Data

The data for the project component comes from github. Each project has a markdown file wich is imported into the component and transformed into html using react-markdown.

# Personal Website

- Aim
- Design Phase
- Routes
- Styling
- Data

### Aim

The aim of this project was to build a personal website that could display my projects and resume.

### Design Phase

Rexmix was used to build the portfolio website and Netlify was used for hosting.

### Routes

The route structure for this website follows the "conventional route folders" pattern as specified in the Remix documentation:
```
app/
├── routes/
│   ├── _index/
│   │   ├── LinkTile.tsx
│   │   └── Modal.tsx
│   │   └── route.tsx
│   ├── about/
│   │   └── route.tsx
│   ├── contact/
│   │   └── route.tsx
│   ├── projects.$projectId/
│   │   └── route.tsx
└── root.tsx
```
The "index" route contains a brief introduction about myself, links to three of my projects, and a link for my resume.

The "about" route contains more detailed information about myself and my career.

The "contact" route contains information on how to get in touch with me. It has a build in email request form.

### Styling

Styling is done with plain css. All css files are organised within a single folder called "styles". 
```
app/
├── routes/
├── styles/
```
Within this folder there is a filed called "shared.css" which is imported in the root.tsx.
The shared css file contains global styles for all parts of the website. If a route contains one or more components a folder named after the route will contain all css files for that route. Otherwise the route css file will not be located in a folder. This is demonstrated in the diagram below.
```
app/
├── styles/
│   ├── _index/
│   │   ├── index.css
│   │   ├── LinkTile.css
│   ├── about/
│   │   └── route.tsx
│   ├── contact/
│   │   └── route.tsx
│   ├── projects.$projectId/
│   │   └── route.tsx
└── root.tsx
```
### Data

The data for the project component comes from github. Each project has a markdown file wich is imported using "loader" and "useLoaderData" Remix API's.

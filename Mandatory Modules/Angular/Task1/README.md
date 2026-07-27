# Task 1: Environment Setup, Project Structure & First Component

## Objective

To set up an Angular development environment, create the **Student Course Portal** project using Angular CLI, understand the generated project structure, and build the first Angular components. :contentReference[oaicite:0]{index=0}

---

## Technologies Used

- Angular 20
- TypeScript
- HTML5
- CSS3
- Node.js
- npm
- Angular CLI
- Visual Studio Code

---

## Prerequisites

- Install Node.js (LTS)
- Install Angular CLI

```bash
npm install -g @angular/cli
```

---

# Project Creation

Create a new Angular project.

```bash
ng new student-course-portal --routing --style=css
```

Move into the project directory.

```bash
cd student-course-portal
```

Run the application.

```bash
ng serve
```

Open the application in the browser.

```
http://localhost:4200
```

---

# Build Project

Generate the production build.

```bash
ng build
```

The compiled application will be generated inside the **dist/** folder.

---

# Components Created

Generate the required components.

```bash
ng generate component components/header

ng generate component pages/home

ng generate component pages/course-list

ng generate component pages/student-profile
```

---

# Header Component

**header.component.html**

```html
<nav>
  <h2>Student Course Portal</h2>

  <a href="#">Home</a>
  <a href="#">Courses</a>
  <a href="#">Profile</a>
</nav>
```

---

# Home Component

**home.component.html**

```html
<h1>Welcome to Student Course Portal</h1>

<p>
  Manage your courses, enrollments and profile from one place.
</p>

<div>
  <p>Courses Available: 12</p>
  <p>Enrolled: 3</p>
  <p>GPA: 3.8</p>
</div>
```

---

# App Component

Replace the default content in **app.component.html**

```html
<app-header></app-header>

<router-outlet></router-outlet>
```

---

# Project Structure

```
student-course-portal
│
├── src
│   ├── app
│   │   ├── components
│   │   │      └── header
│   │   ├── pages
│   │   │      ├── home
│   │   │      ├── course-list
│   │   │      └── student-profile
│   │   ├── app.component.html
│   │   └── app.component.ts
│   │
│   ├── assets
│   ├── index.html
│   └── main.ts
│
├── angular.json
├── package.json
└── tsconfig.json
```

---

## Project Structure Overview

| File | Purpose |
|------|----------|
| angular.json | Angular workspace configuration |
| package.json | Project dependencies and scripts |
| tsconfig.json | TypeScript compiler configuration |
| src/main.ts | Application entry point |
| src/index.html | Main HTML page |
| app.component.ts | Root component |
| app.component.html | Root template |

---

## Maven/Build Equivalent

Install project dependencies.

```bash
npm install
```

Run development server.

```bash
ng serve
```

Create production build.

```bash
ng build
```

---

> **📷 Output Screenshot:**  

<img width="1600" height="691" alt="image" src="https://github.com/user-attachments/assets/8c64a34d-bc1f-4cd9-a4fd-5a98fb6aa857" />

---


## Conclusion

In this hands-on, a new Angular project named **Student Course Portal** was created and configured successfully. The application was built using Angular CLI, organized with reusable components, and verified by running it in the browser. This serves as the foundation for the remaining hands-on exercises, where additional Angular features will be implemented. :contentReference[oaicite:2]{index=2}

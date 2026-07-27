# Task 2: Data Binding, Lifecycle Hooks & Component Communication

## Objective

To implement Angular data binding techniques, lifecycle hooks, and parent-child communication using **@Input** and **@Output** in the Student Course Portal application. :contentReference[oaicite:0]{index=0}

---

## Technologies Used

- Angular 20
- TypeScript
- HTML5
- CSS3
- Angular FormsModule

---

# Data Binding

## Home Component

**home.component.ts**

```typescript
import { Component } from '@angular/core';

@Component({
  selector: 'app-home',
  templateUrl: './home.component.html',
  styleUrls: ['./home.component.css']
})
export class HomeComponent {

  portalName = "Student Course Portal";

  isPortalActive = true;

  message = "";

  searchTerm = "";

  onEnrollClick() {
    this.message = "Enrollment opened!";
  }

}
```

---

**home.component.html**

```html
<h1>{{ portalName }}</h1>

<button
  [disabled]="!isPortalActive"
  (click)="onEnrollClick()">
  Enroll Now
</button>

<p>{{ message }}</p>

<input
  [(ngModel)]="searchTerm"
  placeholder="Search Course">

<p>Searching for: {{ searchTerm }}</p>
```

---

## Import FormsModule

```typescript
import { FormsModule } from '@angular/forms';
```

---

# Lifecycle Hooks

```typescript
import {
  Component,
  OnInit,
  OnDestroy
} from '@angular/core';

export class HomeComponent implements OnInit, OnDestroy {

  ngOnInit() {
    console.log("HomeComponent initialized - courses loaded");
  }

  ngOnDestroy() {
    console.log("HomeComponent destroyed");
  }

}
```

---

# Course Card Component

Generate the component.

```bash
ng generate component components/course-card
```

---

## course-card.component.ts

```typescript
import {
  Component,
  Input,
  Output,
  EventEmitter,
  OnChanges,
  SimpleChanges
} from '@angular/core';

@Component({
  selector: 'app-course-card',
  templateUrl: './course-card.component.html'
})
export class CourseCardComponent implements OnChanges {

  @Input()
  course: any;

  @Output()
  enrollRequested = new EventEmitter<number>();

  ngOnChanges(changes: SimpleChanges) {

    console.log(changes);

  }

}
```

---

## course-card.component.html

```html
<h3>{{ course.name }}</h3>

<p>{{ course.code }}</p>

<p>{{ course.credits }}</p>

<button
(click)="enrollRequested.emit(course.id)">
Enroll
</button>
```

---

# Course List Component

**course-list.component.ts**

```typescript
courses = [

  {
    id:1,
    name:'Angular',
    code:'CS101',
    credits:4
  },

  {
    id:2,
    name:'Java',
    code:'CS102',
    credits:3
  },

  {
    id:3,
    name:'Spring Boot',
    code:'CS103',
    credits:4
  },

  {
    id:4,
    name:'Python',
    code:'CS104',
    credits:3
  },

  {
    id:5,
    name:'Database',
    code:'CS105',
    credits:4
  }

];

selectedCourseId:number=0;

onEnroll(id:number){

  console.log("Enrolling in course : "+id);

  this.selectedCourseId=id;

}
```

---

**course-list.component.html**

```html
<app-course-card

*ngFor="let c of courses"

[course]="c"

(enrollRequested)="onEnroll($event)">

</app-course-card>

<p *ngIf="selectedCourseId">

Selected Course ID : {{ selectedCourseId }}

</p>
```

---

## Run Application

```bash
ng serve
```

---

> **📷 Output Screenshot:**  

<img width="1600" height="710" alt="image" src="https://github.com/user-attachments/assets/938c2061-850d-4865-a963-7e07a1a72491" />


---

## Conclusion

This hands-on introduced Angular's core component interaction concepts. By implementing data binding, lifecycle hooks, and parent-child communication, the Student Course Portal became interactive and reusable, laying the foundation for more advanced Angular features in subsequent exercises. :contentReference[oaicite:2]{index=2}

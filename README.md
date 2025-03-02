import { Component } from '@angular/core';
import { FormGroup, FormControl } from '@angular/forms';

@Component({
  selector: 'app-help-desk',
  templateUrl: './help-desk.component.html',
  styleUrls: ['./help-desk.component.scss']
})
export class HelpDeskComponent {
  helpDeskForm = new FormGroup({
    name: new FormControl(''),
    prn: new FormControl(''),
    department: new FormControl(''),
    email: new FormControl(''),
    title: new FormControl(''),
    description: new FormControl('')
  });

  onSubmit() {
    console.log(this.helpDeskForm.value);
  }
}


<form [formGroup]="helpDeskForm" (ngSubmit)="onSubmit()">
  <mat-form-field>
    <mat-label>Name</mat-label>
    <input matInput formControlName="name">
  </mat-form-field>

  <mat-form-field>
    <mat-label>PRN No</mat-label>
    <input matInput formControlName="prn">
  </mat-form-field>

  <mat-form-field>
    <mat-label>Department</mat-label>
    <input matInput formControlName="department">
  </mat-form-field>

  <mat-form-field>
    <mat-label>Email</mat-label>
    <input matInput formControlName="email" type="email">
  </mat-form-field>

  <mat-form-field>
    <mat-label>Title of Enquiry</mat-label>
    <input matInput formControlName="title">
  </mat-form-field>

  <mat-form-field>
    <mat-label>Description</mat-label>
    <textarea matInput formControlName="description"></textarea>
  </mat-form-field>

  <button mat-raised-button color="primary" type="submit">Submit</button>
</form>

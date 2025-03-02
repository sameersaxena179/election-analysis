import { Component } from '@angular/core';
import { MatDatepickerModule } from '@angular/material/datepicker';
import { MatNativeDateModule } from '@angular/material/core';
import { MatInputModule } from '@angular/material/input';
import { MatFormFieldModule } from '@angular/material/form-field';
import { FormsModule } from '@angular/forms';
import { NgIf } from '@angular/common';

@Component({
  selector: 'app-calendar',
  standalone: true,
  imports: [MatDatepickerModule, MatNativeDateModule, MatInputModule, MatFormFieldModule, FormsModule, NgIf],
  template: `
    <mat-form-field appearance="fill">
      <mat-label>Pick a date</mat-label>
      <input matInput [matDatepicker]="picker" [(ngModel)]="selectedDate">
      <mat-datepicker-toggle matIconSuffix [for]="picker"></mat-datepicker-toggle>
      <mat-datepicker #picker></mat-datepicker>
    </mat-form-field>
    <p *ngIf="selectedDate">Selected Date: {{ selectedDate | date }}</p>
  `
})
export class CalendarComponent {
  selectedDate: Date | null = null;
}

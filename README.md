<div class="help-desk-container">
  <h2>Help Desk</h2>
  <form [formGroup]="helpDeskForm" (ngSubmit)="onSubmit()">
    
    <div class="form-group">
      <mat-form-field appearance="outline">
        <mat-label>Name</mat-label>
        <input matInput formControlName="name">
      </mat-form-field>

      <mat-form-field appearance="outline">
        <mat-label>PRN No.</mat-label>
        <input matInput formControlName="prn">
      </mat-form-field>
    </div>

    <div class="form-group">
      <mat-form-field appearance="outline">
        <mat-label>Department</mat-label>
        <mat-select formControlName="department">
          <mat-option value="IT">IT</mat-option>
          <mat-option value="CSE">CSE</mat-option>
          <mat-option value="Mechanical">Mechanical</mat-option>
        </mat-select>
      </mat-form-field>

      <mat-form-field appearance="outline">
        <mat-label>Email</mat-label>
        <input matInput type="email" formControlName="email">
      </mat-form-field>
    </div>

    <mat-form-field appearance="outline" class="full-width">
      <mat-label>Title of Enquiry</mat-label>
      <input matInput formControlName="title">
    </mat-form-field>

    <mat-form-field appearance="outline" class="full-width">
      <mat-label>Description</mat-label>
      <textarea matInput rows="3" formControlName="description"></textarea>
    </mat-form-field>

    <div class="button-group">
      <button mat-raised-button color="primary" type="submit" [disabled]="helpDeskForm.invalid">Submit</button>
      <button mat-stroked-button color="warn" type="button" (click)="onCancel()">Cancel</button>
    </div>

  </form>
</div>



.help-desk-container {
  width: 60%;
  margin: auto;
  padding: 20px;
  background: #f5f5f5;
  border-radius: 8px;
}

.form-group {
  display: flex;
  justify-content: space-between;
}

mat-form-field {
  width: 48%;
}

.full-width {
  width: 100%;
}

.button-group {
  display: flex;
  justify-content: flex-end;
  gap: 10px;
  margin-top: 20px;
}

import { Component } from '@angular/core';
import { FormBuilder, FormGroup, Validators } from '@angular/forms';

@Component({
  selector: 'app-login',
  standalone: true,
  imports: [ReactiveFormsModule],
  templateUrl: './login.component.html',
  styleUrls: ['./login.component.css']
})
export class LoginComponent {
  loginForm: FormGroup;

  constructor(private fb: FormBuilder) {
    this.loginForm = this.fb.group({
      username: ['', Validators.required],
      password: ['', Validators.required]
    });
  }

  onSubmit() {
    if (this.loginForm.valid) {
      console.log('Login Data:', this.loginForm.value);
    }
  }
}




<h2>Login</h2>
<form [formGroup]="loginForm" (ngSubmit)="onSubmit()">
  <label for="username">Username:</label>
  <input id="username" formControlName="username">
  
  <label for="password">Password:</label>
  <input id="password" type="password" formControlName="password">

  <button type="submit">Sign In</button>
</form>
<a routerLink="/signup">Don't have an account? Sign Up</a>





form {
  display: flex;
  flex-direction: column;
  max-width: 300px;
}





import { Component } from '@angular/core';
import { FormBuilder, FormGroup, Validators } from '@angular/forms';

@Component({
  selector: 'app-signup',
  standalone: true,
  imports: [ReactiveFormsModule],
  templateUrl: './signup.component.html',
  styleUrls: ['./signup.component.css']
})
export class SignupComponent {
  signupForm: FormGroup;

  constructor(private fb: FormBuilder) {
    this.signupForm = this.fb.group({
      username: ['', Validators.required],
      password: ['', Validators.required],
      confirmPassword: ['', Validators.required]
    });
  }

  onSubmit() {
    if (this.signupForm.valid) {
      console.log('Signup Data:', this.signupForm.value);
    }
  }
}






<h2>Sign Up</h2>
<form [formGroup]="signupForm" (ngSubmit)="onSubmit()">
  <label for="username">Username:</label>
  <input id="username" formControlName="username">
  
  <label for="password">Password:</label>
  <input id="password" type="password" formControlName="password">
  
  <label for="confirmPassword">Confirm Password:</label>
  <input id="confirmPassword" type="password" formControlName="confirmPassword">

  <button type="submit">Sign Up</button>
</form>
<a routerLink="/">Already have an account? Login</a>








form {
  display: flex;
  flex-direction: column;
  max-width: 300px;
}

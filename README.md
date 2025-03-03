<div class="container">
  <h2>GROCERY STORE MANAGEMENT SYSTEM</h2>
  <form [formGroup]="loginForm" (ngSubmit)="onSubmit()">
    <label>Username</label>
    <input formControlName="username" type="text" placeholder="Enter Username">
    <label>Password</label>
    <input formControlName="password" type="password" placeholder="Enter Password">
    <button type="submit">Sign In</button>
  </form>
  <p>Don't have an account? <a routerLink="/signup">Sign Up</a></p>
</div>


.container {
  width: 300px;
  margin: 100px auto;
  padding: 20px;
  border: 2px solid #000;
  text-align: center;
}

input {
  display: block;
  width: 100%;
  margin-bottom: 10px;
  padding: 8px;
}

button {
  width: 100%;
  padding: 10px;
  background-color: blue;
  color: white;
  border: none;
  cursor: pointer;
}


<div class="container">
  <h2>GROCERY STORE MANAGEMENT SYSTEM</h2>
  <form [formGroup]="signupForm" (ngSubmit)="onSubmit()">
    <label>Username</label>
    <input formControlName="username" type="text" placeholder="Enter Username">
    <label>Password</label>
    <input formControlName="password" type="password" placeholder="Enter Password">
    <label>Confirm Password</label>
    <input formControlName="confirmPassword" type="password" placeholder="Confirm Password">
    <button type="submit">Sign Up</button>
  </form>
  <p>Already have an account? <a routerLink="/login">Login</a></p>
</div>


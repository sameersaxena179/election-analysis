<!-- sidenav.component.html -->
<div class="sidenav-container">
  <div class="header">
    <div class="logo">
      <img src="assets/grocery-icon.svg" alt="Grocery Store Icon">
    </div>
    <div class="title">
      <h2>Grocery Store</h2>
      <p>Management System</p>
    </div>
  </div>

  <nav class="nav-links">
    <a [routerLink]="['/dashboard']" routerLinkActive="active" class="nav-item">
      <mat-icon>dashboard</mat-icon>
      <span>Dashboard</span>
    </a>

    <a [routerLink]="['/stocks']" routerLinkActive="active" class="nav-item">
      <mat-icon>inventory_2</mat-icon>
      <span>Stocks Management</span>
    </a>

    <a [routerLink]="['/shipment']" routerLinkActive="active" class="nav-item">
      <mat-icon>local_shipping</mat-icon>
      <span>Shipment Tracking</span>
    </a>

    <a [routerLink]="['/reports']" routerLinkActive="active" class="nav-item">
      <mat-icon>bar_chart</mat-icon>
      <span>Reports & Analytics</span>
    </a>

    <a [routerLink]="['/customers']" routerLinkActive="active" class="nav-item">
      <mat-icon>people</mat-icon>
      <span>Customer Management</span>
    </a>

    <a [routerLink]="['/food-safety']" routerLinkActive="active" class="nav-item">
      <mat-icon>article</mat-icon>
      <span>Food Safety Blogs</span>
    </a>

    <div class="divider"></div>

    <a [routerLink]="['/settings']" routerLinkActive="active" class="nav-item">
      <mat-icon>settings</mat-icon>
      <span>Settings</span>
    </a>

    <a [routerLink]="['/account']" routerLinkActive="active" class="nav-item">
      <mat-icon>account_circle</mat-icon>
      <span>My Account</span>
    </a>

    <a [routerLink]="['/help']" routerLinkActive="active" class="nav-item">
      <mat-icon>help</mat-icon>
      <span>Help & Support</span>
    </a>
  </nav>
</div>




/* sidenav.component.scss */
.sidenav-container {
  display: flex;
  flex-direction: column;
  width: 260px;
  height: 100%;
  background-color: #fff;
  border-right: 1px solid #e0e0e0;
  box-shadow: 0 0 10px rgba(0, 0, 0, 0.05);
}

.header {
  display: flex;
  align-items: center;
  padding: 20px;
  border-bottom: 1px solid #f0f0f0;
  margin-bottom: 10px;
  
  .logo {
    margin-right: 15px;
    
    img {
      width: 40px;
      height: 40px;
    }
  }
  
  .title {
    h2 {
      margin: 0;
      font-size: 16px;
      font-weight: 600;
      color: #333;
    }
    
    p {
      margin: 0;
      font-size: 12px;
      color: #666;
    }
  }
}

.nav-links {
  display: flex;
  flex-direction: column;
  flex: 1;
  padding: 10px 0;
  
  .nav-item {
    display: flex;
    align-items: center;
    padding: 12px 20px;
    color: #555;
    text-decoration: none;
    border-radius: 5px;
    margin: 5px 10px;
    transition: all 0.3s ease;
    
    mat-icon {
      margin-right: 15px;
      color: #666;
    }
    
    &:hover {
      background-color: #f5f5f5;
    }
    
    &.active {
      background-color: #3f51b5;
      color: white;
      
      mat-icon {
        color: white;
      }
    }
  }
}

.divider {
  height: 1px;
  background-color: #e0e0e0;
  margin: 15px 20px;
}

import { Component, Input } from '@angular/core';

@Component({
  selector: 'app-card',
  templateUrl: './card.component.html',
  styleUrls: ['./card.component.scss']
})
export class CardComponent {
  @Input() title: string = '';
  @Input() icon: string = '';
}



<div class="card">
  <img [src]="icon" [alt]="title">
  <p>{{ title }}</p>
</div>



.card {
  display: flex;
  flex-direction: column;
  align-items: center;
  background: white;
  padding: 15px;
  border-radius: 10px;
  box-shadow: 0 4px 10px rgba(0, 0, 0, 0.1);
  transition: 0.3s ease-in-out;
  width: 180px;
  text-align: center;

  img {
    width: 50px;
    height: 50px;
    margin-bottom: 10px;
  }

  p {
    font-size: 14px;
    font-weight: bold;
    color: #333;
  }

  &:hover {
    transform: translateY(-5px);
    box-shadow: 0 6px 12px rgba(0, 0, 0, 0.2);
  }
}






import { Component } from '@angular/core';

@Component({
  selector: 'app-collection',
  templateUrl: './collection.component.html',
  styleUrls: ['./collection.component.scss']
})
export class CollectionComponent {
  collections = [
    { name: 'Books', icon: 'assets/icons/books.png' },
    { name: 'Magazines', icon: 'assets/icons/magazines.png' },
    { name: 'Newspapers', icon: 'assets/icons/newspapers.png' },
    { name: 'CDs', icon: 'assets/icons/cds.png' },
    { name: 'DVDs', icon: 'assets/icons/dvds.png' },
    { name: 'Journals', icon: 'assets/icons/journals.png' }
  ];
}






<div class="page-container">
  <h2>Collection</h2>
  <div class="grid-container">
    <app-card *ngFor="let item of collections" [title]="item.name" [icon]="item.icon"></app-card>
  </div>
</div>





import { Component } from '@angular/core';

@Component({
  selector: 'app-ebooks',
  templateUrl: './ebooks.component.html',
  styleUrls: ['./ebooks.component.scss']
})
export class EbooksComponent {
  ebooks = [
    { name: 'IEEE (ASPP) Journals', icon: 'assets/icons/ieee.png' },
    { name: 'J-GATE Complete Database', icon: 'assets/icons/jgate.png' },
    { name: 'Elsevier Science Direct', icon: 'assets/icons/elsevier.png' },
    { name: 'ASCE', icon: 'assets/icons/asce.png' },
    { name: 'ASCE (New)', icon: 'assets/icons/asce-new.png' },
    { name: 'Manupatra Online', icon: 'assets/icons/manupatra.png' },
    { name: 'AIR Online', icon: 'assets/icons/air.png' },
    { name: 'Prowess IQ (Interactive Querying) I', icon: 'assets/icons/prowess1.png' },
    { name: 'Prowess IQ (Interactive Querying) II', icon: 'assets/icons/prowess2.png' },
    { name: 'E-Shodh Sindhu', icon: 'assets/icons/shodh1.png' },
    { name: 'E-Shodh Sindhu II', icon: 'assets/icons/shodh2.png' },
    { name: 'Previous Year Papers', icon: 'assets/icons/papers.png' }
  ];
}







<div class="page-container">
  <h2>E-Books (Database)</h2>
  <div class="grid-container">
    <app-card *ngFor="let item of ebooks" [title]="item.name" [icon]="item.icon"></app-card>
  </div>
</div>








.page-container {
  padding: 20px;
  text-align: left;

  h2 {
    font-size: 24px;
    margin-bottom: 20px;
  }

  .grid-container {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(180px, 1fr));
    gap: 20px;
  }
}

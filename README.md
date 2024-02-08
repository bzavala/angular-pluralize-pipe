# angular-pluralize-pipe
A pipe for pluralizing a word based on a 'count' parameter
---

**Add to component imports property**  
```
import { Component } from '@angular/core';
import { PluralizePipe } from './pluralize.pipe';

@Component({
  standalone: true,
  selector: 'app-root',
  templateUrl: './app.component.html',
  imports: [PluralizePipe],
  styles: [],
})
export class AppComponent {
  public words: string[] = [
    'apple',
    'banana',
    'orange',
    'strawberry',
    'moose',
    'goose',
    'piece',
    'charm',
    'cherry',
    'hero',
    'child',
    'person',
  ];
}
```

**Add to Angular template**  
``` {{ word | pluralize : words.length }}```

**Example usage:**  
```
@for(word of words; track word) {
  {{ word }} :
  {{ word | pluralize : words.length }}<Br />
}
```

**Example output:**  
apple : apples  
banana : bananas  
orange : oranges  
strawberry : strawberries  
moose : moose  
goose : geese  
piece : pieces  
charm : charms  
cherry : cherries  
hero : heroes  
child : children  
person : people  


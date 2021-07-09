# PinkRoccade
Slides and links on the training Angular, PinkRoccade, summer 2021

# Links
- `Angular Fundamentals` repo met voorbeeldcode: https://github.com/PeterKassenaar/voorbeeldenAngular2
- `Angular Advanced` repo met voorbeeldcode: https://github.com/PeterKassenaar/AngularAdvanced

# Extra links
- JavaScript Design Patterns, by Addy Osmani: https://addyosmani.com/resources/essentialjsdesignpatterns/book/
- Specific Angular Design Patterns book: https://www.amazon.co.uk/Angular-Design-Patterns-Implement-patterns/dp/1786461722/
- Java Design Patterns: https://refactoring.guru/design-patterns/java

## Examples
Content projection with default values. A bit cumbersome, but it works.
```javascript
<button class="my-button">
    <ng-content select="img"></ng-content>
    <!-- wrap the ng-content block with a local default template variable -->
    <span #ref><ng-content></ng-content></span>
    <!--    Check if there is content available,
            otherwise show default text-->
    <ng-container *ngIf="!ref.hasChildNodes()">
        Button text here
    </ng-container>
</button>
```

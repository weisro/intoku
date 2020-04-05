# Widgets
https://intokufileshare.blob.core.windows.net/widgets/intoku-widgets-es2015.js <br>
es5: https://intokufileshare.blob.core.windows.net/widgets/intoku-widgets-es5.js
## Account Button
Der Nutzer wird nach dem klick auf den Login button zur Login/Registration Seite umgeleitet.
Das Attribute account-url ist der Link zur Kundenseite, wenn der Nutzer eingeloggt ist.
Mit dem Attribute kann die Farbe des Knopfes festgelegt werden.
```html
<intoku-account-button color="white" account-url="/customer.html"></intoku-account-button>
```
## Logout Button
Der Nutzer wird nach dem klick auf den Login button zur Login/Registration Seite umgeleitet.
Das Attribute account-url ist der Link zur Kundenseite, wenn der Nutzer eingeloggt ist.
```html
<intoku-logout-button color="white" account-url="/customer.html"></intoku-logout-button>
```
## Customer Registration
Das Widget zur Registrierung eines Benutzer.
```html
<intoku-customer-registration></intoku-customer-registration>
```
## Email Verification
Dieses Widget muss sich auf der Seite befinden, zu der der Kunde nach der Bestätigung seiner Email weitergeleitet wird. (Link aus der Email)
```html
<intoku-email-verification></intoku-email-verification>
```

## Kundenwidget
Mit diesem Widget verschafft sich der Kunde einen Überblick über seine Termine und sein Profil.
```html
<intoku-customer-area></intoku-customer-area>
```

## Shop
Der Shop kann kann sowohl einen Kursplan als auch ein FlexTime Widget beinhalten.
Falls das Attribute schedule nicht gesetzt ist, dann werden beide Varianten angezeigt.
Das Attribute step bestimmt welche Schritt als erstes angezeigt wird: Kursplan oder der Einkaufswagen
Folgende Paramter steuern das Aussehen des Shops:
| Attribute     | Mögliche Werte| 
| ------------- |:-------------:|
| schedule      | classes, flexTime |
| account-url   | ein link zur Kundenseite |
| category      | YogaAndMore, Ayurveda, Therapie, HealthCoaching  |
| consultant-id  | Die Id des Teachers (kann aus der url des Teachers in der Manage app entnommen werden). Dabei werden nur die Kurse/Privatstunden dieses Teacher angezeigt.  |
| step      | courses, cart  |

Beispiel:
Um Einen Kursplan anzuzeigen und den Loginknopf auf eine weitere Seite mit dem Kundenwidget zu verlinken.
```html
 <intoku-shop schedule="classes" account-url="/customer.html"></intoku-shop>
```

## Shopping Cart Button
Zeigt das Einkaufswagensymbol und die Anzahl der Elemente im Einkaufswagen.
Mit dem Attribute color kann die Farebe des icons gesetzt werden.
```html
<intoku-shopping-cart-button></intoku-shopping-cart-button>
```


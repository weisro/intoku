# Widgets
https://intokufileshare.blob.core.windows.net/widgets/intoku-widgets-es2015.js <br>
es5: https://intokufileshare.blob.core.windows.net/widgets/intoku-widgets-es5.js

## Account Button

Der Nutzer wird nach dem klick auf den Login button zur Login/Registration Seite umgeleitet.
Das Attribute account-url ist der Link zur Kundenseite, wenn der Nutzer eingeloggt ist.
Mit dem Attribute kann die Farbe des Knopfes festgelegt werden.

``` html
<intoku-account-button color="white" account-url="/customer.html"></intoku-account-button>
```

## Logout Button

Der Nutzer wird nach dem klick auf den Login button zur Login/Registration Seite umgeleitet.
Das Attribute account-url ist der Link zur Kundenseite, wenn der Nutzer eingeloggt ist.

``` html
<intoku-logout-button color="white" account-url="/customer.html"></intoku-logout-button>
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

``` html
 <intoku-shop schedule="classes" account-url="/customer.html"></intoku-shop>
```

## Shopping Cart Button

Zeigt das Einkaufswagensymbol und die Anzahl der Elemente im Einkaufswagen.
Mit dem Attribute color kann die Farebe des icons gesetzt werden.

``` html
<intoku-shopping-cart-button></intoku-shopping-cart-button>
```

## Booking Button

Mit dem Booking Button können sowohl Klassen als auch Flex-Time Termine dem Shopping Cart hinzugefügt werden.

``` html
<stamy-booking-button></stamy-booking-button>
```

Das folgende Attribut entscheidet darüber, ob der Button für Klassen oder Flex-Time Kurse angewendet werden soll
| Attribut    | Beschreibung| 
| ------------- |:-------------:|
| type      | 'flex-time' oder 'class'  |

Folgende Paramter beeinflussen das Verhalten und Aussehen des Booking Buttons für Klassen:
| Attribut    | Beschreibung| 
| ------------- |:-------------:|
| appointment-id      | Die Id des Events/Klasse etc. |
| class-button-text  | Der Text im Booking Button z.b. "Anmelden" |
| background-color     | Hintergrundfarbe des Buttons  |
| color  | Textfarbe des Buttons.  |

Folgende Paramter beeinflussen das Verhalten und Aussehen des Booking Buttons für Flex-Time Kurse:
| Attribut    | Beschreibung| 
| ------------- |:-------------:|
| service-product-id    | Die Id des Services, ist zwingedn erforderlich wenn es sich um einen Flex-Time Button handelt. |
| consultant-id    | Die Id des Therapeuten, ist optional. Falls gesetzt, kann der Therapeut nicht mehr geändert werden. |

Beispiel Klasse:

``` html
<stamy-booking-button type="class" background-color="green" color="white" appointment-id="123456789" cart-url="'/shopping-cart'"></stamy-booking-button>
```

Beispiel Flex-Time:

``` html
<stamy-booking-button type="flex-time" service-product-id="123456789" consultant-id="abc" cart-url="'/shopping-cart'"></stamy-booking-button>
```

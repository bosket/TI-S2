# Opdrachten Classes C++[](title-id)

### Inhoud[](toc-id)
- [Opdrachten Classes C++](#opdrachten-classes-c)
    - [Inhoud](#inhoud)
    - [Opdracht OO1.51 SFML window](#opdracht-oo151-sfml-window)
  - [Opdracht OO1.52 Rechthoek](#opdracht-oo152-rechthoek)
  - [Tips](#tips)


*Deze opdracht kan nog veranderen!*
### Opdracht OO1.51 SFML window
- Bestudeer de [SFML graphics library](https://www.sfml-dev.org/). Voor het installeren zijn verschillende mogelijkheden maar onderstaande werkt op Windows, voor Visual Studio Code:

[Installeer SFML met de packetmanager](../../../inrichten-ontwikkelomgeving/sfml_installatie.md)
(dankzij Lia E.):


## Opdracht OO1.52 Rechthoek
- Bestudeer de [SFML shapes library](https://www.sfml-dev.org/tutorials/2.6/graphics-shape.php).

- Schrijf een programma dat een rechthoek in een window afbeeldt.

## Tips
Hieronder staat voorbeeldcode die misschien behulpzaam is.

```c++
/// @file  main.cpp - incomplete code 
/// exercise: draw a SFML rectangle
#include <SFML/Graphics.hpp>
#include <SFML/Window.hpp>
#include <iostream>

int main ()
{
    // the window in which we want to print the line
    sf::RenderWindow window (sf::VideoMode (800, 600), "My window", sf::Style::Default, sf::ContextSettings (0, 0, 2));

    // Todo: define a sfml rectangle, e.g. named rshape, located at (4, 2) with a size of 120x50
    // ... rshape ...;

    // run the program as long as the window is open
    while (window.isOpen ())
	{
	    // check all the window's events that were triggered since the last iteration of the loop
	    sf::Event event;
	    // window.display ();
	    while (window.pollEvent (event))
		{
		    // "close requested" event: we close the window
		    if (event.type == sf::Event::Closed)
			window.close ();
		}

	    // clear the window
	    window.clear ();
	    // Todo: draw the sfml rectangle - uncomment the next line
	    // window.draw (rshape);

	    window.display ();
	    // voorkom gebibber op het scherm
	    sf::sleep (sf::milliseconds (20));
	}
    return 0;
}
```
*main.cpp*
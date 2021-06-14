# 33164-Phototransistor GROVE

Phototransistor GROVE [33164](https://www.pierron.fr/phototransistor-grove.html)

<div style="text-align: justify">Module capteur de lumière compatible Grove utilisant un phototransistor pour détecter la présence de lumière. L'utilisation d'un phototransistor à la place d'une photorésistance permet d'obtenir un signal plus linéaire. La tension de sortie analogique évolue en fonction de l'intensité lumineuse mesurée. Ce module se raccorde sur une entrée analogique du Base Shield via un câble 4 conducteurs.</div>

Caractéristiques techniques :
- Alimentation : 3,3 à 5 V
- Phototransistor LS06-S

![L-33164](/img/L-33164.jpg)

# Usage :
Pour l’utilisation de ce module référez-vous aux indications présentes sur le circuit imprimé GROVE.

# Schémas :

![SCH-33164](/img/SCH-33164.jpg)
![BRD-33164](/img/BRD-33164.jpg)

# Complément sur la programmation :

La valeur du capteur de lumière ne reflète que la tendance approximative de l’intensité de la lumière, elle ne représente PAS le lumen exact.       

# RESSOURCES À TÉLÉCHARGER :

Ressource utilisation : [LM358](https://github.com/pierron-asco-celda/33164-Phototransistor_GROVE/blob/main/src/Datasheet_LM358.pdf)

Ressource utilisation : [LS06-S](https://github.com/pierron-asco-celda/33164-Phototransistor_GROVE/blob/main/src/Datasheet_LS06.pdf)

# Exemple :
### Arduino / C++
```cpp
/*
    ** Mesure luminosité en lux V1.1 & V1.2 module Grove **
       PIN A0 Module shield GROVE
       Moniteur série -> Baud rate 9600.
       La valeur du capteur de lumière ne reflète que la tendance approximative de l’intensité de la lumière, 
       elle ne représente PAS le lumen exact.
*/

void setup() {
  Serial.begin(9600);
}

void loop() {

  int value = analogRead(A0);
  Serial.print("Luminosité : ");
  Serial.print(value);
  Serial.println(" lux");
  delay(100);

}
```
## À propos :

PIERRON ASCO-CELDA (https://www.pierron.fr).

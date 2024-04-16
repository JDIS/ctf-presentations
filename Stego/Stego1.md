---
marp: true
theme: gaia
class: invert
---
<!-- footer: Frédéric Bilodeau -->

![bg right:25% fit](../Images/logo_jdis.png)

<style scoped>h1 {font-size: 300%;position:absolute; margin:25% 0;}</style>

# Stéganographie

---
<!-- paginate: true -->
<!-- header: Introduction -->
<!-- footer: "" -->
# Stéganographie
###### Caché à la vue de tous
<!-- ###### C'est Quoi ?  -->

Se distainge de la crypto par le fait qu'elle n'est pas encrypté, mais bien juste caché "hidden in plain sight"

Est souvent le cas quand la "track" contient des images

---
# Images

##### Bases
- Métadonnées
- Couleurs
- HEX   
- Pixels non affichés   <!-- https://cyberhacktics.com/hiding-information-by-changing-an-images-height/ -->
- Données style archive zip à l'interieur


--- 
# Outils de bases
- strings
- StringCheese
- binwalk / unblob
- stegHide
- exiftools
- outguess
- Oeil de lynx (code caché sur l'image de base)
- Présentation aperisolve  <!-- https://www.aperisolve.com/cheatsheet -->

---
<!-- header: Outils -->
# Strings

Permet de sortie les "strings" d'un fichier 
Très utile avec grep
Vient par défaut dans linux !

usage:
``` strings fichier ```


---
# StringCheese :watermelon:

> Un ptit coup dans stringcheese c'est pas fou - Fred

It works like a simple strings | grep command, but can detect many encodings (like base64, XOR, rot13) and works on file formats other than plaintext.

installation:  
https://github.com/MathisHammel/stringcheese

usage:
``` stringcheese --file photo.jpeg -v hf{ ```

---
# Binwalk

On peut cacher des archives style zip ou zlib dans une photo ou dans un fichier. Cet outil permet de les extraires

installation:
``` apt install binwalk```

usage:
``` binwalk -e photo.jpeg ```

---
# Unblob
Très similaire à binwalk, mais un peu plus simple, peut donner des résultats similaires, mais ça reste un autre outil utile

installation:
``` python3 -m pip install unblob ```

usage:
``` unblob photo.jpeg ```


---
# StegHide
Un autre outil qui permet de cacher des informations dans des images

installation:
``` apt install steghide ```

usage:
``` steghide extract -sf photo.jpeg ```

---
# Exiftools
Un tools qui permet de sortir les métadonnées d'un fichier

installation:
``` apt install exiftools ```

usage:
``` exiftools a.jpeg ```

---
# outguess
Un autre outil qui permet de cacher des informations dans des images

 
installation:
 ``` apt install outguess ```

usage:
``` outguess -k "my secret pass phrase" -r out.jpg message.txt ```



---
# :eyes:

- Code QR
- image en section
- mauvaise extension (.jpg .png)
- changements des couleurs
- abérations sur les images 

---
# Aperisolve
Un merveilleux site qui fait pas mal toutes les techniques des pages précédantes de façon automagique 

https://www.aperisolve.com/ :watermelon:

---
# PNG specific
Changer la hauteur ou la largeur dune image 
source :
https://cyberhacktics.com/hiding-information-by-changing-an-images-height/

--- 
<!-- header: Wild stuffs -->
# Ésoterie

- Piet Programming language ?


--- 
<!-- header: Exercices -->
# Exercices
Pico CTF:



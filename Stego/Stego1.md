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
- StringCheese
- binwalk / unblob
- stegHide
- Oeil de lynx (code caché sur l'image de base)
- Présentation aperisolve  <!-- https://www.aperisolve.com/cheatsheet -->

---
<!-- header: Outils -->
# StringCheese :watermelon:

> Un ptit coup dans stringcheese c'est jamais perdu  - Fred

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
Très similaire à binwalk, mais un peu plus simple, peut donner des résultats similaires, mais ça reste un autre tool d'utile 

installation:
``` python3 -m pip install unblob ```

usage:
``` unblob photo.jpeg ```


---
# StegHide

installation:
``` apt install steghide ```

usage:


---
:eyes:


---

# Aperisolve
Un merveilleux site qui fait pas mal toutes les techniques des pages précédantes de façon automagique 

https://www.aperisolve.com/ :watermelon:


La sheet cheat

---

# PNG specific

# JPEG specific

# BMP specific

# 
--- 
<!-- header: Wild stuffs -->
# Ésoterie

- Piet Programming language ?


--- 
<!-- header: Exercices -->
# Exercices
Pico CTF:



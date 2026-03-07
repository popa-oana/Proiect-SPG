# Interactive 3D World Simulation

O simulare interactivă a unui mediu 3D direct în browser, dezvoltată folosind biblioteca **Three.js**. Proiectul pune în practică concepte de generare procedurală a terenului, sisteme de iluminare dinamică, detectarea matematică a coliziunilor și implementarea unor comportamente autonome (AI) pentru diverse entități.

## Despre Proiect

Scopul acestui proiect a fost crearea unei lumi virtuale vii și interactive. Utilizatorul poate naviga liber printr-un peisaj montan detaliat, intersectat de un circuit stradal funcțional, controlând un personaj 3D. Accentul a fost pus pe aplicarea matematicii în generarea organică a reliefului și pe crearea unui ecosistem dinamic care include mașini aflate în mișcare, animale sălbatice și un companion virtual.

## Funcționalități Principale

* **Teren Generat Matematic:** Relieful și munții din fundal sunt generați folosind funcții matematice (combinații de sinus/cosinus și zgomot procedural) pentru a crea denivelări organice și o zonă plană de "blending" în apropierea drumului.
* **Sistem Avansat de Iluminare:** Implementarea unei lumini direcționale globale (Soarele) care aruncă umbre realiste, completată de stâlpi de iluminat stradal (`SpotLight`) cu propriile lor hărți de umbre independente.
* **Control și Navigare:** Jucătorul (modelat ca un pieton) se poate deplasa liber pe hartă folosind controale clasice (WASD), acompaniat de o mișcare a camerei de tip orbit (`OrbitControls`) și un efect subtil de "bobbing" la mers.
* **Sistem Custom de Coliziuni:** Un algoritm care verifică în timp real distanța dintre jucător și limitele hărții, unghiul pantelor, obiectele statice (copaci, pietre) și entitățile aflate în mișcare.
* **AI și Entități Autonome:**
  * Mașini NPC care navighează continuu pe un circuit definit printr-o curbă `CatmullRom`, evitând coliziunile între ele sau cu jucătorul.
  * Animale sălbatice (văcuțe) care rătăcesc pe hartă pe baza unor decizii randomizate și care ocolesc obstacolele.
* **Companion Virtual:** Un cățeluș inteligent care calculează constant distanța față de jucător, urmărindu-l automat când se îndepărtează și orientându-se spre el când stă pe loc.

## Tehnologii Utilizate

* **HTML5 & CSS3:** Pentru structura și stilizarea de bază a canvas-ului.
* **JavaScript (ES6+):** Logica aplicației, gestionarea stărilor și matematica vectorială.
* **Three.js:** Motorul principal de randare 3D, WebGL, lumini, materiale și geometrii.

## Controale Jucător

* **W, A, S, D / Săgeți:** Deplasarea pietonului pe hartă.
* **Click Stânga (Hold + Drag):** Rotirea camerei în jurul personajului.
* **Click Dreapta (Hold + Drag):** Panoramarea camerei.
* **Scroll Mouse:** Zoom in / Zoom out.

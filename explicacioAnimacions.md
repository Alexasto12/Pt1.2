<!-- filepath: explicacioAnimacions.md -->
# Explicació de les Animacions Implementades

Aquest document descriu totes les animacions CSS implementades a la pàgina web sobre exploració espacial.

## 1. Animacions de Text i Color

### Títol Animat (`colorChange`)
- **Element**: Títol "COSMOS" al header
- **Classe CSS**: `.animated-title`
- **Descripció**: El text canvia de color suaument, passant per diferents tonalitats.
- **Com funciona**: Utilitza `@keyframes colorChange` per a transicionar entre diversos colors en un cicle infinit de 5 segons.
- **Efecte visual**: El títol comença en blanc, després canvia a blau clar, lila, rosa, i torna a blanc.

```css
.animated-title {
    animation: colorChange 5s infinite;
}

@keyframes colorChange {
    0% { color: #ffffff; }
    25% { color: #00b4d8; }
    50% { color: #5e60ce; }
    75% { color: #ff5e78; }
    100% { color: #ffffff; }
}
```
### Desplaçament del Borde (`borderSlide`)
- **Element**: Footer
- **Classe CSS**: `.footer-dark::before`
- **Descripció**: El borde superior del footer es desplaça amb un gradient de colors.
- **Com funciona**: Utilitza `@keyframes borderSlide` per a desplaçar el gradient de colors en un cicle infinit de 4 segons.
- **Efecte visual**: El borde superior del footer sembla moure's amb un gradient de colors.

```css
.footer-dark::before {
    animation: borderSlide 4s linear infinite;
}

@keyframes borderSlide {
    0% { background-position: 0% 0; }
    100% { background-position: 100% 0; }
}
```

## 2. Animacions de Planetes i Estrelles

### Planeta Flotant (`float`)
- **Element**: Planeta flotant a la secció de galeria
- **Classe CSS**: `.floating-planet`
- **Descripció**: El planeta es mou amunt i avall amb una rotació lleugera.
- **Com funciona**: Utilitza `@keyframes float` per a moure el planeta verticalment i rotar-lo lleugerament en un cicle infinit de 8 segons.
- **Efecte visual**: El planeta sembla flotar en l'espai amb un moviment suau.

```css
.floating-planet {
    animation: float 8s ease-in-out infinite;
}

@keyframes float {
    0% { transform: translateY(0) rotate(0deg); }
    50% { transform: translateY(-20px) rotate(10deg); }
    100% { transform: translateY(0) rotate(0deg); }
}
```

### Estrella Palpitant (`pulse`)
- **Element**: Estrella palpitant a la secció de galeria
- **Classe CSS**: `.pulsing-star`
- **Descripció**: L'estrella augmenta i disminueix de mida, simulant un efecte de palpitació.
- **Com funciona**: Utilitza `@keyframes pulse` per a escalar l'estrella i ajustar la seva ombra en un cicle infinit de 3 segons.
- **Efecte visual**: L'estrella sembla palpitant amb una llum brillant.

```css
.pulsing-star {
    animation: pulse 3s infinite;
}

@keyframes pulse {
    0% { transform: scale(1); box-shadow: 0 0 10px rgba(255, 255, 255, 0.7); }
    50% { transform: scale(1.5); box-shadow: 0 0 20px rgba(255, 255, 255, 0.9), 0 0 40px rgba(255, 255, 255, 0.5); }
    100% { transform: scale(1); box-shadow: 0 0 10px rgba(255, 255, 255, 0.7); }
}
```

### Fade In (`fadeIn`)
- **Element**: Contenidor de la galeria
- **Classe CSS**: `.gallery-container`
- **Descripció**: La galeria apareix gradualment.
- **Com funciona**: Utilitza `@keyframes fadeIn` per a augmentar l'opacitat de 0 a 1 en 1.5 segons.
- **Efecte visual**: La galeria es fa visible de manera suau.

```css
.gallery-container {
    animation: fadeIn 1.5s forwards;
}

@keyframes fadeIn {
    from { opacity: 0; }
    to { opacity: 1; }
}
```

### Flotació a la Galeria (`floatGallery`)
- **Element**: Planeta flotant dins d'un element de la galeria
- **Classe CSS**: `.floating-planet`
- **Descripció**: El planeta es mou amunt i avall amb una rotació lleugera dins de la galeria.
- **Com funciona**: Utilitza `@keyframes floatGallery` per a moure el planeta verticalment i rotar-lo lleugerament en un cicle infinit de 6 segons.
- **Efecte visual**: El planeta sembla flotar dins de la galeria amb un moviment suau.

```css
.floating-planet {
    animation: floatGallery 6s ease-in-out infinite;
}

@keyframes floatGallery {
    0% { transform: translateY(0) rotate(0deg); }
    50% { transform: translateY(-15px) rotate(5deg); }
    100% { transform: translateY(0) rotate(0deg); }
}
```

### Rotació del Borde (`borderRotate`)
- **Element**: Element de la galeria
- **Classe CSS**: `.gallery-item::after`
- **Descripció**: El borde de l'element de la galeria canvia de color i rota.
- **Com funciona**: Utilitza `@keyframes borderRotate` per a canviar el color del borde en un cicle infinit de 4 segons.
- **Efecte visual**: El borde de l'element de la galeria sembla rotar amb colors canviants.

```css
.gallery-item::after {
    animation: borderRotate 4s linear infinite;
}

@keyframes borderRotate {
    0% { border-color: #ff5e78; }
    25% { border-color: #5e60ce; }
    50% { border-color: #00b4d8; }
    75% { border-color: #4a6fa5; }
    100% { border-color: #ff5e78; }
}
```

### Zoom In/Out (`zoomInOut`)
- **Element**: Imatges dels planetes
- **Classe CSS**: `.uranus-img`, `.neptune-img`, etc.
- **Descripció**: Les imatges dels planetes fan zoom in i out.
- **Com funciona**: Utilitza `@keyframes zoomInOut` per a canviar la mida de fons de les imatges en un cicle infinit.
- **Efecte visual**: Les imatges dels planetes semblen fer zoom in i out de manera suau.

```css
.uranus-img, .neptune-img, .mercury-img, .venus-img, .earth-img, .mars-img, .jupiter-img {
    animation: zoomInOut 37s infinite alternate;
}

@keyframes zoomInOut {
    0% { background-size: 100%; }
    50% { background-size: 120%; }
    100% { background-size: 100%; }
}
```


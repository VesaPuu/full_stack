kayttaja->selain:
note left of selain
kayttaja kirjoittaa osoiteriville
https://fullstack-exampleapp.herokuapp.com/spa
end note
selain->palvelin: GET https://fullstack-exampleapp.herokuapp.com/spa
palvelin->selain: status 200, sivun HTML-koodi

selain->palvelin: GET https://fullstack-exampleapp.herokuapp.com/main.css
palvelin->selain: status 200, CSS-tiedosto

selain->palvelin: GET https://fullstack-exampleapp.herokuapp.com/spa.js
palvelin->selain: status 200, javascript-tiedosto

selain->palvelin: GET https://fullstack-exampleapp.herokuapp.com/data.json
palvelin->selain: status 200, JSON-data

note left of selain
 selain näyttää palvelimen palauttaman HTML:n,
 suorittaa spa.js-tiedostossa olevan javascript-koodin,
 joka lataa muistiinpanot JSON-muodossa, ja
 muodostaa niistä selaimeen luettelon
end note

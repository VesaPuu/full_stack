kayttaja->selain:
note left of selain
kayttaja kirjoittaa lomakkeelle uuden muistiinpanon
ja painaa Tallenna
end note

selain->palvelin: POST https://fullstack-exampleapp.herokuapp.com/new_note

note left of palvelin
palvelin luo uutta muistiinpanoa vastaavan olion ja laittaa sen muistiinpanot sisältävään taulukkoon 
end note

palvelin->selain: status 302, uudelleenohjauspyyntö

selain->palvelin: GET https://fullstack-exampleapp.herokuapp.com/notes
palvelin->selain: status 200, sivun HTML-koodi

selain->palvelin: GET https://fullstack-exampleapp.herokuapp.com/main.css
palvelin->selain: status 200, CSS-tiedosto

selain->palvelin: GET https://fullstack-exampleapp.herokuapp.com/main.js
palvelin->selain: status 200, javascript-tiedosto

selain->palvelin: GET https://fullstack-exampleapp.herokuapp.com/data.json
palvelin->selain: status 200, JSON-data



note left of selain
 selain näyttää palvelimen palauttaman HTML:n,
 suorittaa main.js-tiedostossa olevan javascript-koodin,
 joka lataa muistiinpanot JSON-muodossa, ja
 muodostaa niistä selaimeen luettelon
end note

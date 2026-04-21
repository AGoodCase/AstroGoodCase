Teknisk dokumentation – [A good case]
Om projektet
Dette projekt er lavet som en del af Tema 9. Vi har lavet et dynamisk website med HTML, CSS og JavaScript, hvor indholdet bliver hentet fra et Rest API.


Sitet består af flere sider, hvor brugeren kan:


se en liste med indhold
klikke sig videre til en detaljeside
bruge filtrering
Links
GitHub repository: [https://github.com/AGoodCase/AstroGoodCase.git]
GitHub Pages: []
Figma: [https://www.figma.com/design/6Dr8HhVUwTCzSOEOGZluZr/guRppe06?node-id=1041-3129&t=deCiEjLXB6iVQx4C-1]
Trello: [https://trello<.com/b/kg3QdAOh/a-good-case ]


Projektet er opdelt i HTML, CSS og JavaScript-filer.


project/ASTROGOODCASE
├── .astro
├── .vscode
├── node_modules
├── public
├── src
│   └── assets
│       └──Components
          Button.astro
          Footer.astro
          Hero.astro
          Navigation.astro
          Pcard.astro
          Sale.astro
│   └── Layouts
       Layout.astro
│   └── Pages
│       └──About.astro
          contact.astro
          index.astro
          productlist.astro
├── Styles
│   └── global.css
├── .gitignore
├──package-lock.json
├──package.json
└── README.md
├──tsconfig.json


Filbeskrivelser
"public" = favicon
"assets" = billeder og svg
"components" = Komponenter
"layouts" = Hero, nav og footer (globalt)
"pages" = html sider
"Styles" = global css


Hvordan fungere koden?
index er vores forside der tager en videre igennem sitet (startpunktet)


Vi har en Productlist der viser hvilke produkter der er, som bliver hentet fra en api der viser priser samt hjælper med sortering.


About siden er bare information omkring brandet.


id.astro siden er den der henter information fra api til productdetails siden som viser mere detaileret information om produktet.


Flow:


Siden loader
JavaScript kører
Data hentes fra Rest API
Data bliver gennemgået med loop
HTML bliver indsat i DOM'en
Brugeren kan klikke vores undersider og så looper den bare


Id.astro siden læser urlen og henter så det rigtige produkt fra rest api'en som gør at vi har den samme html side til alle vores produkter.


Vi har lavet en pcard component som ser sådan her ud


<a
 href=`details/${product.handle}`
 class="Pcard"
 data-type={product.type}
 data-price={product.price}
>
 <article>
   <img src={product.img} alt="productimage" />
   <h3>{product.name}</h3>
   <h4>{product.percent}%</h4>
   <p class="price">kr. {product.price},-</p>
   <p class="market_price">kr. {product.market_price},-</p>
 </article>
</a>


som så gør at vi bare kan sætte dette ind - <section class="Plist">
   {data.map((product) => <Pcard {product} />)}
 </section>
Hvor enden der skal være et produkt.


Felter vi bruger
product.type = type af øl
product.price = pris på øl
Product.name = navn på øl
product.percent = alkohol% på øl
price = pris
market_price = markedspris


Git og branches


Vi har brugt GitHub til at samarbejde om projektet.


Vi har arbejdet med branches, så vi ikke sad og ændrede i det samme på samme tid.


Vi navngav branchene med feature først og navnet på den, der lavede branchen til sidst.


Workflow


1. Uddele opgaver
2. Lave branch med opgave og navn
3. kode det
4. sikre sig at alle er klar
5. pushe og merge sammen, så vi sikre os at der ikke er nogle konflikter i koden.


Udfordringer undervejs


1. Vi havde enormt mange problemer med rest api'en og hvordan vi skulle inkorporere den i vores kode
2. Vi Havde virkelig svært ved at få alle vores fede ideer i figma, til at faktisk blive kodet i vscode.




Mulige forbedringer


1.






Gruppemedlemmer


Anton Jepsen
Tobias Vincents
Ditte Helene andersen
Eva Roed Schack







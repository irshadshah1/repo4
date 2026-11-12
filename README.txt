AURORA GRAND RESORT — LARGE STATIC WEBSITE DEMO

PAGES
- index.html: Home, booking enquiry, brand introduction, featured sections, newsletter
- rooms.html: Deluxe Room, Garden Suite, Presidential Villa
- dining.html: The Verandah, Ember & Oak, The Atrium
- experiences.html: Spa, pool, local explorations, celebrations
- gallery.html: Image gallery with lightbox
- contact.html: Contact details and enquiry form
- assets/css/style.css: Responsive visual styling
- assets/js/main.js: Mobile navigation, date validation, demo forms, gallery lightbox

RUN
1. Extract the ZIP.
2. Open index.html in a browser.
3. Optional local server from this directory:
   python3 -m http.server 8080
   Browse http://localhost:8080

DOCKERFILE (place in this folder)
FROM httpd:2.4
COPY . /usr/local/apache2/htdocs/
EXPOSE 80
CMD ["httpd-foreground"]

BUILD AND RUN
docker build -t aurora-resort:1 .
docker run -d --name aurora-resort -p 8080:80 aurora-resort:1

IMPORTANT
This is a static front-end portfolio/DevOps POC website. Forms are demo interactions only.
There is no real booking, payment, email, login, or database backend. Images and fonts load
from external Unsplash/Google Fonts services, so internet access is needed for those assets.
All resort details and contact information are fictional sample content.

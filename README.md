# How to add and display a map on your Ionic app

You should already have an installed Ionic app, we will not go through the installation process of ionic.


### Step 1
Head over to google maps javascript API
Select and get a API KEY copy it and save in a file
At: https://developers.google.com/maps/documentation/javascript/get-api-key

### Step 2

Go to `index.html` and add
``<script src="https://maps.googleapis.com/maps/api/js?key=YOUR-API-KEY" async defer></script>``

### Step 3
Go to `home.html` and remove the content between `<ion-content>` and ad `<div #map id="map"></div>
`

### Step 4
Head over to your `home.ts` adn update your `import { Component, } from '@angular/core';` to `import { Component, ViewChild, ElementRef } from '@angular/core';`

 We then need to capture the reference by adding
 `@ViewChild('map') mapRef: ElementRef;` to the `export class HomePage` above the `constructor`


To import component add ViewChild, ElementRef
Add to the export class HomePage
@ViewChild(‘map’) mapRef: ElementRef;

Add ionViewDidLoad() {
	console.log(this.mapRef)

Add showMap() {
Const location = new google.maps.LatLang(your lat, your lang):
}

Add  declare var google: any: above the @component

# How to add and display a map on your Ionic app

You should already have an installed Ionic app, we will not go through the installation process of ionic.


### Step 1
Head over to google maps javascript API
Select and get a API KEY copy it and save in a file
At:https://developers.google.com/maps/documentation/javascript/get-api-key

### Step 2

Go to your app

Index.html
	<script src=”https://maps.googleapis.com/maps/apis/js?key=AIzaSyADuzuOHgmrCJlTlUxIyb_qagTM4MnoBSI async defer“></script>

Home.html

Remove content between ion content
And add
	<div #map id= “map”></div>

Home.ts

To import component add ViewChild, ElementRef
Add to the export class HomePage
@ViewChild(‘map’) mapRef: ElementRef;

Add ionViewDidLoad() {
	console.log(this.mapRef)

Add showMap() {
Const location = new google.maps.LatLang(your lat, your lang):
}

Add  declare var google: any: above the @component

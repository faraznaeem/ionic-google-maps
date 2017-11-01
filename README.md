Head over to google maps javascript API
Select and get a API KEY copy it and save in a file
We are not using the cordova plugin

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

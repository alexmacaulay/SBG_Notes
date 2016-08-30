# MongoDB Brewdog Lab

So now you've seen how we can interact with MongoDB NoSQL databases, it's time to stretch ourselves and have a bit of a pratice. 

### Setup
Run the following bash script from your command line to import the data from Brewdog's Punk API into a database called `brewdog` on your local machine:

```bash
touch punkapi.json && curl https://punkapi.com/api/v1/beers -u c4ae17fcb0f44fccb93f5c8494732b72 >> punkapi.json && mongoimport --db brewdog --collection beers --jsonArray --file ./punkapi.json && rm ./punkapi.json
```
Inside the brewdog database you'll find a collection called beers, containing loads of data about the beers brewdog provide for us.

### Tasks

Find a Mongo command that will do each of the following tasks. Google and the MongoDB docs are your friends: 

1. Returns all the beers in the database
	* db.beers.find()
2. Returns how many beers are in the database as a number
	* db.beers.count()
3. Returns the names and alcohol contents of all the beers in the database 
	* db.beers.find({}, {name: true, ingredients: true}) 
4. Adds a custom beer with your chosen values
	* db.beers.insert({
... "id" : 999,
... "name" : "Alex Brew",
... "tagline" : "Beats a Cup of Joe.",
... "first_brewed" : "November 2008",
... "description" : "This beer was released as both as \"Danish Beerhouse Coffee Imperial Stout\" and \"BrewDog Coffee Imperial Stout\". Deep, dark, roasted flavours make this a perfect Sunday brunch beer.",
... "abv" : 9,
... "ibu" : 65,
... "target_fg" : 1019,
... "target_og" : 1080,
... "ebc" : 97,
... "srm" : 49,
... "ph" : 4.4,
... "attenuation_level" : 76,
... "volume" : {
... "value" : 20,
... "unit" : "liters"
... },
... "boil_volume" : {
... "value" : 25,
... "unit" : "liters"
... },
... "method" : {
... "mash_temp" : [
... {
... "temp" : {
... "value" : 64,
... "unit" : "celsius"
... },
... "duration" : 90
... }
... ],
... "fermentation" : {
... "temp" : {
... "value" : 19,
... "unit" : "celsius"
... }
... },
... "twist" : "Coffee added after boil. Aged on French oak chips., Dark muscovado sugar: 312.5g for 20mins"
... },
... "ingredients" : {
... "malt" : [
... {
... "name" : "Extra Pale",
... "amount" : {
... "value" : 7.5,
... "unit" : "kilograms"
... }
... },
... {
... "name" : "Dark Crystal",
... "amount" : {
... "value" : 0.63,
... "unit" : "kilograms"
... }
... },
... {
... "name" : "Chocolate",
... "amount" : {
... "value" : 0.31,
... "unit" : "kilograms"
... }
... },
... {
... "name" : "Roast Barley",
... "amount" : {
... "value" : 0.31,
... "unit" : "kilograms"
... }
... }
... ],
... "hops" : [
... {
... "name" : "Chinook",
... "amount" : {
... "value" : 25,
... "unit" : "grams"
... },
... "add" : "start",
... "attribute" : "bitter"
... },
... {
... "name" : "Galena",
... "amount" : {
... "value" : 25,
... "unit" : "grams"
... },
... "add" : "start",
... "attribute" : "bitter"
... },
... {
... "name" : "Galena",
... "amount" : {
... "value" : 25,
... "unit" : "grams"
... },
... "add" : "end",
... "attribute" : "flavour"
... },
... {
... "name" : "First Gold",
... "amount" : {
... "value" : 25,
... "unit" : "grams"
... },
... "add" : "end",
... "attribute" : "flavour"
... },
... {
... "name" : "Coffee",
... "amount" : {
... "value" : 9.4,
... "unit" : "grams"
... },
... "add" : "end",
... "attribute" : "flavour"
... },
... {
... "name" : "Coffee",
... "amount" : {
... "value" : 9.4,
... "unit" : "grams"
... },
... "add" : "dry hop",
... "attribute" : "aroma"
... }
... ],
... "yeast" : "Wyeast 1056 - American Ale™"
... },
... "food_pairing" : [
... "Gooey chocolate brownies",
... "Chicken fried steak with cheesy mash",
... "Spicy chicken empanadas"
... ],
... "brewers_tips" : "Grind the coffee as if making an espresso to really get the most out of it.",
... "contributed_by" : "Sam Mason <samjbmason>"
... }
... )
5. Returns the 10 strongest beers
	* db.beers.find({},{name:true}).sort({abv:-1}).limit(10)
6. Returns the three weakest beers
	* db.beers.find({},{name:true}).sort({abv:1}).limit(3)
7. Returns the beer with the highest pH value
	* db.beers.find({},{name:true}).sort({pH:-1}).limit(1)
8. Returns the beer with the highest number of hop varieties in its recipe
	* db.beers.aggregate([{$project:{ hop_count: { $size: "$ingredients.hops" } }},{$sort:{hop_count:-1}},{ $limit : 1 }])
9. Returns the beer that pairs best with Haggis Spring Rolls
	* db.beers.find({food_pairing:"Haggis spring rolls"}).pretty()
10. Finds your favourite beer and adds a "favourites" field to it with your name
	* db.beers.update({name:'Storm'},{$setOnInsert:{favourites:'Alex'}});
11. Changes the "contributed_by" field for all the beers to your name 
	* db.beers.updateMany( {}, {$set:{contributed_by: "Alex Macaulay"}} )
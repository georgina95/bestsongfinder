# bestsongfinder
Korszerű webfejlesztés beadandó

Osztályok

Store:
		albums:	Array<Album>
	
	o	Constructor():	Store
	
	o	addAlbum(Obj)
	
	o	formatJSON(JsonObj inputAlbum):	Album
	
	o	checkInput(JsonObj inputAlbum):	?Error
	
	o	getAll()	Array<Album>
	
	o	getBestOf(Int id, Int number):	String
	
	o	getAlbum(Int id):	Album

Album:
		id:	ID
		tracks:	ARRAY<Track>
		bestSongFinder:	BestSongFinder
	o	Constructor(Store store, Obj albumData):	Album
	o	getBests(Int number):	Array<Track>
	
Track:
		id:	ID
		title:	String
		frequency:	Int
		zipfIndex:	Int
	o	Constructor(Album album, String title, Int frequency):	Track
	o	countZipfIndex( )

BestSongsFinder:
		album:	Album
	o	Constructor(Album album):	BestSongFinder
	o	sortByZipf(Album album):	Album
	o	findBests(Int number):	Array<Track>

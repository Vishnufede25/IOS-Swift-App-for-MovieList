# IOS-Swift-App-for-MovieList
TMDB account is used to get the Movie details and display them based on the various aspects.

This API generates the movie list for various categories like recently added, now playing, top rated or most popular. 
data from this API is fetched in JSON format and displayed in table view initially.
Further a detailed view is generated for each movie which elaborates on its title, description, rating and posters.

Master view must be tableview: 
  Custom cell
  Movie list from TMDB server through Json downloading
  Small image of poster, title are shown
  Image downloaded from the poster link
  Can select a movie by tapping a row, then load detail view
  Can delete a movie with swiping action

Detail view:
  Customized detail view
  Title, rating, descriptionare all added to the view
  Movie detail downloaded from TMDB with id of Movie
  Poster/Backdrop images are shown within a collection view and make swiping action
  Images are downloaded from server (No local Images)
  poster/backdrop images are used to manipulate >= 4 collectionview items
  Model defined for fetching Movie Json data
  Movie list/Movie detail - Decodable (No need to parse JSON data)
  
Database:
  Firebase for login authentication/reviews for movies
  User credentials/profiles created/saved in Firebase
  Users' reviews saved in Firebase and fetched into master/detail screens
  Login Screen for login or regster / Profile Editing Screen
      if successfully logged in, displays the list of movies fetched from API
      if successfully registered, displays profile screen to add profile image and other information
      profile image must be selected and uploaded intofirebase
      if not selected, default image for profile image is used
      Username, favorite movie and genre are stored as User Information
    
Updates to existing Views:
  Master View (TableView)
      poster icon, title, # of reviews for each movie if they exist
  Detail View (either TableView or CollectionView)
      Multiple sections; for example, first section is for movie information from API and second section is for reviews from                    Firebase
  Reviews can be written by multiple logged users
      user name, review written by the user, # of like or dislike tapped by other users
      review cell designed with username, review text,like/dislike buttons and number for each,  review can be edited/deleted only by         author
           
  Database-realtime update
  Own review data model
  Storage to save profile images
  
With all the above elements the final updates are:
  TabBar: with 4 menus: User favorites, Popular, Upcoming and Now Playing movie list.
  
  If item is selected, detail view of the selected movie must be displayed with reviews
  favorite button added into movie item cell of all movie lists
  If favorite button is selected, the movie will be added into the user's favorite list both in the firebase and in the favorite list of    the app
  If deselected, the movie must be removed from the user's favorite list in both firebase and app
  realtime operations must be demoed in the video
  

     

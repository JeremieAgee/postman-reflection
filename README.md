### Objective
Use Postman Api get request on pokemon api.
https://pokeapi.co/api/v2/pokemon/

The first Pokemon i chose was Ivysaur. I used the https://pokeapi.co/api/v2/pokemon/2/ in the url to get ivysaur. The information it produces shows you the abilities in an array,
base experience, forms, game_indices, height, held_items, id,
moves  of the pokemon. It also gives the height, id and the encounter areas.
<img src="img/Screenshot 2024-02-05 201921.png">

The next pokemon I searched for was squirtle. url. https://pokeapi.co/api/v2/pokemon/7/ 
original game index of 177 and it was in pokemon red, blue, yellow.
<img src="img/squirtle.png">

Lastly I chose pidgeotto. has a base experience of 122 and an original game index off 150 in red, blue and yellow.
if i wanted to access the game_indices i would use a data.game_indices[0].game_index or data.game_indices[0].version.name either use should get the desired data from information
<img src="img/pidgeotto.png">
 
### Postman Github api
Today I created a github environment in postman to store our bearer token in private.
<img src="img/githubEnv.png">
Then I created a github collection and set the auth to bearer and the value to the variable we stored(pat-github).
<img src="img/setAuth.png">
Next I set the variables for the Collection I created 2 of them one to store the base url and another to store the rest of what you need to create a repo.
<img src="img/collectionVars.png">
After that we call the first get request of the {baseUrl}user. This gets all my account info and is displayed in json format.
<img src="img/baseUser.png"> 
Lastly I created a repo using a post request in postman. I took the two variable baseurl and createRepo above and then we have to add a body in raw/json format.
<img src="img/createRepo.png">

### Day 5
Today I downloaded the Thunder Client Extension to VSCode. The first Thing I did was create an environment with the name Github and set a variable for my bearer token and set it to secret. 
<img src="img/thunderEnv.png">
 
I then created an collection with the name GitHub and set the auth to bearer
and the value to my pat-github from before.
<img src="img/collection.png">
 I also set a base url for github which makes the creation of request much easier and looks good.
 <img src="img/baseUrl.png"> Noted you cant set variables in collections like you can on postman but you can make local environments and global ones as well to set any variables you might need. I went ahead and created a create variable thats used for creating new repos.
<img src="img/variables.png">
I then went and created a get request for user info which is my basic info. Only needed to add user to the request since i set the base Url.
<img src="img/user.png">

After that i created a folder called repos and added a post request with the variable I had set earlier called create.
<img src="img/create.png">
As you can see i got a status of 201 created and shows all the information on the creation of the new repo.
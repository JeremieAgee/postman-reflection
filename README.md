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
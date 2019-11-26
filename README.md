# Pursuit-Core-Introduction-To-Networking-and-APIs-Lab

# Part One

API Scavenger Hunt!

For each of the questions below, identify a website and search query that will give you the appropriate JSON.  Paste the url and a snippet of the json below.  Googling the category + API will generally take you to where you need.  Ex. https://lmgtfy.com/?q=cat+fact+api

1. A random cat fact
2. A list of 150 random users in English.
3. All the repos on Github with Pursuit their name
4. All the JavaScript repos on Github with Pursuit in their name
5. All the Swift repos on Github with Pursuit in their name
6. A list of all Pokemon
7. A list of all items in Fortnite
8. A list of all Game of Thrones Episodes.
9. A list of all songs with "Love" in the title.
10. All information about Petyr Baelish from the Game of Thrones books
11. All the movies Leonardo Dicaprio has acted in

Answers:

1. website: https://documenter.getpostman.com/view/1946054/S11HvKSz?version=latest

query:
https://catfact.ninja/fact?max_length=140

snippet:


var settings = {
  "url": "https://catfact.ninja/fact?max_length=140",
  "method": "GET",
  "timeout": 0,
  "headers": {
    "Accept": "application/json"
  },
};

$.ajax(settings).done(function (response) {
  console.log(response);
});


2. website:
https://randomuser.me

query: 
$.ajax({
  url: 'https://randomuser.me/api/',
  dataType: 'json',
  success: function(data) {
    console.log(data);
  }
});
snippet:
{
  "results": [
    {
      "gender": "male",
      "name": {
        "title": "mr",
        "first": "brad",
        "last": "gibson"
      },
      "location": {
        "street": "9278 new road",
        "city": "kilcoole",
        "state": "waterford",
        "postcode": "93027",
        "coordinates": {
          "latitude": "20.9267",
          "longitude": "-7.9310"
        },
        "timezone": {
          "offset": "-3:30",
          "description": "Newfoundland"
        }
      },
      "email": "brad.gibson@example.com",
      "login": {
        "uuid": "155e77ee-ba6d-486f-95ce-0e0c0fb4b919",
        "username": "silverswan131",
        "password": "firewall",
        "salt": "TQA1Gz7x",
        "md5": "dc523cb313b63dfe5be2140b0c05b3bc",
        "sha1": "7a4aa07d1bedcc6bcf4b7f8856643492c191540d",
        "sha256": "74364e96174afa7d17ee52dd2c9c7a4651fe1254f471a78bda0190135dcd3480"
      },
      "dob": {
        "date": "1993-07-20T09:44:18.674Z",
        "age": 26
      },
      "registered": {
        "date": "2002-05-21T10:59:49.966Z",
        "age": 17
      },
      "phone": "011-962-7516",
      "cell": "081-454-0666",
      "id": {
        "name": "PPS",
        "value": "0390511T"
      },
      "picture": {
        "large": "https://randomuser.me/api/portraits/men/75.jpg",
        "medium": "https://randomuser.me/api/portraits/med/men/75.jpg",
        "thumbnail": "https://randomuser.me/api/portraits/thumb/men/75.jpg"
      },
      "nat": "IE"
    }
  ],
  "info": {
    "seed": "fea8be3e64777240",
    "results": 1,
    "page": 1,
    "version": "1.3"
  }
}

3. https://developer.github.com/v3/search/ - code snipped
{
  "total_count": 40,
  "incomplete_results": false,
  "items": [
    {
      "id": 3081286,
      "node_id": "MDEwOlJlcG9zaXRvcnkzMDgxMjg2",
      "name": "Tetris",
      "full_name": "dtrupenn/Tetris",
      "owner": {
        "login": "dtrupenn",
        "id": 872147,
        "node_id": "MDQ6VXNlcjg3MjE0Nw==",
        "avatar_url": "https://secure.gravatar.com/avatar/e7956084e75f239de85d3a31bc172ace?d=https://a248.e.akamai.net/assets.github.com%2Fimages%2Fgravatars%2Fgravatar-user-420.png",
        "gravatar_id": "",
        "url": "https://api.github.com/users/dtrupenn",
        "received_events_url": "https://api.github.com/users/dtrupenn/received_events",
        "type": "User"
      },
      "

4. website:
https://developer.github.com/v3/repos/#list-languages

query:GET /repos/:owner/:repo/languages


snippet: 

{
  "C": 78769,
  "Python": 7769
}
      
5. website:
https://developer.github.com/v3/repos/#list-languages

query:GET /repos/:owner/:repo/languages

snippet:
{
  "C": 78769,
  "Python": 7769
}

6. website:
https://pokeapi.co 

query:
https://pokeapi.co/api/v2/pokemon/1/

snippet:
{
"abilities": [
  {
    "ability": {
      "name": "chlorophyll",
      "url": "https://pokeapi.co/api/v2/ability/34/"
    },
    "is_hidden": true,
    "slot": 3
  },
  {
    "ability": {
      "name": "overgrow",
      "url": "https://pokeapi.co/api/v2/ability/65/"
    },
    "is_hidden": false,
    "slot": 1
  }
],
"base_experience": 64,
"forms": [
  {
    "name": "bulbasaur",
    "url": "https://pokeapi.co/api/v2/pokemon-form/1/"
  }
],
"game_indices": [
  {
    "game_index": 1,
    "version": {
      "name": "white-2",
      "url": "https://pokeapi.co/api/v2/version/22/"
    }
  },
  {
    "game_index": 1,
    "version": {
      "name": "black-2",
      "url": "https://pokeapi.co/api/v2/version/21/"
    }
  },
  {
    "game_index": 1,
    "version"
    
7.  website: https://docs.fortniteapi.com/?version=latest

query: https://fortnite-api.theapinetwork.com/items/list

snippet: 
var settings = {
  "url": "https://fortnite-api.theapinetwork.com/items/list",
  "method": "GET",
  "timeout": 0,
  "headers": {
    "Authorization": "{{authorization}}"
  },
};

$.ajax(settings).done(function (response) {
  console.log(response);
});
# Part Two

Status Code Scavenger Hunt!

Use Postman to find each of the following HTTP codes:


1. 200
1. 301
1. 400
1. 401
1. 403
1. 404
1. 418
1. 500


For each of the questions below, write:

1. The website which generated the HTTP status code
2. A description of what the status code means
3. If an app you were writing encountered this status code, what would you do (if anything) to resolve any issues?


For reference, see:

https://en.wikipedia.org/wiki/List_of_HTTP_status_codes (Links to an external site.)
https://http.cat




Welcome to the one and only KB friend finder, guarenteed to get you a friend that you'll enjoy!

## Live Link
 -https://kb-friend-finder.herokuapp.com/survey

## link to Video of demonstration
https://drive.google.com/file/d/1Cc0XMNBtorqlQmgSEh4BxMsGOFVR4jSE/view

### Requirements
- Modularity in the form of separate files for server logic, storing of friends, views, and routing
- 10-question survey to assess uniqueness of users
- Use `express`, `body-parser`, and `path` npm packages in the `server.js` file
- Separate JavaScript files for routing (`htmlRoutes.js` and `apiRoutes.js`)
- Appropriate GET and POST routes for serving HTML pages and API calls
- Separate file for storing friends (`friends.js`)
- Calculate best match for user once survey is completed and return that match to the user

## Technologies Used
- JavaScript
- jQuery
- node.js
- Express.js
- HTML
- Bootstrap

## Code Explanation
- Our `server.js` file sets up the Express server, specifying our port number, the npm packages that need to be loaded, and also the routes, which we have externalized
- There are 2 separate HTML files (`home.html` and `survey.html`) that serve as the front-end portion of our code; they determine what the user sees (the homepage and the survey, which will also show the resulting best match)
- Our 2 routing files (`htmlRoutes.js` and `apiRoutes.js`) determine the back-end logic (based on the request being made, the response that gets sent to the browser); the HTML routes display the survey and the homepage based on the URL that is accessed, and the API routes send back existing content in our server-side data or add new friends
- Best match is calculated by finding the friend with the minimal difference in scores and then sending that friend to the browser as a JSON object
- A modal is then toggled, displaying the the best match to the person who just took the survey
- In essense, this will also be a form of notes that you may later reference weeks later
- Friends are stored as such:

```js
{
	name: "Matthew",
        photo: "https://cdn.pixabay.com/photo/2018/05/26/13/04/robot-3431313_1280.png",
        scores: [
            "5",
            "4",
            "3",
            "3",
            "1",
            "2",
            "1",
            "4",
            "5",
            "2"
        ]
}

# Brewery-Rating

This is a Yelp-like website that publishes user-generated ratings and reviews for breweries. We want brewery-lovers to be well-informed about famous breweries and freely interact with users of similar preferences on breweries.

## Building & Running

We use the NPM build system, React.js for the front-end website, Node.js for the server side, and MongoDB for data storage. To run the system for the first time from the CLI:

1. Run the frontend: ```npm start```
2. Install packages: ```npm install <module-name>```
3. Common packages for web side: ```bootstrap```, ```react```, ```react-icons```, ```react-router```, ```redux```, ```react-google-maps/api```,
4. Common packages for server side: ```express```, ```axios```, ```cors```,
5. Common packages for database: ```mongoose```
6. Run the server: ```nodemon App.js``` or ```node App.js```

## Functionalities

### Homepage
Landing page for guests

#### Components:
- **Top 5 likes/follows:** Dynamic board that changes with in-time ratings from users
- **Brewery bank:** All breweries claimed from brewery owners (users) or from a remote API, listing name (hyperlink to homepage), brewery type, beer serving, contact info, like/follow/comment, random search, sign in/up
- **Navigation:** Activities, Random Search, Next/Previous Page, My Breweries (owner only)

### Login/Register
User-oriented or triggered by clicking unauthorized button

#### Components:
- **Sign in:** Successful login redirects to personal profile for information updates
- **Sign up:** Sign up as 3 types of user: user, brewery owner, admin
- **Navigation:** Public profile, read followings/followers

### Search from External APIs
#### Components:
- **Google Map API:** Random search location by brewery name
- **Remote API:** Return brewery details from "https://www.openbrewerydb.org/"

### Details
#### Components:
- **Map window:** Address and homepage
- **Retrieve related data from other database domains:** Beers & Stores

### Profile
#### Components:
- **Personal profile:** Personal info updates
- **Public profile (admin excluded)**
- **User table (admin only):** CRUD operations on all website users
- **Navigation:** Followings/followers, brewery claim request (brewery-owner/admin only)

### Activities
#### Components:
- **Unlike/Unfollow**
- **Ratings bank:** Listing all the breweries the user ever liked/followed/commented and all shared reviews from given breweries
- **Settings (admin only):** Delete breweries, excluding newly claimed ones

## Error Handling

Included try-catch blocks to handle errors. When users navigate to pages (e.g., personal profile, activities, settings) via copying URLs, they will be redirected to login. Like/follow/comment also requires user authentication.

## Deployment

- **Server from Heroku:** [Heroku Server](https://cafe-node-server-06d2fe9af4a2.herokuapp.com/)
- **Web from Netlify:** [Netlify Web](https://main--kaleidoscopic-conkies-6c59ca.netlify.app/)

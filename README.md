# BestNow

## Specification Deliverable

### Elevator pitch

At BestNow, we understand the frustration of spending countless hours searching for trustworthy product reviews across multiple websites, only to be bombarded by ads and conflicting opinions. That's why we've created a platform that does the hard work for you. BestNow aggregates trending, highly rated products from trusted sources, presenting a clear, concise view of what actual users say. Whether you're looking for the latest gadget or a daily essential, BestNow helps you make confident decisions quickly and easily by showing you the best products.

### Design

![Mock](bestnow.png)

Here is a sequence diagram that shows how to people would interact with the backend to vote.

```mermaid
sequenceDiagram
    actor Alice
    actor Juan
    actor Bud
    Alice->>Server: product review
    Server -->>Juan: product review with Alice's review added
    Server -->>Bud: product review with Alice's review added
    Juan->>Server: Like Alice's good review
    Server -->>Bud: Alice's review like count + 1
    Server -->>Alice: your review like count + 1
```

### Key features

- Secure login over HTTPS
- Collect data about a product reviews
- display the reviews
- Ability to let users like a review
- Display the number of likes a review has
- Ability to sort reviews by number of likes
- Ability for users to add reviews
- Ability for users to edit/delete reviews
- People can see the reviews from different site in real time

### Technologies

I am going to use the required technologies in the following ways.

- **HTML** - Uses correct HTML structure for application. Start with three HTML pages. One for login and one for write reviews, and one for displaying reviews.
- **CSS** - Application styling that looks good on different screen sizes, uses good whitespace, color choice and contrast.
- **React** - Provides login, choice display, display the product reviews data from different site, and use of React for routing and components.
- **Service** - Backend service with endpoints for:
  - login
  - retrieving review data
  - submitting new reviews
- **DB/Login** - Store users, people's reviews in database. Register and login users. Credentials securely stored in database. Can't review a product unless authenticated.
- **WebSocket** - As each review got liked, their likes are broadcast to all other users.

## HTML deliverable

➡️ The following is an example of the required information for the `Startup HTML` deliverable

For this deliverable I built out the structure of my application using HTML.

- [ ] **HTML pages** - Three HTML page that represent the ability to login and display reviews and write reviews.
- [ ] **Links** - The login page automatically links to the Home page(home page contains product review products). The Home page has a link to the write review page.
- [ ] **Text** - The login page has a login form. The Home page has a list of products with reviews. The write review page has a form to write a review.
- [ ] **Images** - Images will be added for represent the products.
- [ ] **DB/Login** - Input box and submit button for login. The voting choices represent data pulled from the database.
- [ ] **WebSocket** -

## CSS deliverable

➡️ The following is an example of the required information for the `Startup CSS` deliverable

For this deliverable I properly styled the application into its final appearance.

- [ ] **Header, footer, and main content body**
- [ ] **Navigation elements** -
- [ ] **Responsive to window resizing** - My app looks great on all window sizes and devices
- [ ] **Application elements** - Used good contrast and whitespace
- [ ] **Application text content** - Consistent fonts
- [ ] **Application images** -

## React deliverable

➡️ The following is an example of the required information for the `Startup React` deliverable

For this deliverable I used JavaScript and React so that the application completely works for a single user. I also added placeholders for future technology.

- [ ] **Bundled and transpiled** - done!
- [ ] **Components** - Login, voting list, vote are all components with mocks for login, WebSocket.
  - [ ] **login** - When you press enter or the login button it takes you to the voting page.
  - [ ] **database** - Displayed the voting counts. Currently this is stored and retrieved from local storage, but it will be replaced with the database data later.
  - [ ] **WebSocket** - I used the setInterval function to periodically increase a random vote count. This will be replaced with WebSocket messages later.
  - [ ] **application logic** - The highlight and ranking number change based up the user's selections.
- [ ] **Router** - Routing between login and voting components.
- [ ] **Hooks** - Vue uses class properties instead of `UseState` to track changes in vote state.

## Service deliverable

➡️ The following is an example of the required information for the `Startup Service` deliverable

For this deliverable I added backend endpoints that receives votes and returns the voting totals.

- [ ] **Node.js/Express HTTP service** - done!
- [ ] **Static middleware for frontend** - done!
- [ ] **Calls to third party endpoints** - I didn't have time to implement this. 😔
- [ ] **Backend service endpoints** - Placeholders for login that stores the current user on the server. Endpoints for voting.
- [ ] **Frontend calls service endpoints** - I did this using the fetch function.

## DB/Login deliverable

➡️ The following is an example of the required information for the `Startup DB/Login` deliverable

For this deliverable I associate the votes with the logged in user. I stored the votes in the database.

- [ ] **MongoDB Atlas database created** - done!
- [ ] **Stores data in MongoDB** - done!
- [ ] **User registration** - Creates a new account in the database.
- [ ] **existing user** - Stores the votes under the same user if the user already exists.
- [ ] **Use MongoDB to store credentials** - Stores both user and their votes.
- [ ] **Restricts functionality** - You cannot vote until you have logged in. This is restricted on the frontend only. 😔

## WebSocket deliverable

➡️ The following is an example of the required information for the `Startup WebSocket` deliverable

For this deliverable I used webSocket to update the votes on the frontend in realtime.

- [ ] **Backend listens for WebSocket connection** - done!
- [ ] **Frontend makes WebSocket connection** - done!
- [ ] **Data sent over WebSocket connection** - done!
- [ ] **WebSocket data displayed** - All user votes display in realtime. I'm really proud that this is working. Way cool!

## Notes

For more details on what I learned, check out my [notes.md](./notes.md).

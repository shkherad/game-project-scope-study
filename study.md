# Game Project Scope Study

## Required Readings

-   [Game Project](https://github.com/ga-wdi-boston/game-project)
-   [Game API](https://github.com/ga-wdi-boston/game-project-api)
-   [What is a User Story](http://searchsoftwarequality.techtarget.com/definition/user-story)

## Deliverables

After reading the `game-project` prompt and the `game-project-api` documentation
please do the following and be prepared to share and discuss during our next
class.

Submit detailed answers to these in this file via a pull request.

-   A wireframe of what your game project will look like.
-   The data structure you plan to use.
-   How you will take the markup of the game board and represent it in JS
-   How you plan to approach this project.
-   4-8 user stories for your game project.
-   How you plan to keep your code modular.
-   What creative spin will you add to your project.
-   How you will use version control to backup / track your project.
-   Do you plan to attempt any of the bonuses.

WIREFRAME:
-Extremely clean
-Login screen upon arrivial is a block with
  login: email, password
  sign up: email, password, password
  main screen can toggle between these two
-Main screen: game right in middle of screen
  left dropdown to keep track of statiics
  right dropdown: logout, change password etc
-Change password will pop up similat box to loging but
  old password, new password, submit/close
-Logout will clear page contents and return to home login/signup menu

DATA STRUCTURE:
Ajax+json communicating with ruby server
Ruby server will keep track of users for authentication
  current games
  game status
  (see game api)
Ajax will get/set user information and game information
Client will sent game statuses back to the server but will calculate
  the result of a game each time a move is sumbitted.
Games will be in form of a 9 element array

GAME BOARD MARKUP:
Game will be represented as a 9 element array with indicies 0-8:
0-1-2
3-4-5
6-7-8
or game array = [0,1,2,3,4,5,6,7,8];
Game will be initialized as an empty string array length 9
Then filled in with a player x or o.
All cobinations for winning will be represented in an if || statement to determine
  game status.

GAME PLAN:
Build out everything in modules. Achieve functionality first then play around with appearance. When both are satisfactory then go back to build in more functionality features.
Modules: authentication, login,change password, logout
Logic: filling game array, testing game status,
    keoing track of statistics
Appearance: games appear side by side, stacked on mobile
    maximum of 4 games at onCreateNewGame

USER STORIES:
As an administrator I want to keep track of every user so that I can track an inidviduals statistics.

As an administrator, I want to keep track of everyone who is logged in so that I can pair individuals with other individuals to play a game.

As a user I want to create my own user profile and password so that I am the only one that can play from my account.

As a user I want to play more than one game at a time so that I don't need to wait for one person to make a move.

As a user I want to be able to know who won the game so that I dont waste time if the game is a draw and keep track of statistics.

As a user I want to know if it is my turn or an opponents turn so I know what game I should give my attention.

As a user I want to know if I am x or o so that I don't have to remember each time.

MODULAR CODE:
First I will begin by laying out a base holding the repo with all files. I will commit often, separating authentication features from game features, from styling features etc.

CREATIVE SPIN:
I like clean UI so I do not want to do a whole bunch of bacgronds and colors etc. I do want multiple games to go acrosss the screen and scale as more games are added or stack on mobile. Perhaps I will add animations the the drawing of an x or o when a player makes a move or an animating win line.  A creative alternative is to use cats and dogs instead of x's and o's.

VERSION CONTROL:
Commit early and often! Everytime I finish a feature, I will commit.

BONUSES:
I want to attempt allowing users to play from multiple devices.

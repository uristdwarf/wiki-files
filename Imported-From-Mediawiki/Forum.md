```{=mediawiki}
{{Infobox Project
|name = forum
|image = [[File:Forum.png|250px]]
|require = [[lem-in]]
|xp = 76.3 kB
|language = Go
|members = 2 -> 5
|type = Basic
}}
```
Forum is the first large scale project of the program. You will need to
implement a database, sessions, users, registering/login, a post/comment
structure, being able to posts/comments and liking/disliking those same
posts and comments. You will also need to implement a basic \"user
page\" that shows that users likes and post history. The project
requires at least 2 people but it\'s recommended that you be part of a
larger team since this reduces the amount of XP needed for auditing (you
will need at least 10 audits to pass. If your team consists of 2 members
this will result in about \~380k incoming XP at the end). Being part of
a larger team also means you can practice on using [collaboration
tools](Collaborating "wikilink") that are used every day in software
development.

## Database

In order to store the data in your forum (like users, posts, comments,
etc.) you will use the database library SQLite.

SQLite is a popular choice as an embedded database software for
local/client storage in application software such as web browsers. It
enables you to create a database as well as controlling it by using
queries.

To structure your database and to achieve better performance we highly
advise you to take a look at the entity relationship diagram and build
one based on your own database.

-   You must use at least one SELECT, one CREATE and one INSERT queries.

To know more about SQLite you can check the [SQLite
page](SQLite "wikilink").

## User registration/login {#user_registrationlogin}

In this segment the client must be able to register as a new user on the
forum, by inputting their credentials. You also have to create a login
session to access the forum and be able to add posts and comments.

You should use cookies to allow each user to have only one opened
session. Each of this sessions must contain an expiration date. It is up
to you to decide how long the cookie stays \"alive\".

Instructions for user registration:

-   Must ask for email
    -   When the email is already taken return an error response.
-   Must ask for username
-   Must ask for password
    -   The password must be encrypted when stored

The forum must be able to check if the email provided is present in the
database and if all credentials are correct. It will check if the
password is the same with the one provided and, if the password is not
the same, it will return an error response.

### Sessions

WIP

## Posting and commenting {#posting_and_commenting}

In order for users to communicate between each other, they will have to
be able to create posts and comments.

-   Only registered users will be able to create posts and comments.
-   When registered users are creating a post they can associate one or
    more categories to it.
    -   The implementation and choice of the categories is up to you.
-   The posts and comments should be visible to all users (registered or
    not).
-   Non-registered users will only be able to see posts and comments.

## Likes and Dislikes {#likes_and_dislikes}

Only registered users will be able to like or dislike posts and
comments.

The number of likes and dislikes should be visible by all users
(registered or not).

## Filter

You need to implement a filter mechanism, that will allow users to
filter the displayed posts by :

-   categories
-   created posts
-   liked posts

You can look at filtering by categories as subforums. A subforum is a
section of an online forum dedicated to a specific topic.

Note that the last two are only available for registered users and must
refer to the logged in user.

## Docker

For the forum project you must use [Docker](Docker "wikilink").

## Helpful Materials {#helpful_materials}

[Useful database patterns and how to solve their
pitfalls](https://www.slideshare.net/billkarwin/sql-antipatterns-strike-back/48)

[How to make small and focused pull
requests](https://artsy.github.io/blog/2021/03/09/strategies-for-small-focused-pull-requests/)

[Organizing Database
Access](https://www.alexedwards.net/blog/organising-database-access)

[On the uses and misuses of panics in
Go](https://eli.thegreenplace.net/2018/on-the-uses-and-misuses-of-panics-in-go/)

[SQL Test Data Generator](https://www.mockaroo.com/)

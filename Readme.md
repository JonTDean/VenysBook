# MERN Social-Dev

## To-Do

- [ ] Refactor The Backend once Finished, separate each of the Route 'router.HTTP_REQ' via SRD (The Single Responsiblity Design Pattern)

---

## Summary

The MERN Social-Dev site is a pet project in order to utilize React and Express in a developmental Setting.

---

## Documentation

Documentation for the site

### Backend

API:

1.  Users & Auth

    Link: https://documenter.getpostman.com/view/11934869/TVRg6pFy

    | Schema | HTTP Request | Parameters                                                  | URL        | Description               |
    | ------ | ------------ | ----------------------------------------------------------- | ---------- | ------------------------- |
    | User   | POST         | Headers: { <br/> "Content-Type": "application/json" <br/> } | /api/users | Register User to Database |

    | Schema | HTTP Request | Parameters                                                  | URL       | Description    |
    | ------ | ------------ | ----------------------------------------------------------- | --------- | -------------- |
    | Auth   | GET          | Headers: { <br/> "x-auth-token": USER_TOKEN <br/> }         | /api/auth | Authorize User |
    | Auth   | POST         | Headers: { <br/> "Content-Type": "application/json" <br/> } | /api/auth | Login User     |

2.  Profile

    Link: https://documenter.getpostman.com/view/11934869/TVRg6pFx

    | Schema  | HTTP Request | Parameters                                                                                    | URL                     | Description                    |
    | ------- | ------------ | --------------------------------------------------------------------------------------------- | ----------------------- | ------------------------------ |
    | Profile | GET          | Headers: { <br/> "Content-Type": "application/json", <br/> "x-auth-token": USER_TOKEN <br/> } | /api/profile/me         | Get logged in profile data     |
    | Profile | GET          | PATH_VARIABLES: { <br/> ":id" : USER_ID <br/> }                                               | /api/profile/user/:id   | Grab profile by user ID        |
    | Profile | GET          |                                                                                               | /api/profile            | Grab all Profiles              |
    | Profile | POST         | Headers: { <br/> "Content-Type": "application/json", <br/> "x-auth-token": USER_TOKEN <br/> } | /api/profile            | Create and Update Profile      |
    | Profile | DELETE       | Headers: { <br/> "x-auth-token": USER_TOKEN <br/> }                                           | /api/profile            | Delete the Specified Profile   |
    | Profile | PUT          | Headers: { <br/> "Content-Type": "application/json", <br/> "x-auth-token": USER_TOKEN <br/> } | /api/profile/experience | Add Experience to Profile      |
    | Profile | DELETE       | Headers: { <br/> "x-auth-token": USER_TOKEN <br/> }                                           | /api/profile/experience | Delete Experience from profile |
    | Profile | PUT          | Headers: { <br/> "Content-Type": "application/json", <br/> "x-auth-token": USER_TOKEN <br/> } | /api/profile/education  | Add Education to profile       |
    | Profile | DELETE       | Headers: { <br/> "x-auth-token": USER_TOKEN <br/> }                                           | /api/profile/education  | Delete Education from profile  |

3.  Posts

    Link: https://documenter.getpostman.com/view/11934869/TVRg6p2d

    | Schema | HTTP Request | Parameters                                                                                                                            | URL                                | Description             |
    | ------ | ------------ | ------------------------------------------------------------------------------------------------------------------------------------- | ---------------------------------- | ----------------------- |
    | Posts  | GET          | Headers: {<br> "x-auth-token": USER_TOKEN<br>}                                                                                        | /api/posts                         | Get all posts           |
    | Posts  | GET          | PATH_VARIABLES:{<br> ":id": POST_ID<br>}<br><br>Headers: {<br> "x-auth-token": USER_TOKEN <br>}                                       | /api/posts/:id                     | Grab post by ID         |
    | Posts  | POST         | Headers: {<br> "Content-Type": "application/json",<br> "x-auth-token": USER_TOKEN <br>}                                               | /api/posts                         | Create a Post           |
    | Posts  | PUT          | PATH_VARIABLES: {<br> ":id": POST_ID<br>}<br>Headers: {<br> "x-auth-token": USER_TOKEN <br>}                                          | /api/posts/like/:id                | Like Post               |
    | Posts  | PUT          | PATH_VARIABLES: {<br> ":id": POST_ID<br>}<br>Headers: {<br> "x-auth-token": USER_TOKEN <br>}                                          | /api/unlike/:id                    | Unlike a Post           |
    | Posts  | POST         | PATH_VARIABLES: {<br> ":id": POST_ID<br>}<br>Headers: {<br> "Content-Type": "application/json", <br> "x-auth-token": USER_TOKEN <br>} | /api/posts/comment/:id             | Add a comment to a Post |
    | Posts  | DELETE       | PATH_VARIABLES: {<br> ":id": POST_ID,<br> ":comment_id": COMMENT_ID<br>}<br><br>Headers: {<br> "x-auth-token": USER_TOKEN <br>}       | /api/posts/comment/:id/:comment_id | Delete User comment     |

---

### Frontend

API:

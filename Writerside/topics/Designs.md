# Designs

## Frontend

| Route       | Description                                                        |
|-------------|--------------------------------------------------------------------|
| `/`         | Landing page. Getting started or News feeds                        |
| `/register` | Register                                                           |
| `/login`    | Login                                                              |
| `/profile`  | User profile page. Only renders after login. Else, redirect to `/` |
| `/shop`     | Place to buy products                                              |

## Backend

| Endpoint    | Method                | Input                                   | Return    | Description                                                                                    |
|-------------|-----------------------|-----------------------------------------|-----------|------------------------------------------------------------------------------------------------|
| `/register` | `POST`                | `username`, `password`                  | `message` | Register a new user (create folder)                                                            |
| `/login`    | `POST`                | `username`, `password`                  | `message` | Login as user (check password)                                                                 |
| `/data`     | `GET` `POST` `DELETE` | `username`, `filename`                  | `message` | Get, update, or delete one user file                                                           |
| `/user`     | `GET` `POST` `DELETE` | `username`, [`password`, `newPassword`] | `message` | Get or delete a user; use `POST` to change the password. `POST` and `DELETE` requires password |
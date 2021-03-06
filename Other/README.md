---
title: Other
---

## Setting up environment Variable in a Postman Collection

```js
// - Code to be pasted in Tests Tab of a Request
var jsonData = JSON.parse(responseBody);
pm.environment.set("ACCESS_TOKEN", jsonData["access"]);

// - Using the Set variable : `{{ACCESS_TOKEN}}`
```

## Heroku

```sh
heroku login # Login to heroku `
heroku create # Creating an heroku app(repo)
git push heroku master # Pushing the changes
heroku run bash # Running the Heroku bash in local system
heroku logs --tail # Logging logs
heroku open # To Open the App
heroku auth:whoami # To see the login ID
heroku git:clone -a APP_NAME # to clone a heroku app
```

- [Renaming the app](https://devcenter.heroku.com/articles/renaming-apps)

## Screen Commands in Linux

- By using Screen command in Linux we can start multiple shell session at the same time and use them.
- [https://www.geeksforgeeks.org/screen-command-in-linux-with-examples/](https://www.geeksforgeeks.org/screen-command-in-linux-with-examples/)

```sh
# - Installing Screen
	- sudo apt install screen
# - Start a Screen Session
	- sudo screen
	- sudo screen -S SESSION_NAME
# - See the List of the Screens
	- sudo screen -ls
# - To detach a Screen
	- screen -d SESSION_ID
# - To attach to a detached Screen
	- screen -r SESSION_ID
# - To Close a Screen
	# - I - Go to that screen
	# - II - type exit
# - To attach to a not detached Screen
	- screen -x SESSION_ID
# - To rename a session
	- I - Go to that Session Screen
	- II - (CTRL + A) + type :sessionname NEW_SESSION_NAME
# - To see the current Session name
	- I - Go to that Session
	- II - echo $STY
```

## VIM Usage

- Modes
  - Insert Mode (i)
  - to change a mode press ESC
- Working with Files
  - Opening a file in vim `vim hello.txt`
  - Saving a file in Vim
  - Saving a file and switching back to normal mode without closing vim
    - `ESC + :w + ENTER`
  - Saving a file with another name
    - `ESC + :w NEW_FILE_NAME + ENTER`
  - To save a file and Quit Vim
    - `ESC + :wq + ENTER`
    - `ESC + :x + ENTER`
    - Difference b/w `:wq` and `:x`
      - `:wq` - always write buffer to file so modify its time
      - `:x` - only write to file when there are unsaved changes
- Moving the Cursor
  - j - down
  - k - up
  - h - left
  - l - right

## Sublime Shortcuts

- `ctrl + alt + down_arrow` : to make multiple cursor
- `alt + f3` : to select all the same text on which currently cursor is
- `ctrl + click` : to add cursor to the position where we click
- `ctrl + d` : make multiple cursor at the next text under the cursor
- `ctrl + tab` : to go to next tab
- `ctrl + shift + tab` : to go to previous tab
- `ctrl + w` : to close a tab
- `ctrl + shit + t` : to reopen the recently closed tab
- `alt + shift + (1,2,3,4)`: to open multiple layout
- `alt + shift + (8,9)` : to open to row layout
- `alt + shift + 5` : to open 4 layout grid
- `ctrl + shift + (up,down)` : to move a line up or down
- `esc` : to close the down bar
- `ctrl + k + ctrl + b` : to toggle the side bar
- `ctrl + b` : to run the build system
- `ctrl + shift + b` : to choose the build system
- `ctrl + /` : to do comment
- `.someClass>ul>li>a*8`

## Setting Up Husky

```bash
cd FOLDER_NAME
git init
npm init -y
yarn add -D husky lint-staged prettier
```

- Add following code to `package.json` file

```json
{
  "husky": {
    "hooks": {
      "pre-commit": "lint-staged"
    }
  },
  "lint-staged": {
    "./src/*.{js,jsx,ts,tsx}": ["npx prettier --write"]
  },
  "dependencies": {}
}
```

- Create some `.js` file in `src` folder

```jsx
// src/sum.js
function sum(a, b) {
  console.log("Hello world");
  return a + b;
}

module.exports = sum;
```

- Now, when we are going to commit it will **format the code** before committing

```bash
git commit -m "COMMIT MESSAGE"
```

## Netlify toml file for custom build folder

- `netlify.toml`

```toml
[build]

base = "website/"
```

## MySQL Installation Terminal

```sh
sudo apt update
sudo apt install mysql-server
sudo service mysql start
sudo mysql_secure_installation
sudo mysql -u root -p
  > Apple@123

sudo service mysql start
sudo apt show mysql-server
```

- To see the password validation configurations

  - https://stackoverflow.com/questions/43094726/your-password-does-not-satisfy-the-current-policy-requirements
  - SHOW VARIABLES LIKE 'validate_password%';

- To alter user password
  - https://stackoverflow.com/questions/50093144/mysql-8-0-client-does-not-support-authentication-protocol-requested-by-server
  - ALTER USER 'root'@'localhost' IDENTIFIED WITH mysql_native_password BY 'Apple@123';
  - flush privileges;

## VSCode Code Snippet

```json
{
  "editor.formatOnSave": true,
  "css.remoteStyleSheets": [
    "https://stackpath.bootstrapcdn.com/bootstrap/4.5.0/css/bootstrap.min.css"
  ]
}
```

## Text Editors in bash

- nano - to write something to file
- cat - to view small file
- less - to view large file
- head / tail - to view some peace of text

## Sprint Plan

- Backlogs
- ToDo Sprint 01
- ToDo Sprint 02
- InDesign/Research
- Development
- Blocked
- Testing
- Review
- Released

### Task Status

- Not Started
- In Progress
- Completed

NATOURS Project:

____________________________________________________________________________________________________________________________

Start:

1. Download the files to a local folder and open it in VSC.

2. For security reasons change the PORT number that is set to '1234' and save the file.
   For that go to 'package.json' --> 'scripts' --> "devserver": "live-server --port=XXXX" (choose any number with 4 digits).

3. In VSC, open a terminal window and type 'npm i' (this will install the necessary dependencies for the site to work properly. See 'package.json').

4. In a terminal window type 'npm run build:css'.
   This command will run the following script: 
   "build:css": "npm-run-all compile:sass concat:css prefix:css compress:css"
   
   This script will automatically run 4 other scripts:
       . "compile:sass" : script that is going convert 'sass/main.scss' into 'css/style.comp.css'
       . "concat:css" : script that is going to concatenate files 'css/style.concat.css' and 'css/icon-font.css' into 'css/style.comp.css'
       . "prefix:css" : script that is going to introduce in the file 'css/style.concat.css' the necessary prefix of the lastest 10 browsers.
                        The result is going to be stored in 'css/style.prefix.css'.
       . "compress:css" : script that is going to compress the file 'css/style.prefix.css' into 'css/style.css'.
                          The result will be a unique line of code, with all the CSS code and without spaces.

5. In a terminal window type 'npm start'.
   This command will run the following script: 
   "start": "npm-run-all --parallel devserver watch:sass"

   This script will automatically run 2 other scripts:
       . "devserver" : script that is going to open a page in your pre defined browser and reload the page when changes are made in the code.
       . "watch:sass" : script that is going to watch if you have made any changes in your SCSS code and togheter with "devserver" script
                        will reload the page.
                        

____________________________________________________________________________________________________________________________

Notes:

. Copyright © by Jonas Schmedtmann. Original design is credit to the original author, Jonas Schmedtmann.
. My special thanks to Jonas Schmedtmann for is online course 'Advanced CSS and SASS'.
. Responsibility for downloads, assembly files and launch this project in the browser, are your sole responsibility. 
. Enjoy it!!
  
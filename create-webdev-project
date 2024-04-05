#!/bin/sh

if [ $# -eq 0 ]
    # Ensure a name parameter has been provided
  then
    echo "Please provide a project name"
    exit 1
fi


# Save project name
PROJECT_NAME="$1"
LANG="${2:-en}"
 
# HTML CONTENT
function HTML_BODY
{
    echo '<!doctype html>
<html lang="'$LANG'">
    <head>
        <meta charset="UTF-8" />
        <meta name="viewport" content="width=device-width, initial-scale=1" />
        <title> '$PROJECT_NAME' </title>
        <!-- CSS -->
        <link href="css/style.css" rel="stylesheet">
    </head>
    <body>
        <div id="main">

        </div>
        
        <!-- JS -->
        <script src="js/script.js" type="module"></script>
    </body>
</html>'
}

function CSS_BODY
{
    echo "
/* default */
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
  font-family: Arial, Helvetica, sans-serif;
}

/* general */
a {
  text-decoration: none;
  color: #59b4d6;
}
a:hover {
  color: #5fe3f6;
}

#main {

}

/* flex-container with auto adjustable flex-item */ 
.flex-container {
  display: flex;
  justify-content: center;
  gap: 20px;
}

.flex-item {
  width: 0px;
  flex: 1 0 auto;
}"
}

# Create The directories
mkdir -p "$PROJECT_NAME"
mkdir -p "$PROJECT_NAME/js"
mkdir -p "$PROJECT_NAME/css"

# CSS
touch "$PROJECT_NAME/css/style.css"
CSS_BODY > "$PROJECT_NAME/css/style.css"

# JS
touch "$PROJECT_NAME/js/script.js"

# INDEX
touch "$PROJECT_NAME/index.html"
HTML_BODY > "$PROJECT_NAME/index.html"

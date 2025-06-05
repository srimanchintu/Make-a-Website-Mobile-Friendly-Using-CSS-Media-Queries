# step 1
Launch Visual Studio Code.
Open your project folder or the specific HTML file you want to edit element 
# step 2
Search your HTML and CSS files for elements with fixed widths, such as:

width: 600px; 
# step 3
@media (max-width: 768px) {
  /* Styles for smaller screens */
}
# step 4 
@media (max-width: 768px) {
  .container {
    flex-direction: column;
  }
  .column {
    width: 100%;
  }
  body {
    font-size: 16px;
  }
}
# step 5 
@media (max-width: 768px) {
  .nav-menu {
    flex-direction: column;
    display: none; /* Hide menu by default */
  }
  .nav-toggle {
    display: block; /* Show toggle button */
  }
}

Implement JavaScript to toggle the .nav-menu display when the .nav-toggle button is clicked.
# step 6 
Open your webpage in Google Chrome.

Press Ctrl + Shift + I (or Cmd + Option + I on Mac) to open DevTools.

Click the Toggle Device Toolbar icon (or press Ctrl + Shift + M) to simulate different device viewports.

Test your page's responsiveness across various screen sizes. 
# step 7 
* {
  box-sizing: border-box;
}
body {
  overflow-x: hidden;
}
img {
  max-width: 100%;
  height: auto;
}
# step 8 
img {
  max-width: 100%;
  height: auto;
  display: block;
}
# i have done this task 4 with help of css and html 

 # OUTPUT 
 
 <!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <style>
    body {
      font-family: Arial, sans-serif;
      margin: 0;
      padding: 0;
    }
    .nav-toggle {
      display: none;
      background-color: #333;
      color: white;
      padding: 14px 20px;
      cursor: pointer;
    }
    .nav-menu {
      display: flex;
      list-style: none;
      background-color: #333;
      padding: 0;
      margin: 0;
    }
    .nav-menu li {
      padding: 14px 20px;
      color: white;
    }
    .container {
      display: flex;
      flex-direction: row;
    }
    .column {
      flex: 1;
      padding: 20px;
    }
    img {
      max-width: 100%;
      height: auto;
      display: block;
    }
    @media (max-width: 768px) {
      .container {
        flex-direction: column;
      }
      .nav-menu {
        flex-direction: column;
        display: none;
      }
      .nav-toggle {
        display: block;
      }
      body {
        font-size: 16px;
      }
    }
  </style>
</head>
<body>
  <div class="nav-toggle">Menu</div>
  <ul class="nav-menu">
    <li>Home</li>
    <li>About</li>
    <li>Contact</li>
  </ul>
  <div class="container">
    <div class="column">
      <h2>Column 1</h2>
      <p>Content for column 1.</p>
    </div>
    <div class="column">
      <h2>Column 2</h2>
      <p>Content for column 2.</p>
    </div>
  </div>
  <script>
    const toggle = document.querySelector('.nav-toggle');
    const menu = document.querySelector('.nav-menu');
    toggle.addEventListener('click', () => {
      menu.style.display = menu.style.display === 'flex' ? 'none' : 'flex';
    });
  </script>
</body>
</html>

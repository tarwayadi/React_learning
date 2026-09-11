# some important terms to understand:
  
# what is NPM?
---> it stands for Node Package manager
it comes with Node.js. its main job is to help you install , manage and run JavaScript packages/tools

think of npm like an app store
suppose you need a package react.
instead of writing everything yourself, you can tell npm: npm install react



npm downloads react and put it into your project
so,
            You
            ↓
            npm
            ↓
            Download package
            ↓
            Your project


npm → "Install/manage this tool."
npx → "Run/use this tool."




goal ye hai ki javascript ko html me inject kaise krein
javascript akele jab bhi chalti hai to vo sirf javascript hi chalti hai usko html me lana hi padega scripts call krni hi padegi


# what happens?
Normal Html  + javascript mein:
Browser directly html ko render krta hai:
aur agar javascript chalani hai toh html mein javascript file ko connect krna padta hai:

flow: 
        HTML
        ↓
        Browser
        ↓
        HTML page display

        JavaScript
        ↓
        <script> se HTML ke saath connect
        ↓
        Browser mein JavaScript execute


Example:

index.html
    <!DOCTYPE html>
    <html>
    <body>

        <h1 id="heading">Hello</h1>

        <script src="script.js"></script>
    </body>
    </html>

script.js

document.getElementById("heading").innerText = "Hello JavaScript";


Yahan JavaScript HTML ke DOM ko manipulate kar rahi hai.


lekin normal react mein kya hota hai ye thoda interesting part hai. React javaScript ke through UI create krta hai.

for example:

function App() {
    return <h1>Hello React</h1>
}

    JavaScript
        ↓
    React
        ↓
    UI/HTML
        ↓
    Browser

aur vite automatically tumhare react code ko browser ke liye prepare /create krta hai
isilye  hr baar manually :<script src="something.js"></script>
likhne ki zaroorat nhi hai


# in vite project

  main.jsx 
  import App from './App.jsx'

  aur phir:
    createRoot(document.getElementById('root')).render(
        <App />
    )

  yaani react root naam ka HTML element ke andar tumhari react UI ko render karta hai 


  # connection with previous javascript learning ?

    --> Vanilla JavaScript

        HTML
        ↕
        JavaScript
        ↓
        DOM manipulation

    where as:

     React

    JavaScript + JSX
        ↓
        React
        ↓
        DOM/UI

Its important to understand the connection because knowledge of DOM of JavaScript will be useful.

we will study it in detail that in JSX we can return only one html element.


what did we learn from the lecture 3:

1. jab bhi hum koi component bnaye create react se ya vite se to hum uska naam capital letter me likhe
2. kuchh libraries force krti hai ki app component ka naam jsx rakhe
3. basic flow and structure of a react project via vite.

       
# what is rendering?
rendering means taking your code/data and showing the result on the screen.

think:
            Your code
            ↓
            React processes it
            ↓
            UI is created/updated
            ↓
            Browser shows it


In your React code

Suppose App.jsx has:
 function App() {
  return <h1>Hello React</h1>
}

When React renders <App />, it basically means:
Take what App returns and display it in the browser."

So:

        App.jsx
        ↓
        <h1>Hello React</h1>
        ↓
        Browser
        ↓
        Hello React appears on screen

in main.jsx:
 we have seen:
   createRoot(document.getElementById('root')).render(
  <App />
)

the important part is: .render(<App />)

it means:
Render the App component inside the root element.

and html file that is index.html

<div id="root"></div>
So the overall flow is:
            index.html
                ↓
            <div id="root">
                ↓
            main.jsx
                ↓
            <App />
                ↓
            App.jsx
                ↓
            <h1>Hello React</h1>
                ↓
            Browser displays it

In React, rendering means React figures out what the UI should look like based on your components and their current data/state, then updates the browser's DOM accordingly.

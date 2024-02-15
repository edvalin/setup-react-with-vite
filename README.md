# Setup React With Vite
ReactJS is a JavaScript library developed by Facebook for building interfaces. It has gained widespread adoption owing to its declarative approach and the use of components. Components manage their own state and can be composed to easily build complex user interfaces. This lab is designed to build your proficiency with ReactJS starting from setting up a ReactJS web application and gradually building upon it to develop a functioning web application involving multiple views and ReactJS components. The lab environment provides you with a Visual Studio Code development environment so you can gain experience with one of the most popular tools for web application development as you progress through the lab.

### Learning Objectives
Upon completion of this lab you will be able to:

- Set up ReactJS applications using a Vite - a frontend development tool. 
- Produce production-ready code for web applications
- Create various types of ReactJS components
- Use acceptance criteria and mock-ups to identify component hierarchies

### Intended Audience
This lab is intended for:

- All who wish to learn how to use the ReactJS framework.

### Prerequisites
It is essential you understand the face of contemporary web development to attend this lab. We insist upon JavaScript experience, along with good HTML and CSS skills.



# Steps

To create a React application we will use Vite.

Vite eliminates the need for a bundler during development by using native ES modules through the browser. This allows for fast build times and instant updates. Vite offers a web development server with built-in hot module replacement.

1. To begin, open the new terminal window in your VSCode instance and type the following:
    ~~~~~~~
    npm create vite@latest
    ~~~~~~~

2. You will see a message asking to install the latest version of Create Vite. Key in `Y` for yes. 

3. Next, name the project. Change the default value of `viteproject` this to `calabs`. 

4. You will be propted with a drop-down menu. Select `React`. 

5. After selecting `React`, a new drop-down appears. Sselect `JavaScript`. 

6. The terminal now has a message suggesting you to do the following:
    ~~~~~~~
    cd calabs
    npm install
    npm run dev
    ~~~~~~~


# If running on CA-CLOUD-SERVER

Configure custom proxy rules for the dev server.
code-server rewrites the URL by stripping the base out when proxying
append `/absproxy/<port>` to base URL fixed the issue.

1. Open `vite.config.js` file
2. Edit `defineConfig()` function to the following:
    ~~~~~~~
    export default defineConfig({
        plugins: [react()],
        base: '/absproxy/8000',
        server: {
            host: true,
            port: 8000,
            strictPort: true
        },
    })
    ~~~~~~~

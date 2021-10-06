---
layout: mypost
title: React Learning Journey
categories: [React]
---

# React Learning Journey

### 2020.08.07 Code pen and React Coding Learnning

#### src and dis in the fold of the Code pen export file.

[1.What is the role of src and dist folders?](https://stackoverflow.com/questions/23730882/what-is-the-role-of-src-and-dist-folders)<br>
[Exporting Pens](https://blog.codepen.io/documentation/exporting-pens/)

#### 2.Put the code pen code into the "creat react -app" project

1.npm version check:

```
npm -version
```

2.npx install the creat new app

```
npx create-react-app my-app
```

3.For the project to build, these files must exist with exact filenames:

[](https://create-react-app.dev/docs/folder-structure)

```
For the project to build, these files must exist with exact filenames:

public/index.html is the page template;
src/index.js is the JavaScript entry point.
```

[How do I check the version of Node.js and npm installed on my machine?](https://www.quora.com/How-do-I-check-the-version-of-Node-js-and-npm-installed-on-my-machine)<br>
If you use npm 5.1 or earlier, you can't use npx. Instead, install create-react-app globally:
[https://gist.github.com/gaearon/4064d3c23a77c74a3614c498a8bb1c5f](https://gist.github.com/gaearon/4064d3c23a77c74a3614c498a8bb1c5f)<br>
[Creating an App](https://github.com/facebook/create-react-app)<br>
[Create a New React App](https://reactjs.org/docs/create-a-new-react-app.html)<br>

4.Remove the below code in index.js within src and add"<h1>Hello, world!</h1>,"into the file

```
<React.StrictMode>
    <App />
  </React.StrictMode>,
```

5.study note here:  
all react code will be chnaged in the index.js < src directory<br>
all html code willl be changed in the index.html < public directory<br>

```
Html in codepen ---> index.html at public in creat my-app(add in the middle of the body tag)

CSS in codepen  ----> index.css at src in create my-app (fully copy)

JS in Codepen----> indeµx.js at src in create my-app (add in the middle of  import scrpts  serviceworker )
```

6.allow the JS running in the website;
remove the no at "<script>You need to enable JavaScript to run this app.</script>" in index.hrml to run the app.
[React Error: Target Container is not a DOM Element](https://stackoverflow.com/questions/26416334/react-error-target-container-is-not-a-dom-element/35234369)
change the code into:

```
 <div id="app"></div>
    <script src="/bundle.js"></script>
```

7.allow the CSS running in the website:
convert the SCSS to CSS:
[SCSS to CSS](https://jsonformatter.org/scss-to-css)  
8.run the code in the browser:  
first you need to go to the project directory via cd then you need to use "npm start" to begin the project .

```
cd my-app
npm start
```

### 2020.08.07 Tic tac tutorail running

```
function Square(props) {
  return (
    <button className="square" onClick={props.onClick}>
      {props.value}
    </button>
  );
}

class Board extends React.Component {

renderSquare(i) {
    return (
    	<Square
    	value={this.props.squares[i]}
        onClick={() => this.props.onClick(i)}
    />
    );
  }

render(){
  return (
      <div>
       <div className="board-row">
          {this.renderSquare(0)}
          {this.renderSquare(1)}
          {this.renderSquare(2)}
        </div>
        <div className="board-row">
          {this.renderSquare(3)}
          {this.renderSquare(4)}
          {this.renderSquare(5)}
        </div>
        <div className="board-row">
          {this.renderSquare(6)}
          {this.renderSquare(7)}
          {this.renderSquare(8)}
        </div>
      </div>
    );
  }
}

class Game extends React.Component {
constructor(props) {
    super(props);
    this.state = {
      history: [{
        squares: Array(9).fill(null),
      }],
      xIsNext: true,
    };
  }

  handleClick(i) {
    const history = this.state.history;
    const current = history[history.length - 1];
    const squares = current.squares.slice();
    if (calculateWinner(squares) || squares[i]) {
      return;
    }
    squares[i] = this.state.xIsNext ? 'X' : 'O';
    this.setState({
      history: history.concat([{
        squares: squares
      }]),
      xIsNext: !this.state.xIsNext,
    });
}

  render() {
    const history = this.state.history;
    const current = history[history.length -1];
    const winner = calculateWinner(current.squares);

    let status;
    if (winner) {
    	status = 'Winner: ' + winner;
    	} else {
    		status ="Next player: " + (this.state.xisNext ? 'X' :'0');
    	}



    return (
      <div className="game">
        <div className="game-board">
          <Board
             squares={current.squares}
             onClick={(i) => this.handleClick(i)}
          />
        </div>
        <div className="game-info">
          <div>{status}</div>
          <ol>{/* TODO */}</ol>
        </div>
      </div>
    );
  }
}

// ========================================

ReactDOM.render(
  <Game />,
  document.getElementById('root')
);

function calculateWinner(squares) {
  const lines = [
    [0, 1, 2],
    [3, 4, 5],
    [6, 7, 8],
    [0, 3, 6],
    [1, 4, 7],
    [2, 5, 8],
    [0, 4, 8],
    [2, 4, 6],
  ];
  for (let i = 0; i < lines.length; i++) {
    const [a, b, c] = lines[i];
    if (squares[a] && squares[a] === squares[b] && squares[a] === squares[c]) {
      return squares[a];
    }
  }
  return null;
}
```

### study note:

1.Resource list<br>
2.Repeatthe code into the Codepen<br>
3.all content need to be refreshed<br>
4.Winner<br>
5.: and ;<br>
6.diffrerence checker:<br>
[Welcome to Diffchecker](https://www.diffchecker.com/)<br>

## Learning Resource list Overview

official document:<br>
[Tutorial: Intro to React](https://reactjs.org/tutorial/tutorial.html#completing-the-game)<br>
Tictoc game background introduction:<br>
[How to play Tic Tac Toe](https://www.youtube.com/watch?v=USEjXNCTvcc)<br>
[Learn React (Front end master)](https://frontendmasters.com/books/front-end-handbook/2018/learning/react.html)<br>
[complete Intro to React, v5](https://frontendmasters.com/courses/complete-react-v5/)<br>
[React (web framework)](<https://en.wikipedia.org/wiki/React_(web_framework)#External_links>)<br>
Bonus resource:  
Book:  
React book which I purchased from the Amazon  
React book in the Oreilly

Video:  
Tutorail & Website:  
Udacity<br>
[egghead.io](https://egghead.io/)  
[Markdown Preview Documentation](https://facelessuser.github.io/MarkdownPreview/usage/)<br>
[The History of React and Flux with Dan Abramov](https://threedevsandamaybe.com/the-history-of-react-and-flux-with-dan-abramov/)<br>
[Markdown Cheatsheet](https://github.com/adam-p/markdown-here/wiki/Markdown-Cheatsheet#links)<br>

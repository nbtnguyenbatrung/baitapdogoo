### <a name="home">Đáp án</a>

Tuần 01

- [Bài tập ngày 02](#day02)

- [Bài tập tuần 01](#tuan01)

- [Bài tập ngày 07](#day07)

> ### <a name="day02"> Bài tập ngày 02 </a>

### Bài 1:

- Liệt kê 10 thẻ inline
  - span
  - img
  - em
  - i
  - b
  - a
  - button
  - sub
  - sub
- Liệt kê 10 thẻ block
  - div
  - selection
  - body
  - h1
  - article
  - header
  - li
  - ol
  - map
  - p
  - select
- Liệt kê thẻ semactic
  - article
  - aside
  - figure
  - footer
  - header
  - main
  - mark
  - time
  - selection

### Bài 2: Làm 1 ví dụ về BEM cho block có tên là `boy`

BE: `boy__arm`, `boy__eye`, `boy__nose`

BEM: `boy__arm--long`, `boy__eye--big`

BM: `boy--tall`, `boy--fat`

### Bài 3: Áp dụng kiến thức về BEM đặt tên cho UI này: static.collectui.com/shots/1436570/dropdown-menu-large Hint: Block có tên `dropdown

Sử dụng font awesome, thêm đoạn sau vào dưới thẻ `<title>`

```
<link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/5.15.4/css/all.min.css" integrity="sha512-1ycn6IcaQQ40/MKBW2W4Rhis/DbILU74C1vSrLJxCq57o941Ym01SwNsOMqvEBFlcgUa6xLiPY/NS5R+E6ztJQ==" crossorigin="anonymous" referrerpolicy="no-referrer" />
```

Phân tích hình như sau

```
    <div class="dropdown">
        <div class="dropdown__select">
            <span class="dropdown__selected"></span>
            <i class="fa fa-caret-down dropdown__caret"></i>
        </div>
        <div class="dropdown_list">
            <div class="dropdown_item">
                <span class="dropdown_title"></span>
                <i class="fa fa-plus dropdown__icon" ></i>
            </div>
        </div>
    </div>

```

### Bài 4: Chèn font từ Google vào bài tập sử dụng Fonts Roboto với các độ đậm là 400 và 600

```
<link href="https://fonts.googleapis.com/css2?family=Roboto:wght@400;700&display=swap" rel="stylesheet">

body {
    font-family: 'Roboto', sans-serif;
}
```

### Bài 5: Tạo ra các button như hình: designerup.co/blog/content/images/2019/01/button_corners.png sử dụng padding, margin, text-align, kiến thức đã học

```
<div class="button">
    <a href="#" class="link">Button</a>
    <a href="#" class="link link--rounded">Button</a>
    <a href="#" class="link link--round">Button</a>
</div>

.link {
    text-decoration: none;
    padding: 1rem 5rem;
    text-align: center;
    color: white;
    background-color: purple;
    margin-right: 5rem;
}

.link--rounded {
    border-radius: 5px;
}

.link--round {
    border-radius: 2rem;
}

```

### Bài 6: Áp dụng pseudo :hover để khi rê chuột vào kết quả bài 5 thì đổi màu nền và màu chữ

```
.link:hover {
    color: black;
    background-color: wheat;
}

```

### Bài 7: Sử dụng CSS về child hoặc type để làm các màu như hình ví dụ color\_\_item:first-child{background-color:red}: cdn.dribbble.com/users/757683/screenshots/5942067/attachments/1281258/style_02.jpg

```
<ul>
    <li class="color_item"></li>
    <li class="color_item"></li>
    <li class="color_item"></li>
    <li class="color_item"></li>
    <li class="color_item"></li>
</ul>

.color_item {
    width: 13rem;
    height: 15rem;
    border-radius: 4px;
    margin-left: 2rem;
    margin-bottom: 2rem;
    display: inline-block;
}

.color_item:first-child {
    background-color: #a24bf0;
}

.color_item:nth-child(2) {
    background-color: #38dbb2;
}

.color_item:nth-child(3) {
    background-color: #25c2e3;
}

.color_item:nth-last-child(2) {
    background-color: #e8e8e8;
}

.color_item:last-child {
    background-color: #fcfcfc;
}
```

### Bài 8

```
<div data-link="https://google.com">google.com</div>

<div data-link="http://vnexpress.vn">vnexpress.vn</div>

<div data-name="hello">hello</div>

<div data-name="againhello">again hello</div>

<input type="email" name="email">

<input type="text" name="fullname">


div[data-link^="https"] {
    color: wheat;
}

div[data-link$=".vn"] {
    color: teal;
}

div[data-name*="hello"] {
    color: red;
}

input[type="email"] {
    background-color: yellow;
}

input[type="text"] {
    background-color: violet;
}
```

:top: [về đầu trang](#home)

> ## <a name="tuan01"> Bài tập tuần 01 </a>

### Bài 1: Tạo một máy tính cá nhân có thể thực hiện được các phép tính:

- Cộng
- Trừ
- Nhân
- Chia
- Bình phương
- Trị tuyệt đối
- Căn bậc 2

```

let Calculator = function () {}

Calculator.prototype.add = function (a, b) {
    return a + b;
}

Calculator.prototype.subtract = function (a, b) {
    return a - b;
}

Calculator.prototype.multiply = function (a, b) {
    return a * b;
}

Calculator.prototype.divide = function (a, b) {
  if (b === 0) {
    return 'Can not divide for Zero';
  }

  return a/b;
}

Calculator.prototype.power = (a) => {
  return a * a;
}


Calculator.prototype.abs = (a) => {
  if (a >= 0) {
    return a
  } else {
    return -1 * a;
  }
}

Calculator.prototype.sqrt = (a) => {
  if (a < 0) {
    return 'Can not calculator';
  } else {
    return Math.sqrt(a);
  }
}


```

Kiểm tra kết quả

```
let cal = new Calculator();

console.log("Sum: 1 + 2 = " + cal.add(1,2));
console.log("Subtract: 1 - 2 = " + cal.add(1,2));
console.log("Divide: 1/0 = " + cal.divide(1, 0));
console.log("Divide: 1/2 = " + cal.divide(1, 2));
console.log("Multiply: 3 * 2 = " + cal.multiply(3, 2));
console.log("Power of 3  = " + cal.power(3));
console.log("ABS of -3  = " + cal.abs(-3));
console.log("ABS of 3  = " + cal.abs(3));
console.log("Square root of 3  = " + cal.sqrt(3));
console.log("Square root of 4 = " + cal.sqrt(4));

```

### Bài 2: Yêu cầu là viết một hàm trả về giá trị của một số fibonacci cụ thể. Ví dụ, mình truyền vào là thứ tự của số đó, trả về giá trị của nó, fibonacci(4) trả về 3, fibonacci(6) trả về 8.

```
let Fibonacci = function () {}

Fibonacci.prototype.get = function (count) {
  if (count < 0) return "OOPS";
  if (count == 0) return 0;
  let a = 0;
  let b = 1;
  for (let i = 1; i < count; i++) {
      const temp = b;
      b = a + b;
      a = temp;
  }
  return b;
}
```

Kiểm tra kết quả

```
let fib = new Fibonacci();

console.log("Fibonacci at 8 is ", fib.get(8));
```

### Bài 03: Viết một hàm để kiểm tra một năm bất kỳ có phải là năm nhuận hay không?

```
let LeapYear = function () {};

LeapYear.prototype.isLeapYears  = function(year) {
	return year % 4 === 0 && ( year % 100 !== 0 || year % 400 == 0)
}
```

Kiểm tra kết quả

```
let leapYear = new LeapYear();

console.log("2025 is leap year? ", leapYear.isLeapYears(2025));
console.log("2028 is leap year? ", leapYear.isLeapYears(2028));
```

### Bài 4: Viết một hàm nhận vào 1 mảng và một số. Bạn cần phải tìm và xóa đối số đó khỏi mảng

```
var ArrayUtils = function () {};

ArrayUtils.prototype.removeFromArray  = function(...args) {
	const array = args[0];
	const newArray = [];
	array.forEach((item) => {
	  if (!args.includes(item)) {
		newArray.push(item);
	  }
	});
	return newArray;
}
```

Kiểm tra kết quả

```
let arrayUtils = new ArrayUtils();

console.log("remove  3, 4 from [1, 2, 3, 4] => " + arrayUtils.removeFromArray([1, 2, 3, 4], 3, 4));
```

### Bài 5: Viết một hàm đảo ngược chuỗi số

```
let NumberUtils = function () {};

NumberUtils.prototype.reverse = (n) => {
  n = n + "";

	return Number(n.split("").reverse().join(""));
}
```

Kiểm tra kết quả

```
let numberUtils = new NumberUtils();

console.log("Reverse number of 123456 is " + numberUtils.reverse(123456));
```

### Bài 6: Cho đoạn HTML sau, Hãy viết hàm JavaScript để thay đổi style của đoạn text được hiển thị trong thẻ `p`

```
<p id ='text'>Dogoo FS01 - Exercises</p>

<div>
    <button id="jsstyle" onclick="js_style()">Style</button>
</div>
```

Đáp án:

```
function js_style()
{
  //font styles added by JS:
  text.style.fontSize = "24pt";
  text.style.fontFamily = "Comic Sans MS";
  text.style.color = "red";
}
```

### Bài 7: Viết hàm JavaScript xoá toàn bộ phần tử của mảng nếu phần tử đó không là duy nhất

```
const filterNonUnique = (arr) => {
  return arr.filter(i => arr.indexOf(i) === arr.lastIndexOf(i))
}
```

Kiểm tra kết quả

```
console.log('Remove non unique ' + filterNonUnique([1,1,2,3,4,4,5,6,7]));
```

:top: [về đầu trang](#home)

### <a name="day07"> Bài tập ngày 07 </a>

Cho đoạn code hiện tại của Game Tic-Tac-Toe

https://codepen.io/gaearon/pen/gWWZgR?editors=0010

Hãy viết thêm các chức năng:

1. Hiển thị vị trí của mỗi bước đi dưới dạng (cột, dòng) trong lịch sử các bước đi.
2. In đậm bước hiện tại trong danh sách các bước đi.
3. Viết lại Board sử dụng hai vòng lặp để tạo ra Square thay vì hardcode như hiện nay.
4. Thêm toogle button cho phép sắp sếp các bước đi theo thứ tự tăng hoặc giảm.
5. Khi một người chơi thắng cuộc, highlight ba ô vuông dẫn đến chiến thắng.
6. Khi không ai thắng cuộc, hiển thị thông báo kết quả hòa.

Đáp án

```
import React from 'react';
import ReactDOM from 'react-dom';

import './index.css'


// class Square extends React.Component {
//     render() {
//         return (
//         <button className="square"
//             onClick={() => this.props.onClick()}>
//             {this.props.value}
//         </button>
//         );
//     }
// }

var toogleHis = false;

function Square(props) {
    return (
        <button
            className={props.winner ? 'square winner' : 'square'}
            onClick={props.onClick}>
            {props.value}
        </button>
    );
}

class Board extends React.Component {

    renderSquare(i) {
        const winnerRow = this.props.winner;

        return <Square
            value={this.props.squares[i]}
            key={i}
            onClick={() => this.props.onClick(i)}
            winner={ winnerRow != null && winnerRow.includes(i) ? true : false} />;
    }

    render() {

        const arrayX = [1, 2, 3];
        const arrayY = [1, 2, 3];


        return (
            <div>
                {
                    arrayY.map(y => (
                        <div className="board-row" key={y}>
                            {
                                arrayX.map(x => (
                                    this.renderSquare(x*y + (y-1) * (3-x) - 1)
                                ))
                            }
                        </div>
                    ))
                }
            </div>
        );
    }
}


class Game extends React.Component {
    constructor (props) {
        super(props);

        this.state ={
            history: [{
                squares: Array(9).fill(null),
                pos: '',
                isWinner: 'false',
            }],
            xIsNext: true,
            stepNumber: 0,
        }
    }


    handleClick (i) {
        const history = this.state.history.slice(0, this.state.stepNumber + 1);
        const current = history[history.length - 1];
        const squares = current.squares.slice();

        const pos = getPos(i + 1);

        if (calculateWinner(squares) || squares[i]) {
            return;
        }

        squares[i] = this.state.xIsNext ? 'X' : 'O';

        //const winner = calculateWinner(squares);

        //alert(winner);

        this.setState({
            history: history.concat([{
                squares: squares,
                pos: pos,
            }]),
            stepNumber: history.length,
            xIsNext: !this.state.xIsNext,
        });
    }

    jumpTo(step) {
        this.setState({
            stepNumber: step,
            xIsNext: (step % 2) === 0,
        });
    }

    toogle() {
        toogleHis = !toogleHis;

        this.forceUpdate();
    }

    render() {

        const history  = this.state.history;

        const current = history[this.state.stepNumber];

        const winner = calculateWinner(current.squares);

        const showHistory = toogleHis ? history.slice().reverse() : history;

        const moves = showHistory.map((step, index) => {

            const indexReverse = toogleHis ? Math.abs(index - (history.length - 1)) : index;

            let desc = '';
            let lastClass = '';

            if (toogleHis) {
                lastClass = index === 0 ? 'last-step' : 'step';
                desc = index === (history.length - 1) ? 'Go to game start' : 'Go to move #' + indexReverse;
            } else {
                lastClass = (index + 1 === history.length) ? 'last-step' : 'step';
                desc = index ? 'Go to move #' + index : 'Go to game start';
            }

            return (
                <li key={index} className={ lastClass }>
                    <button onClick={() => this.jumpTo(indexReverse)}> {desc} { step.pos } </button>
                </li>
            );

        });

        let status;

        if (winner) {
            status = 'Winner: ' + current.squares[winner[0]];
        } else {
            const endGame = current.squares.includes(null) ? false : true;

            if (endGame) {
                status = 'The game draw';
            } else {
                status = 'The next player is ' + (this.state.xIsNext ? 'X' : 'O');
            }
        }

        return (
            <div className="game">
                <div className="game-board">
                    <Board squares={current.squares}
                           onClick={(i) => this.handleClick(i)}
                           winner={winner}
                    />
                </div>
                <div className="game-info">
                <div>{ status }</div>
                <ol> <button onClick={() => {this.toogle()}}> Toogle</button> </ol>
                <ol>{ moves } </ol>
                </div>
            </div>
        );
    }
}


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
            //return squares[a];
            return lines[i];
        }
    }

    return null;
}

function getXPos(index) {
    let xPos = index % 3;

    if (xPos === 0) {
        xPos = 3;
    }

    return xPos;
}

function getYPos(index) {
    return Math.ceil(index/3);
}

function getPos(index) {
    return 'X:' + getXPos(index) + ' Y:' + getYPos(index);
}
```

:top: [về đầu trang](#home)

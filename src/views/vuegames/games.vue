<template>
  <div id="main"> 
		<h1>TIC TAC TOE</h1> 
		<p id="ins"> 
			Game starts by just Tap on 
			box<br><br>First Player starts as 
			<b>Player X </b>And Second Player as 
			<b>Player 0</b> 
		</p> 
		<br><br> 
		<div class = "ui"> 
			<div class="row"> 
				<input type="text" id= "b1"
					class="cell" @click="myfunc_3(); myfunc();"
					readonly> 
				<input type="text" id= "b2"
					class="cell" @click="myfunc_4(); myfunc();"
					readonly> 
				<input type="text" id= "b3" class="cell"
					@click="myfunc_5(); myfunc();"
					readonly> 
			</div> 
			<div class="row"> 
				<input type="text" id= "b4"
					class="cell" @click="myfunc_6(); myfunc();"
					readonly> 
				<input type="text" id= "b5"
					class="cell" @click="myfunc_7(); myfunc();"
					readonly> 
				<input type="text" id= "b6"
					class="cell" @click="myfunc_8(); myfunc();"
					readonly> 
			</div> 
			<div class="row"> 
				<input type="text" id= "b7"
					class="cell" @click="myfunc_9(); myfunc();"
					readonly> 
				<input type="text" id= "b8"
					class="cell" @click="myfunc_10();myfunc();"
					readonly> 
				<input type="text" id= "b9"
					class="cell" @click="myfunc_11();myfunc();"
					readonly> 
			</div> 
		</div> 
		<br><br><br> 
		
		<button id="but" @click="myfunc_2()"> 
			RESET 
		</button> 
		<br><br> 
		<p id="print"></p> 
	</div>
</template>

  <script>
    export default {
      data(){
        return{
          flag: 1,
        }
      },
      methods: {
        // Function called whenever user tab on any box 
        myfunc() { 
        // Setting DOM to all boxes or input field 
        var b1, b2, b3, b4, b5, b6, b7, b8, b9; 
        b1 = document.getElementById("b1").value; 
        b2 = document.getElementById("b2").value; 
        b3 = document.getElementById("b3").value; 
        b4 = document.getElementById("b4").value; 
        b5 = document.getElementById("b5").value; 
        b6 = document.getElementById("b6").value; 
        b7 = document.getElementById("b7").value; 
        b8 = document.getElementById("b8").value; 
        b9 = document.getElementById("b9").value; 

        var b1btn, b2btn, b3btn, b4btn, b5btn, 
          b6btn, b7btn, b8btn, b9btn; 
          
        b1btn = document.getElementById("b1"); 
        b2btn = document.getElementById("b2"); 
        b3btn = document.getElementById("b3"); 
        b4btn = document.getElementById("b4"); 
        b5btn = document.getElementById("b5"); 
        b6btn = document.getElementById("b6"); 
        b7btn = document.getElementById("b7"); 
        b8btn = document.getElementById("b8"); 
        b9btn = document.getElementById("b9"); 

        // Checking if Player X won or not and after 
        // that disabled all the other fields 
        if ((b1 == 'x' || b1 == 'X') && (b2 == 'x' || 
          b2 == 'X') && (b3 == 'x' || b3 == 'X')) { 
          document.getElementById('print') 
            .innerHTML = "Player X won"; 
          b4btn.disabled = true; 
          b5btn.disabled = true; 
          b6btn.disabled = true; 
          b7btn.disabled = true; 
          b8btn.disabled = true; 
          b9btn.disabled = true; 

          b1btn.style.color = "red"; 
          b2btn.style.color = "red"; 
          b3btn.style.color = "red"; 
        } 
        else if ((b1 == 'x' || b1 == 'X') && (b4 == 'x' || 
          b4 == 'X') && (b7 == 'x' || b7 == 'X')) { 
          document.getElementById('print') 
            .innerHTML = "Player X won"; 
          b2btn.disabled = true; 
          b3btn.disabled = true; 
          b5btn.disabled = true; 
          b6btn.disabled = true; 
          b8btn.disabled = true; 
          b9btn.disabled = true; 

          b1btn.style.color = "red"; 
          b4btn.style.color = "red"; 
          b7btn.style.color = "red"; 
        } 
        else if ((b7 == 'x' || b7 == 'X') && (b8 == 'x' || 
          b8 == 'X') && (b9 == 'x' || b9 == 'X')) { 
          document.getElementById('print') 
            .innerHTML = "Player X won"; 

          b1btn.disabled = true; 
          b2btn.disabled = true; 
          b3btn.disabled = true; 
          b4btn.disabled = true; 
          b5btn.disabled = true; 
          b6btn.disabled = true; 

          b7btn.style.color = "red"; 
          b8btn.style.color = "red"; 
          b9btn.style.color = "red"; 
        } 
        else if ((b3 == 'x' || b3 == 'X') && (b6 == 'x' || 
          b6 == 'X') && (b9 == 'x' || b9 == 'X')) { 
          document.getElementById('print') 
            .innerHTML = "Player X won"; 

          b1btn.disabled = true; 
          b2btn.disabled = true; 
          b4btn.disabled = true; 
          b5btn.disabled = true; 
          b7btn.disabled = true; 
          b8btn.disabled = true; 

          b3btn.style.color = "red"; 
          b6btn.style.color = "red"; 
          b9btn.style.color = "red"; 
        } 
        else if ((b1 == 'x' || b1 == 'X') && (b5 == 'x' || 
          b5 == 'X') && (b9 == 'x' || b9 == 'X')) { 
          document.getElementById('print') 
            .innerHTML = "Player X won"; 
          b2btn.disabled = true; 
          b3btn.disabled = true; 
          b4btn.disabled = true; 
          b6btn.disabled = true; 
          b7btn.disabled = true; 
          b8btn.disabled = true; 

          b1btn.style.color = "red"; 
          b5btn.style.color = "red"; 
          b9btn.style.color = "red"; 
        } 
        else if ((b3 == 'x' || b3 == 'X') && (b5 == 'x' || 
          b5 == 'X') && (b7 == 'x' || b7 == 'X')) { 
          document.getElementById('print') 
            .innerHTML = "Player X won"; 
          b1btn.disabled = true; 
          b2btn.disabled = true; 
          b4btn.disabled = true; 
          b6btn.disabled = true; 
          b8btn.disabled = true; 
          b9btn.disabled = true; 

          b3btn.style.color = "red"; 
          b5btn.style.color = "red"; 
          b7btn.style.color = "red"; 
        } 
        else if ((b2 == 'x' || b2 == 'X') && (b5 == 'x' || 
          b5 == 'X') && (b8 == 'x' || b8 == 'X')) { 
          document.getElementById('print') 
            .innerHTML = "Player X won"; 
          b1btn.disabled = true; 
          b2btn.disabled = true; 
          b4btn.disabled = true; 
          b6btn.disabled = true; 
          b7btn.disabled = true; 
          b9btn.disabled = true; 

          b2btn.style.color = "red"; 
          b5btn.style.color = "red"; 
          b8btn.style.color = "red"; 
        } 
        else if ((b4 == 'x' || b4 == 'X') && (b5 == 'x' || 
          b5 == 'X') && (b6 == 'x' || b6 == 'X')) { 
          document.getElementById('print') 
            .innerHTML = "Player X won"; 
          b1btn.disabled = true; 
          b2btn.disabled = true; 
          b3btn.disabled = true; 
          b7btn.disabled = true; 
          b8btn.disabled = true; 
          b9btn.disabled = true; 

          b4btn.style.color = "red"; 
          b5btn.style.color = "red"; 
          b6btn.style.color = "red"; 
        } 

        // Checking of Player X finish 
        // Checking for Player 0 starts, Is player 0 won or 
        // not and after that disabled all the other fields 
        else if ((b1 == '0' || b1 == '0') && (b2 == '0' || 
          b2 == '0') && (b3 == '0' || b3 == '0')) { 
          document.getElementById('print') 
            .innerHTML = "Player 0 won"; 
          b4btn.disabled = true; 
          b5btn.disabled = true; 
          b6btn.disabled = true; 
          b7btn.disabled = true; 
          b8btn.disabled = true; 
          b9btn.disabled = true; 

          b1btn.style.color = "red"; 
          b2btn.style.color = "red"; 
          b3btn.style.color = "red"; 
        } 
        else if ((b1 == '0' || b1 == '0') && (b4 == '0' || 
          b4 == '0') && (b7 == '0' || b7 == '0')) { 
          document.getElementById('print') 
            .innerHTML = "Player 0 won"; 
          b2btn.disabled = true; 
          b3btn.disabled = true; 
          b5btn.disabled = true; 
          b6btn.disabled = true; 
          b8btn.disabled = true; 
          b9btn.disabled = true; 

          b1btn.style.color = "red"; 
          b4btn.style.color = "red"; 
          b7btn.style.color = "red"; 
        } 
        else if ((b7 == '0' || b7 == '0') && (b8 == '0' || 
          b8 == '0') && (b9 == '0' || b9 == '0')) { 
          document.getElementById('print') 
            .innerHTML = "Player 0 won"; 
          b1btn.disabled = true; 
          b2btn.disabled = true; 
          b3btn.disabled = true; 
          b4btn.disabled = true; 
          b5btn.disabled = true; 
          b6btn.disabled = true; 

          b7btn.style.color = "red"; 
          b8btn.style.color = "red"; 
          b9btn.style.color = "red"; 
        } 
        else if ((b3 == '0' || b3 == '0') && (b6 == '0' || 
          b6 == '0') && (b9 == '0' || b9 == '0')) { 
          document.getElementById('print') 
            .innerHTML = "Player 0 won"; 
          b1btn.disabled = true; 
          b2btn.disabled = true; 
          b4btn.disabled = true; 
          b5btn.disabled = true; 
          b7btn.disabled = true; 
          b8btn.disabled = true; 
          b3btn.style.color = "red"; 
          b6btn.style.color = "red"; 
          b9btn.style.color = "red"; 
        } 
        else if ((b1 == '0' || b1 == '0') && (b5 == '0' || 
          b5 == '0') && (b9 == '0' || b9 == '0')) { 
          document.getElementById('print') 
            .innerHTML = "Player 0 won"; 
          b2btn.disabled = true; 
          b3btn.disabled = true; 
          b4btn.disabled = true; 
          b6btn.disabled = true; 
          b7btn.disabled = true; 
          b8btn.disabled = true; 

          b1btn.style.color = "red"; 
          b5btn.style.color = "red"; 
          b9btn.style.color = "red"; 
        } 
        else if ((b3 == '0' || b3 == '0') && (b5 == '0' || 
          b5 == '0') && (b7 == '0' || b7 == '0')) { 
          document.getElementById('print') 
            .innerHTML = "Player 0 won"; 
          b1btn.disabled = true; 
          b2btn.disabled = true; 
          b4btn.disabled = true; 
          b6btn.disabled = true; 
          b8btn.disabled = true; 
          b9btn.disabled = true; 

          b3btn.style.color = "red"; 
          b5btn.style.color = "red"; 
          b7btn.style.color = "red"; 
        } 
        else if ((b2 == '0' || b2 == '0') && (b5 == '0' || 
          b5 == '0') && (b8 == '0' || b8 == '0')) { 
          document.getElementById('print') 
            .innerHTML = "Player 0 won"; 
          b1btn.disabled = true; 
          b3btn.disabled = true; 
          b4btn.disabled = true; 
          b6btn.disabled = true; 
          b7btn.disabled = true; 
          b9btn.disabled = true; 

          b2btn.style.color = "red"; 
          b5btn.style.color = "red"; 
          b8btn.style.color = "red"; 
        } 
        else if ((b4 == '0' || b4 == '0') && (b5 == '0' || 
          b5 == '0') && (b6 == '0' || b6 == '0')) { 
          document.getElementById('print') 
            .innerHTML = "Player 0 won"; 
          b1btn.disabled = true; 
          b2btn.disabled = true; 
          b3btn.disabled = true; 
          b7btn.disabled = true; 
          b8btn.disabled = true; 
          b9btn.disabled = true; 

          b4btn.style.color = "red"; 
          b5btn.style.color = "red"; 
          b6btn.style.color = "red"; 
        } 

        // Checking of Player 0 finish 
        // Here, Checking about Tie 
        else if ((b1 == 'X' || b1 == '0') && (b2 == 'X'
          || b2 == '0') && (b3 == 'X' || b3 == '0') && 
          (b4 == 'X' || b4 == '0') && (b5 == 'X' || 
            b5 == '0') && (b6 == 'X' || b6 == '0') && 
          (b7 == 'X' || b7 == '0') && (b8 == 'X' || 
            b8 == '0') && (b9 == 'X' || b9 == '0')) { 
          document.getElementById('print') 
            .innerHTML = "Match Tie"; 
        } 
        else { 

          // Here, Printing Result 
          if (this.flag == 1) { 
            document.getElementById('print') 
              .innerHTML = "Player X Turn"; 
          } 
          else { 
            document.getElementById('print') 
              .innerHTML = "Player 0 Turn"; 
          } 
        } 
        },

        // Function to reset game 
        myfunc_2() { 
        location.reload(); 
        b1 = b2 = b3 = b4 = b5 = b6 = b7 = b8 = b9 = ''; 
        },

        // Here onwards, functions check turn of the player 
        // and put accordingly value X or 0 
        
        myfunc_3() { 
        if (this.flag == 1) { 
          document.getElementById("b1").value = "X"; 
          document.getElementById("b1").disabled = true; 
          this.flag = 0; 
        } 
        else { 
          document.getElementById("b1").value = "0"; 
          document.getElementById("b1").disabled = true; 
          this.flag = 1; 
        } 
        },

        myfunc_4() { 
        if (this.flag == 1) { 
          document.getElementById("b2").value = "X"; 
          document.getElementById("b2").disabled = true; 
          this.flag = 0; 
        } 
        else { 
          document.getElementById("b2").value = "0"; 
          document.getElementById("b2").disabled = true; 
          this.flag = 1; 
        } 
        }, 

        myfunc_5() { 
        if (this.flag == 1) { 
          document.getElementById("b3").value = "X"; 
          document.getElementById("b3").disabled = true; 
          this.flag = 0; 
        } 
        else { 
          document.getElementById("b3").value = "0"; 
          document.getElementById("b3").disabled = true; 
          this.flag = 1; 
        } 
        },

        myfunc_6() { 
        if (this.flag == 1) { 
          document.getElementById("b4").value = "X"; 
          document.getElementById("b4").disabled = true; 
          this.flag = 0; 
        } 
        else { 
          document.getElementById("b4").value = "0"; 
          document.getElementById("b4").disabled = true; 
          this.flag = 1; 
        } 
        },

        myfunc_7() { 
        if (this.flag == 1) { 
          document.getElementById("b5").value = "X"; 
          document.getElementById("b5").disabled = true; 
          this.flag = 0; 
        } 
        else { 
          document.getElementById("b5").value = "0"; 
          document.getElementById("b5").disabled = true; 
          this.flag = 1; 
        } 
        },

        myfunc_8() { 
        if (this.flag == 1) { 
          document.getElementById("b6").value = "X"; 
          document.getElementById("b6").disabled = true; 
          this.flag = 0; 
        } 
        else { 
          document.getElementById("b6").value = "0"; 
          document.getElementById("b6").disabled = true; 
          this.flag = 1; 
        } 
        },

        myfunc_9() { 
        if (this.flag == 1) { 
          document.getElementById("b7").value = "X"; 
          document.getElementById("b7").disabled = true; 
          this.flag = 0; 
        } 
        else { 
          document.getElementById("b7").value = "0"; 
          document.getElementById("b7").disabled = true; 
          this.flag = 1; 
        } 
        },

        myfunc_10() { 
        if (this.flag == 1) { 
          document.getElementById("b8").value = "X"; 
          document.getElementById("b8").disabled = true; 
          this.flag = 0; 
        } 
        else { 
          document.getElementById("b8").value = "0"; 
          document.getElementById("b8").disabled = true; 
          this.flag = 1; 
        } 
        },

        myfunc_11() { 
        if (this.flag == 1) { 
          document.getElementById("b9").value = "X"; 
          document.getElementById("b9").disabled = true; 
          this.flag = 0; 
        } 
        else { 
          document.getElementById("b9").value = "0"; 
          document.getElementById("b9").disabled = true; 
          this.flag = 1; 
        } 
        },
      mounted() {
        this.tetris = {
          board: [],
          boardDiv: null,
          canvas: null,
          pSize: 20,
          canvasHeight: 440,
          canvasWidth: 200,
          boardHeight: 0,
          boardWidth: 0,
          spawnX: 4,
          spawnY: 1,
          shapes: [
            [
              [-1, 1],
              [0, 1],
              [1, 1],
              [0, 0], //TEE
            ],
            [
              [-1, 0],
              [0, 0],
              [1, 0],
              [2, 0], //line
            ],
            [
              [-1, -1],
              [-1, 0],
              [0, 0],
              [1, 0], //L EL
            ],
            [
              [1, -1],
              [-1, 0],
              [0, 0],
              [1, 0], //R EL
            ],
            [
              [0, -1],
              [1, -1],
              [-1, 0],
              [0, 0], // R ess
            ],
            [
              [-1, -1],
              [0, -1],
              [0, 0],
              [1, 0], //L ess
            ],
            [
              [0, -1],
              [1, -1],
              [0, 0],
              [1, 0], //square
            ],
          ],
          tempShapes: null,
          curShape: null,
          curShapeIndex: null,
          curX: 0,
          curY: 0,
          curSqs: [],
          nextShape: null,
          nextShapeDisplay: null,
          nextShapeIndex: null,
          sqs: [],
          score: 0,
          scoreDisplay: null,
          level: 1,
          levelDisplay: null,
          numLevels: 10,
          time: 0,
          maxTime: 1000,
          timeDisplay: null,
          isActive: 0,
          curComplete: false,
          timer: null,
          sTimer: null,
          speed: 700,
          lines: 0,
      
          init: function () {
            this.isStart = true;
            this.canvas = document.getElementById('canvas');
            this.initBoard();
            this.initInfo();
            this.initLevelScores();
            this.initShapes();
            this.bindKeyEvents();
            this.play();
          },
          initBoard: function () {
            this.boardHeight = this.canvasHeight / this.pSize;
            this.boardWidth = this.canvasWidth / this.pSize;
            var s = this.boardHeight * this.boardWidth;
            for (var i = 0; i < s; i++) {
              this.board.push(0);
            }
            //this.boardDiv = document.getElementById('board); //for debugging
          },
          initInfo: function () {
            this.nextShapeDisplay = document.getElementById('next_shape');
            this.levelDisplay = document
              .getElementById('level')
              .getElementsByTagName('span')[0];
            this.timeDisplay = document
              .getElementById('time')
              .getElementsByTagName('span')[0];
            this.scoreDisplay = document
              .getElementById('score')
              .getElementsByTagName('span')[0];
            this.linesDisplay = document
              .getElementById('lines')
              .getElementsByTagName('span')[0];
            this.setInfo('time');
            this.setInfo('score');
            this.setInfo('level');
            this.setInfo('lines');
          },
          initShapes: function () {
            this.curSqs = [];
            this.curComplete = false;
            this.shiftTempShapes();
            this.curShapeIndex = this.tempShapes[0];
            this.curShape = this.shapes[this.curShapeIndex];
            this.initNextShape();
            this.setCurCoords(this.spawnX, this.spawnY);
            this.drawShape(this.curX, this.curY, this.curShape);
          },
          initNextShape: function () {
            if (typeof this.tempShapes[1] === 'undefined') {
              this.initTempShapes();
            }
            try {
              this.nextShapeIndex = this.tempShapes[1];
              this.nextShape = this.shapes[this.nextShapeIndex];
              this.drawNextShape();
            } catch (e) {
              throw new Error('Could not create next shape. ' + e);
            }
          },
          initTempShapes: function () {
            this.tempShapes = [];
            for (var i = 0; i < this.shapes.length; i++) {
              this.tempShapes.push(i);
            }
            var k = this.tempShapes.length;
            while (--k) {
              //Fisher Yates Shuffle
              var j = Math.floor(Math.random() * (k + 1));
              var tempk = this.tempShapes[k];
              var tempj = this.tempShapes[j];
              this.tempShapes[k] = tempj;
              this.tempShapes[j] = tempk;
            }
          },
          shiftTempShapes: function () {
            try {
              if (
                typeof this.tempShapes === 'undefined' ||
                this.tempShapes === null
              ) {
                this.initTempShapes();
              } else {
                this.tempShapes.shift();
              }
            } catch (e) {
              throw new Error('Could not shift or init tempShapes: ' + e);
            }
          },
          initTimer: function () {
            var me = this;
            var tLoop = function () {
              me.incTime();
              me.timer = setTimeout(tLoop, 2000);
            };
            this.timer = setTimeout(tLoop, 2000);
          },
          initLevelScores: function () {
            var c = 1;
            for (var i = 1; i <= this.numLevels; i++) {
              this['level' + i] = [c * 1000, 40 * i, 5 * i]; //for nxt level, row score, p sore,
              c = c + c;
            }
          },
          setInfo: function (el) {
            this[el + 'Display'].innerHTML = this[el];
          },
          drawNextShape: function () {
            var ns = [];
            for (var i = 0; i < this.nextShape.length; i++) {
              ns[i] = this.createSquare(
                this.nextShape[i][0] + 2,
                this.nextShape[i][1] + 2,
                this.nextShapeIndex
              );
            }
            this.nextShapeDisplay.innerHTML = '';
            for (var k = 0; k < ns.length; k++) {
              this.nextShapeDisplay.appendChild(ns[k]);
            }
          },
          drawShape: function (x, y, p) {
            for (var i = 0; i < p.length; i++) {
              var newX = p[i][0] + x;
              var newY = p[i][1] + y;
              this.curSqs[i] = this.createSquare(newX, newY, this.curShapeIndex);
            }
            for (var k = 0; k < this.curSqs.length; k++) {
              this.canvas.appendChild(this.curSqs[k]);
            }
          },
          createSquare: function (x, y, type) {
            var el = document.createElement('div');
            el.className = 'square type' + type;
            el.style.left = x * this.pSize + 'px';
            el.style.top = y * this.pSize + 'px';
            return el;
          },
          removeCur: function () {
            var me = this;
            this.curSqs.forEach(function (item) {
              me.canvas.removeChild(item);
            });
            this.curSqs = [];
          },
          setCurCoords: function (x, y) {
            this.curX = x;
            this.curY = y;
          },
          bindKeyEvents: function () {
            var me = this;
            var event = 'keypress';
            if (this.isSafari() || this.isIE()) {
              event = 'keydown';
            }
            var cb = function (e) {
              me.handleKey(e);
            };
            if (window.addEventListener) {
              document.addEventListener(event, cb, false);
            } else {
              document.attachEvent('on' + event, cb);
            }
          },
          handleKey: function (e) {
            var c = this.whichKey(e);
            var dir = '';
            switch (c) {
              case 37:
                this.move('L');
                break;
              case 38:
                this.move('RT');
                break;
              case 39:
                this.move('R');
                break;
              case 40:
                this.move('D');
                break;
              case 27: //esc: pause
                this.togglePause();
                break;
              default:
                break;
            }
          },
          whichKey: function (e) {
            var c;
            if (window.event) {
              c = window.event.keyCode;
            } else if (e) {
              c = e.keyCode;
            }
            return c;
          },
          incTime: function () {
            this.time++;
            this.setInfo('time');
          },
          incScore: function (amount) {
            this.score = this.score + amount;
            this.setInfo('score');
          },
          incLevel: function () {
            this.level++;
            this.speed = this.speed - 75;
            this.setInfo('level');
          },
          incLines: function (num) {
            this.lines += num;
            this.setInfo('lines');
          },
          calcScore: function (args) {
            var lines = args.lines || 0;
            var shape = args.shape || false;
            var speed = args.speed || 0;
            var score = 0;
      
            if (lines > 0) {
              score += lines * this['level' + this.level][1];
              this.incLines(lines);
            }
            if (shape === true) {
              score += shape * this['level' + this.level][2];
            }
            /*if (speed > 0){ score += speed * this["level" +this .level[3]];}*/
            this.incScore(score);
          },
          checkScore: function () {
            if (this.score >= this['level' + this.level][0]) {
              this.incLevel();
            }
          },
          gameOver: function () {
            this.clearTimers();
            this.isStart = false;
            this.canvas.innerHTML = '<h1>GAME OVER</h1>';
          },
          play: function () {
            var me = this;
            if (this.timer === null) {
              this.initTimer();
            }
            var gameLoop = function () {
              me.move('D');
              if (me.curComplete) {
                me.markBoardShape(me.curX, me.curY, me.curShape);
                me.curSqs.forEach(function () {
                  me.sqs.push(this);
                });
                me.calcScore({ shape: true });
                me.checkRows();
                me.checkScore();
                me.initShapes();
                me.play();
              } else {
                me.pTimer = setTimeout(gameLoop, me.speed);
              }
            };
            this.pTimer = setTimeout(gameLoop, me.speed);
            this.isActive = 1;
          },
          togglePause: function () {
            if (this.isActive === 1) {
              this.clearTimers();
              this.isActive = 0;
            } else {
              this.play();
            }
          },
          clearTimers: function () {
            clearTimeout(this.timer);
            clearTimeout(this.pTimer);
            this.timer = null;
            this.pTimer = null;
          },
          move: function (dir) {
            var s = '';
            var me = this;
            var tempX = this.curX;
            var tempY = this.curY;
            switch (dir) {
              case 'L':
                s = 'left';
                tempX -= 1;
                break;
              case 'R':
                s = 'left';
                tempX += 1;
                break;
              case 'D':
                s = 'top';
                tempY += 1;
                break;
              case 'RT':
                this.rotate();
                return true;
                break;
              default:
                throw new Error('wtf');
                break;
            }
            if (this.checkMove(tempX, tempY, this.curShape)) {
              this.curSqs.forEach(function (i) {
                var l = parseInt(i.style[s], 10);
                dir === 'L' ? (l -= me.pSize) : (l += me.pSize);
                i.style[s] = l + 'px';
              });
              this.curX = tempX;
              this.curY = tempY;
            } else if (dir === 'D') {
              if (this.curY === 1 || this.time === this.maxTime) {
                this.gameOver();
                return false;
              }
              this.curComplete = true;
            }
          },
          rotate: function () {
            if (this.curShapeIndex !== 6) {
              //square
              var temp = [];
              this.curShape.forEach(function (item) {
                temp.push([item[1] * -1, item[0]]);
              });
              if (this.checkMove(this.curX, this.curY, temp)) {
                this.curShape = temp;
                this.removeCur();
                this.drawShape(this.curX, this.curY, this.curShape);
              } else {
                throw new Error('Could not rotate!');
              }
            }
          },
          checkMove: function (x, y, p) {
            if (this.isOB(x, y, p) || this.isCollision(x, y, p)) {
              return false;
            }
            return true;
          },
          isCollision: function (x, y, p) {
            var me = this;
            var bool = false;
            p.forEach(function (item) {
              var newX = item[0] + x;
              var newY = item[1] + y;
              if (me.boardPos(newX, newY) === 1) {
                bool = true;
              }
            });
            return bool;
          },
          isOB: function (x, y, p) {
            var w = this.boardWidth - 1;
            var h = this.boardHeight - 1;
            var bool = false;
            p.forEach(function (item) {
              var newX = item[0] + x;
              var newY = item[1] + y;
              if (newX < 0 || newX > w || newY < 0 || newY > h) {
                bool = true;
              }
            });
            return bool;
          },
          getRowState: function (y) {
            var c = 0;
            for (var x = 0; x < this.boardWidth; x++) {
              if (this.boardPos(x, y) === 1) {
                c = c + 1;
              }
            }
            if (c === 0) {
              return 'E';
            }
            if (c === this.boardWidth) {
              return 'F';
            }
            return 'U';
          },
          checkRows: function () {
            var me = this;
            var start = this.boardHeight;
            this.curShape.forEach(function (item) {
              var n = item[1] + me.curY;
              console.log(n);
              if (n < start) {
                start = n;
              }
            });
            console.log(start);
      
            var c = 0;
            var stopCheck = false;
            for (var y = this.boardHeight - 1; y >= 0; y--) {
              switch (this.getRowState(y)) {
                case 'F':
                  this.removeRow(y);
                  c++;
                  break;
                case 'E':
                  if (c === 0) {
                    stopCheck = true;
                  }
                  break;
                case 'U':
                  if (c > 0) {
                    this.shiftRow(y, c);
                  }
                  break;
                default:
                  break;
              }
              if (stopCheck === true) {
                break;
              }
            }
            if (c > 0) {
              this.calcScore({ lines: c });
            }
          },
          shiftRow: function (y, amount) {
            var me = this;
            for (var x = 0; x < this.boardWidth; x++) {
              this.sqs.forEach(function () {
                if (me.isAt(x, y, this)) {
                  me.setBlock(x, y + amount, this);
                }
              });
            }
            me.emptyBoardRow(y);
          },
          emptyBoardRow: function (y) {
            for (var x = 0; x < this.boardWidth; x++) {
              this.markBoardAt(x, y, 0);
            }
          },
          removeRow: function (y) {
            for (var x = 0; x < this.boardWidth; x++) {
              this.removeBlock(x, y);
            }
          },
          removeBlock: function (x, y) {
            var me = this;
            this.markBoardAt(x, y, 0);
            this.sqs.forEach(function (i) {
              if (me.getPos(this)[0] === x && me.getPos(this)[1] === y) {
                me.canvas.removeChild(me);
                me.sqs.splice(i, 1);
              }
            });
          },
          setBlock: function (x, y, block) {
            this.markBoardAt(x, y, 1);
            var newX = x * this.pSize;
            var newY = y * this.pSize;
            block.style.left = newX + 'px';
            block.style.top = newY + 'px';
          },
          isAt: function (x, y, block) {
            if (this.getPos(block)[0] === x && this.getPos(block)[1] === y) {
              return true;
            }
            return false;
          },
          getPos: function (block) {
            var p = [];
            p.push(parseInt(block.style.left, 10) / this.pSize);
            p.push(parseInt(block.style.top, 10) / this.pSize);
            return p;
          },
          getBoardIdx: function (x, y) {
            return x + y * this.boardWidth;
          },
          boardPos: function (x, y) {
            return this.board[x + y * this.boardWidth];
          },
          markBoardAt: function (x, y, val) {
            this.board[this.getBoardIdx(x, y)] = val;
          },
          markBoardShape: function (x, y, p) {
            var me = this;
            p.forEach(function (i) {
              var newX = p[i] && p[i][0] !== undefined ? p[i][0] + x : x;
              var newY = p[i] && p[i][1] !== undefined ? p[i][1] + y : y;

              me.markBoardAt(newX, newY, 1);
            });
          },
          isIE: function () {
            return this.bTest(/IE/);
          },
          isFirefox: function () {
            return this.bTest(/Firefox/);
          },
          isSafari: function () {
            return this.bTest(/Safari/);
          },
          bTest: function (rgx) {
            return rgx.test(navigator.userAgent);
          },
        };

        this.$nextTick(() => {
          const btn = this.$refs.startButton;
          btn.addEventListener('click', this.startGame);
        });
      },
      }
    };
    </script>
  
  <style scoped>
  h1 { 
	color: orangered; 
	margin-bottom: -5px; 
} 
p { 
	margin-bottom: -10px; 
} 
.ui { 
	display: flex; 
	flex-direction: column; 
	align-items: center; 
} 
.row { 
	display: flex; 
} 
.cell { 
	border: none; 
	width: 80px; 
	height: 80px; 
	display: flex; 
	align-items: center; 
	justify-content: center; 
	font-size: 24px; 
	text-align: center; 
	cursor: pointer; 
} 
.cell:active { 
	outline: none; 
} 
/* 3*3 Grid */
#b1{ 
	border-bottom: 1px solid gray; 
	border-right: 1px solid gray; 
} 

#b2 { 
	border-bottom: 1px solid gray; 
	border-right: 1px solid gray; 
	border-left: 1px solid gray; 
} 

#b3 { 
	border-bottom: 1px solid gray; 
	border-left: 1px solid gray; 
} 

#b4 { 
	border-top: 1px solid gray; 
	border-bottom: 1px solid gray; 
	border-right: 1px solid gray; 
} 
	
#b5 { 
	border: 1px solid gray; 
} 

#b6 { 
	border-top: 1px solid gray; 
	border-bottom: 1px solid gray; 
	border-left: 1px solid gray; 
} 

#b7 { 
	border-top: 1px solid gray; 
	border-right: 1px solid gray; 
} 

#b8 { 
	border-top: 1px solid gray; 
	border-right: 1px solid gray; 
	border-left: 1px solid gray; 
} 

#b9 { 
	border-top: 1px solid gray; 
	border-left: 1px solid gray; 
} 
/* Reset Button */
#but { 
	box-sizing: border-box; 
	width: 95px; 
	height: 40px; 
	border: 1px solid dodgerblue; 
	margin-left: auto; 
	border-radius: 8px; 
	font-family: Verdana, 
		Geneva, Tahoma, sans-serif; 

	background-color: whitesmoke; 
	color: dodgerblue; 
	font-size: 20px; 
	cursor: pointer; 
} 

/* Player turn space */
#print { 
	font-family: Verdana, 
		Geneva, Tahoma, sans-serif; 
	color: dodgerblue; 
	font-size: 20px; 
} 

/* Main Container */
#main { 
	text-align: center; 
} 

/* Game Instruction Text */
#ins { 
	font-family: Verdana,Geneva, 
					Tahoma, sans-serif; 
	color: dodgerblue; 
}

  </style>
  
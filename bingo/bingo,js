function generateBoard() {
    var bingoNumbers = [];
    var min = 1;
    var max = 75;

    // Preencher array com números de 1 a 75
    for (var i = min; i <= max; i++) {
        bingoNumbers.push(i);
    }

    // Embaralhar os números
    for (var i = bingoNumbers.length - 1; i > 0; i--) {
        var j = Math.floor(Math.random() * (i + 1));
        var temp = bingoNumbers[i];
        bingoNumbers[i] = bingoNumbers[j];
        bingoNumbers[j] = temp;
    }

    var board = document.getElementById("bingo-board");
    board.innerHTML = "";

    var counter = 0;
    for (var i = 0; i < 5; i++) {
        var row = document.createElement("tr");
        for (var j = 0; j < 5; j++) {
            var cell = document.createElement("td");
            cell.textContent = bingoNumbers[counter++];
            row.appendChild(cell);
        }
        board.appendChild(row);
    }
}
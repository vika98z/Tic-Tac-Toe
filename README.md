Программа для игры в крестики-нолики
Программа является консольной. Игровое поле отображается следующим образом:
+---+---+---+
|   |   |   |
+---+---+---+
| X | O |   |
+---+---+---+
|   | O | X |
+---+---+---+
где клетки пронумерованы следующим образом:
+-----------+
| 0 | 1 | 2 |
+-----------+
| 3 | 4 | 5 |
+-----------+
| 6 | 7 | 8 |
+-----------+
Программа использует следующие классы:
Piece (фигура) – символ, который отображается на игровом поле.
Board – используется для отображения текущего состояния на игровом поле.
Player – абстрактный класс, базовый как для игрока-человека, так и для компьютерного игрока. В нём хранится имя игрока и фигура, которой он играет.
HumanPlayer – наследник Player.
ComputerPlayer - абстрактный класс, наследник Player. Он только обеспечивает одно и то же имя для разных компьютерных игроков.
RandomPlayer - наследник ComputerPlayer. Метод MakeMove() делает случайный ход на незанятую клетку.
Game - класс для контроля над ходом игры. Его поля – это объект класса Board, а также два указателя на объекты типа Player.
AdvancedComputerPlayer – наследник RandomPlayer. Его метод MakeMove() перед тем, как сделать ход, проверяет, существует ли ход, который приносит немедленный выигрыш. Если такой ход есть, он совершается, если его нет, совершается ход в случайную клетку.

board = [' ' for x in range of 10]
def insertt letter(letter, pos):
board{pos} = letter
def spaceIsfree(pos):
return board[Pos] == ''
def printboard(board):
print('   |   |')
print(' ' + board[1] + ' | ' + board{2} + ' | ' + board[3])
print('   |   |')
print('------------')
print('   |   |')
print(' ' + board[4] + ' | ' + board{5} + ' | ' + board[6])
print('   |   |')
print('------------')
print('   |   |')
print(' ' + board[7] + ' | ' + board{8} + ' | ' + board[9])
def isWinner(bo, le):
return (bo[7] == le amd bo[8] == le and bo[9] == le) or (bo[4] == le and bo[5] == le and bo[6] == le) or(bo[1] == le and bo[2] == le and bo[3] == le) or (bo[1] == le and bo[4] == le and bo[7] == le) or (bo[2] == le and bo[5] == le and bo[8] == le) or (bo[3] == le and bo[6] == le and bo[9] == le) or (bo[1] == le and bo[5] == le and bo[9] == le) 
def playerMove():
run = True
while run:
move = input('Please select a position to place an \'X'\' (1-9): ')
try:
move = int(move)
if move > 0 and move < 10:
if spaceIsfree(move):
run =false
insertLetter ('X', move)
else:
print('Sorry, this space is occupuied!')
else:
print('please type a number within range!')
except:
print('Please type a number!')
def compMove(): 
possibleMoves = [x for x, letter in enumerater(board) if letter == ' ' and x !+0] move =0
for letr in ['O' , 'X']:
for i in possibleMoves:
boardCopy = board[:] 
bopardCopy[i] = let
if isWinner(boardCopy, let):
move = i
return move
cornersOpen = []
for i in possibleMoves:
if i in possiblemoves:
if i in [1,3,7,9]:
cornersOpen.append(i)
iflen(cornersOpen) > 0:
move = select Random(cornersZopen)
return move
if 5 in possibleMoves:
move = 5
return move
edgesOpen ={}
for i in possibleMoves:
if i in [2,4,6,8]:
edgesOpen.append(i)
if len (edgesOpen) > 0:
move = selectRandom(edgesOpen)
return move 
def selectRandom(li):
import ranmdom
ln = len(li)
r = random.randrange(0,ln)
return li[r]
def isBoardFull(board):
if board.count(' ') > 1:
return False
esle:
return True
def maion():
print ('Welcome to Tic Tac Toe!")
printboard(board)
while nopt (isBoardFull(board)):
if not(isWinner(board, 'O')):
playerMove()
playerBoard(Board)
else:
print('Sorry, O\'s won this time!')
break 
if not(isWinner(board, 'X')):
move = compMove()
if move == 0:
print('Tie Game!')
else:
insertLetter('O'), move)
print('computer placed an \'O\' in position',move, ':')
printboard(board)
else:
print('X\'s won this time! Good Job')
break
if isBoardFull(board):
print('Tie Game!')
while True 
answer = input('Do you want to play again? (Y/N)')
if answer.lower() == 'y' pr answer.lower == 'yes':
board = [' ' for x in range(10)
print('----------------------------------')
main()
else:
break


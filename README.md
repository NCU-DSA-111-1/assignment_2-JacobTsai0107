# __Assignment 3 : Shogi Game In C Language(Through Linked List)__
## Introduction
It's a simple shogi game without resurrection and transform.(just basic rules)In this game, the blue first, and the person who defeats the king of the enemy wins the game. In this program, you can know the time one spend and the total time of this game. Additionally, after the game, you can save it into a binary file to review the game whenever you want. Compard to assignment 2 using array to save structure, the process of the game is saved in a structure with linked list, which needs pointer to check where the data is.
## Compile & Run & Stop

```sh
# Compile
cd ~/桌面/hw3 
//路徑位置不一定相同，可依自身路徑調整
gcc -o shogi shogi.c -lev
ls
# Run
./shogi
# Stop
^Z
```
## Usage
```c
enter 'n' for new game, 'r' for shogi manual, 's' for saving the previous game, amd 'q' to quit:n//new game
Game starts!
 9   8   7   6   5   4   3   2   1  
 香  桂  銀  金  王  金  銀  桂  香 一
    飛                     角     二
 步  步  步  步  步  步  步  步  步 三
                                 四
                                 五
                                 六
 步  步  步  步  步  步  步  步  步 七
    角                     飛     八
 香  桂  銀  金  王  金  銀  桂  香 九
blue s turn
the total time of the game is 0 sec, and the total time the blue spend is 0 sec.
enter the origin of row(段, y-axis) or enter 0 to go back to last step://wrong step detection
7
enter the origin of column(筋, x-axis):5
enter the destination of row(段, y-axis):6
enter the destination of column(筋, x-axis):6
wrong step!!
 9   8   7   6   5   4   3   2   1  
 香  桂  銀  金  王  金  銀  桂  香 一
    飛                     角     二
 步  步  步  步  步  步  步  步  步 三
                                 四
                                 五
                                 六
 步  步  步  步  步  步  步  步  步 七
    角                     飛     八
 香  桂  銀  金  王  金  銀  桂  香 九
the total time of the game is 1 sec, and the total time the blue spend is 1 sec.
enter the origin of row(段, y-axis) or enter 0 to go back to last step://correct step,changing to red
7
enter the origin of column(筋, x-axis):5
enter the destination of row(段, y-axis):6
enter the destination of column(筋, x-axis):5
action finishes! now it's red's turn 
 9   8   7   6   5   4   3   2   1  
 香  桂  銀  金  王  金  銀  桂  香 一
    飛                     角     二
 步  步  步  步  步  步  步  步  步 三
                                 四
                                 五
                步                六
 步  步  步  步      步  步  步  步 七
    角                     飛     八
 香  桂  銀  金  王  金  銀  桂  香 九
the total time of the game is 12 sec, and the total time the blue spend is 12 sec.
red s turn
//... game continues...
 9   8   7   6   5   4   3   2   1  
 香  桂  銀  金  王  金  銀  桂  香 一
    飛                     角     二
 步  步  步  步      步  步  步  步 三
                                 四
                                 五
                步               六
 步  步  步  步  王  步  步  步  步 七
    角                     飛     八
 香  桂  銀  金      金  銀  桂  香 九
red s turn
the total time of the game is 415 sec, and the total time the red spend is 372 sec.
enter the origin of row(段, y-axis) or enter 0 to go back to last step://defeated the king
6
enter the origin of column(筋, x-axis):5
enter the destination of row(段, y-axis):7
enter the destination of column(筋, x-axis):5
 9   8   7   6   5   4   3   2   1  
 香  桂  銀  金  王  金  銀  桂  香 一
    飛                     角     二
 步  步  步  步      步  步  步  步 三
                                 四
                                 五
                                 六
 步  步  步  步  步  步  步  步  步 七
    角                     飛     八
 香  桂  銀  金      金  銀  桂  香 九
red wins !!
end game
the total time of the game is 417 sec, and the total time the red spend is 374 sec.
enter 'n' for new game, 'r' for shogi manual, 's' for saving the previous game, amd 'q' to quit:s//save the game to file
name for saving file(binary file as '.dat'):shogi.dat
enter 'n' for new game, 'r' for shogi manual, 's' for saving the previous game, amd 'q' to quit:r//review the game
enter 'o' to open saved files(it will recover the previous game, suggesting saving the game first.) or 'p' to review previous game:o
name for saving file(binary file as '.dat'):shogi.dat
**********1**********
 9   8   7   6   5   4   3   2   1  
 香  桂  銀  金  王  金  銀  桂  香 一
    飛                     角     二
 步  步  步  步  步  步  步  步  步 三
                                 四
                                 五
                步               六
 步  步  步  步      步  步  步  步 七
    角                     飛     八
 香  桂  銀  金  王  金  銀  桂  香 九
please enter 'f' to forward, 'b' to backward, 'q' to quit:f//forward
**********2**********
 9   8   7   6   5   4   3   2   1  
 香  桂  銀  金  王  金  銀  桂  香 一
    飛                     角     二
 步  步  步  步      步  步  步  步 三
                步                四
                                 五
                步                六
 步  步  步  步      步  步  步  步 七
    角                     飛     八
 香  桂  銀  金  王  金  銀  桂  香 九
please enter 'f' to forward, 'b' to backward, 'q' to quit:f
**********3**********
 9   8   7   6   5   4   3   2   1  
 香  桂  銀  金  王  金  銀  桂  香 一
    飛                     角     二
 步  步  步  步      步  步  步  步 三
                步                四
                步                五
                                 六  
 步  步  步  步      步  步  步  步 七
    角                     飛     八
 香  桂  銀  金  王  金  銀  桂  香 九
please enter 'f' to forward, 'b' to backward, 'q' to quit:f
**********4**********
 9   8   7   6   5   4   3   2   1  
 香  桂  銀  金  王  金  銀  桂  香 一
    飛                     角     二
 步  步  步  步      步  步  步  步 三
                                 四
                步                五
                                 六
 步  步  步  步      步  步  步  步 七
    角                     飛     八
 香  桂  銀  金  王  金  銀  桂  香 九
please enter 'f' to forward, 'b' to backward, 'q' to quit:b//backward
**********3**********
  9   8   7   6   5   4   3   2   1  
 香  桂  銀  金  王  金  銀  桂  香 一
    飛                     角     二
 步  步  步  步      步  步  步  步 三
                步                四
                步                五
                                 六  
 步  步  步  步      步  步  步  步 七
    角                     飛     八
 香  桂  銀  金  王  金  銀  桂  香 九
please enter 'f' to forward, 'b' to backward, 'q' to quit:b
**********2**********
 9   8   7   6   5   4   3   2   1  
 香  桂  銀  金  王  金  銀  桂  香 一
    飛                     角     二
 步  步  步  步      步  步  步  步 三
                步                四
                                 五
                步                六
 步  步  步  步      步  步  步  步 七
    角                     飛     八
 香  桂  銀  金  王  金  銀  桂  香 九
please enter 'f' to forward, 'b' to backward, 'q' to quit:q//quit
enter 'n' for new game, 'r' for shogi manual, 's' for saving the previous game, amd 'q' to quit:q
//system close;
```
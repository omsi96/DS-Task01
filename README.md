![image-20220922160858276](C:\Users\vip phone\AppData\Roaming\Typora\typora-user-images\image-20220922160858276.png)

For this task, we will go through a simple **Fruit Dataset** and use **Pandas** to display the different Fruit types (apple, mandarin, orange, and lemon) in our dataset.

## How to use the starter file?

- Fork and clone [this repo](https://github.com/SimoCs/Task01) to your `tasks` folder in your device.
- You can go to [Colab](https://colab.research.google.com/) and click on **Upload** choose the  `"Task 01.ipynb"`.
- Read the starter code carefully, there are some functions you need to fill.

## Basic Requirements 🍋

1. **Alternate players**: If you first click on a button, it should show "X", then next tap on any other button should show "O"
2. **Prevent clicking on clicked button**: After clicking a button, you shouldn't be able to change it by clicking on it again.
3. **Winning**: Consider the winning situations, if X wins, show an `alert` with a message `"X wins"`. Use the pre-made function `winningAlert` and pass it the winner to present an alert with the winner string.
   
   > 💡**Tip**
   > The if statement will be very long if you try to consider all winning conditions. Break down every winning condition in a single boolean constant. For example
   ```js
   const row1 = condition
   const row2 = condition
   const row3 = condition
   // ...
   if(row1 ...)
   ```

## (Bonus) Extra Requirements 🤼‍

1. **Reset Game**: After confirming the alert, you should reset the game and play again. (You should not refres the page, or use a code that refreshes the page)
2. **Draw**: Consider the draw case, if no one wins, and present an alert that shows "Draw"

## (Extra Bonus) Styling 🎨

1. Animate the appearance of "X" and "O"
2. "X" should be shown in green, "O" should be shown in red.

# Connect4 Command

## Example
```js
module.exports = {
  name: "connect4",
  code: `$djsEval[(async () => {
 let opponent = message.mentions.members.first()
  if (!opponent) return message.channel.send("**⛔ Please provide the user to challenge**")

const { Connect4 } = require('leaf-utils')

new Connect4({
  message: message,
  opponent: message.mentions.users.first(),
  embed: {
    title: 'Connect 4',
    color: '#5865F2',
  },
  emojis: {
    player1: '🔵',
    player2: '🟡'
  },
  turnMessage: '{emoji} | Its now **{player}** turn!',
  winMessage: '{emoji} | **{winner}** won the game!',
  gameEndMessage: 'The game went unfinished',
  drawMessage: 'It was a draw!',
  askMessage: 'Hey {opponent}, {challenger} challenged you for a game of Connect 4!',
  cancelMessage: 'Looks like they refused to have a game of Connect4. \:(',
  timeEndMessage: 'Since the opponent didnt answer, i dropped the game!',
}).startGame();

})()]
$suppressErrors`
}
```
let gameScore = 0
let time = 350
// create player sprite:
let sprite: game.LedSprite = game.createSprite(2, 4)
// create enemy:
let enemy: game.LedSprite = game.createSprite(Math.randomRange(0, 4), 0)

basic.forever(function () {
    if (enemy.get(LedSpriteProperty.Y) == 4) {
        enemy.delete()  // delete enemy
        enemy = game.createSprite(Math.randomRange(0, 4), 0) // create new enemy
    }
    basic.pause(time)
    enemy.change(LedSpriteProperty.Y, 1) // move enemy down
    if (sprite.isTouching(enemy)) {
        basic.showIcon(IconNames.Heart)
    }
})

input.onButtonPressed(Button.A, function () {
    sprite.move(-1)
})

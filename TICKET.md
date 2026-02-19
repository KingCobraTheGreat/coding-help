Put the code below in your code block:

```item = api.getHeldItem(myId)
let safeTp = false
for (;;) {
if (!item) break
if (item.name == "Light Blue Carpet") safeTp = true
if (item.name == "Cyan Carpet") safeTp = Math.random <= 0.3 // random chance, must be between 0 and 1
break
}
if (safeTp) {
    api.setPosition(myId, [0, 0, 0]) // safe position
} else {
    api.setPosition(myId, [1, 1, 1]) // unsafe position
    api.sendMessage(myId, "You have been arrested!") // unsafe message
}
undefined // used to stop the result message appearing in chat

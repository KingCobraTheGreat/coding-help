For the delay every 5 minutes, you want the following code:

```lastTick = 0
tickDelay = 5*60*1000 // time in ms
tick = () => {
    if (Date.now() - tickDelay < lastTick) return
    lastTick = Date.now()
    api.getPlayerIds().forEach(ele=>{\n
        let op=api.getPosition(ele);
        if(op[1]>200) {
            api.broadcastMessage(api.getEntityName(ele)+" has crossed y level 200! Set them back", {color:"red"});
            api.setPosition(ele, op[0], 200, op[2]);
        }
    })
}

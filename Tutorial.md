# kod exempel:

Om du har en physics group med flera olika objekt i kan du lopa över dem och ändra datan i dem såhär:
```js
this.foes.children.iterate(function (child) {
    if (child != null) {
        // setData(namn på datat / varialbeln, värdet(kan vara vad som helst))
        child.setData('data', 12345)
        // getData(namn på datat / varialbeln) returnerar värdet på datan med det namn du angett
        child.getData('data')
        // if sats som använder getData() 
        if(child.getData('data') <= 0){
            // görs om data <= 0
        }
    }                    
})
```

För att lägga till ett elelement till en physics group:
```js
object = objects.create(xPos, yPos, 'sprite namn');
```

För räkna ut vinkeln mellan två grejer och sedan ge en velocity till ett object som matchar vinkeln:
```js
let v = Math.atan2((xPos1 - xPos2),(yPos1 - yPos2)) 
object.setVelocityY(Math.cos(v+Math.PI)*(-hastighet))
object.setVelocityX(Math.sin(v+Math.PI)*(-hastighet))
```

# ActionQ

These two classes create a FIFO queue that will sequentially process any SKAction that is passed into it.  
the purpose of creating this class is I was sick of having to deal with call back routines to process SKActions when 
dealing multiple sprites. this class removes the complexity of creating many sequential actions for multiple different sprites. 

### Example   
```swift
// In this example we create an ActionQ object, and use it to add two actions to 2 different sprites
 
// define the ActionQ object
let actq = ActionQ()

// add actions to the queue
actq.addNext(mySprite, action: SKAction.fadeAlphaTo(1.0, duration: 1))

// Add another action to the queue
actq.addNext(mySprite2, action: SKAction.moveTo( CGPointMake(10, 10), duration: 1))
```

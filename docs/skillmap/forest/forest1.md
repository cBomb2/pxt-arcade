# Save the Forest


## Welcome @showdialog

Welcome to MakeCode Arcade!

The last couple of summers have been some of the hottest on record and the forest service needs you to help them keep fires under control.

Let's start by setting up your plane to make sure you can get everywhere you need to be.

![Get Flying](/static/skillmap/forest/forest1.gif "Look what we're about to do today!")




## 2. Set the Scene 

**🌲 Welcome to the Forest 🌲**

---

► The [__*tilemap*__](#tiled "a scene or world created using predefined tiles") has already been set 
to a forest deep in the Australian bush.  

💡 Notice that the ``||scene:set tilemap to [ ]||`` block has been added to the ``||loops: on start||`` container so it 
loads as soon as the activity starts.



## 3. A Plane!

**🛫 We need a hero 🛬**

Choose a plane [__*sprite*__](#sprote "a 2-D image that moves on the screen") 
to fly around the screen. 

---

► From the ``||sprites:Sprites||`` category, drag 
``||variables:set [mySprite] to sprite [ ] of kind [Player]||`` 
to **the end** of the ``||loops:on start||`` container.

► To choose your plane, click the empty grey box, then toggle to **My Assets** 
and choose the **Fire Plane Right** sprite.


```blocks
tiles.setTilemap(tilemap`level1`)
// @highlight
let mySprite = sprites.create(assets.image`Fire Plane Right`, SpriteKind.Player)
```




## 4. Learn to Fly

**↔️ Time to get the sprite moving ↔️**

---

► From ``||controller:Controller||``, drag 
``||controller:move [mySprite] with buttons ⊕||``   
to **the end** of the ``||loops:on start||`` container.


```blocks
tiles.setTilemap(tilemap`level1`)
let mySprite = sprites.create(assets.image`Fire Plane Right`, SpriteKind.Player)
// @highlight
controller.moveSprite(mySprite)
```


## 5. Try It

**🕹️ Test it out in the Game Window 🕹️ **

---

Your sprite should move around the forest as you move the joypad.   
You can also use the arrow keys on your keyboard!




## 6. Follow with Camera

**😮 Ack!  Our plane flies off-screen! 😮**

---

►  To keep your sprite in sight, open ``||scene:Scene||`` and drag 
``||scene:camera follow sprite [mySprite]||`` to **the end** of the ``||loops:on start||`` container.

💡 Don't forget to play with your project after each step to see the changes your code has made.

```blocks
tiles.setTilemap(tilemap`level1`)
let mySprite = sprites.create(assets.image`Fire Plane Right`, SpriteKind.Player)
controller.moveSprite(mySprite)
// @highlight
scene.cameraFollowSprite(mySprite)

```





## Finale

👏 **You're off to a great start!** 👏   

---

When you're done, click **Finish** to 
head to the next activity where you'll add the FIRE.





```package
pxt-tilemaps=github:microsoft/pxt-tilemaps/
pxt-text=github:microsoft/arcade-text
arcade-premium-life=github:jwunderl/arcade-premium-life/
pxt-characterAnimations=github:microsoft/arcade-character-animations/
pxt-data=github:microsoft/arcade-sprite-data/
pxt-story=github:microsoft/arcade-storytelling/
arcade-sprite-util=github:jwunderl/arcade-sprite-util/
pxt-status-bar=github:jwunderl/pxt-status-bar
```

```template
tiles.setTilemap(tilemap`level1`)

```

```customts

namespace animation {
    /**
     * Loops the passed frames on the sprite at the given interval whenever
     * the specified rule is true for that sprite.
     *
     * If more than one rule applies, the most specific rule will be used.
     * If multiple rules are equally specific, the currently executing rule
     * is favored (or one is chosen at random).
     *
     * @param sprite    the sprite to animate
     * @param frames    the images that make up that animation
     * @param frame     Interval the amount of time to spend on each frame in milliseconds
     * @param rule      the rule that decides when this animation will play
     */
    //% blockId=arcade_character_loop_frames2
    //% block="animate $sprite loop frames $frames interval (ms) $frameInterval when $rule"
    //% sprite.defl=mySprite
    //% frames.defl=Fire Plane Right
    //% sprite.shadow=variables_get
    //% frames.shadow=animation_editor
    //% frameInterval.shadow=timePicker
    //% rule.shadow=arcade_character_make_rule
    //% weight=100
    //% blockGap=8
    //% help=github:arcade-character-animations/docs/loop-character-animation
    export function loopFrames2(sprite: Sprite, frames: Image[], frameInterval: number, rule: number) {
        characterAnimations.loopFrames(sprite, frames, frameInterval, rule);
    }
}
```


```assetjson
{
  "README.md": " ",
  "assets.json": "",
  "images.g.jres": "{\n    \"a5zAhGKtmEx`ww9FE(zZ\": {\n        \"data\": \"hwQEAAQAAACQCQAAmZkAAJmZAACQCQAA\",\n        \"mimeType\": \"image/x-mkcd-f4\",\n        \"displayName\": \"water\"\n    },\n    \"image1\": {\n        \"data\": \"hwQQABAAAACZmZmZmZmZmRkRERERERGRGRRBEREREZEZQRQRERERkRlBFBERERGRGRRBEREREZEZERERERERkRkRERERERGRGREREREREZEZERERERERkRkRERERERGRGREREREREZEZERERERERkRkRERERERGRGREREREREZGZmZmZmZmZmQ==\",\n        \"mimeType\": \"image/x-mkcd-f4\",\n        \"displayName\": \"q1\"\n    },\n    \"image4\": {\n        \"data\": \"hwQQABAAAACZmZmZmZmZmRkRERERERGRGREREREREZEZERERERERkRkRERERERGRGREREREREZEZERERERERkRkRERERERGRGREREREREZEZERERERERkRkUQRERERGRGUEUEREREZEZQRQRERERkRkUQRERERGRGREREREREZGZmZmZmZmZmQ==\",\n        \"mimeType\": \"image/x-mkcd-f4\",\n        \"displayName\": \"q2\"\n    },\n    \"image5\": {\n        \"data\": \"hwQQABAAAACZmZmZmZmZmRkRERERERGRGREREREREZEZERERERERkRkRERERERGRGREREREREZEZERERERERkRkRERERERGRGREREREREZEZERERERERkRkRERERFEGRGRERERFBFJEZEREREUEUkRkRERERFEGRGREREREREZGZmZmZmZmZmQ==\",\n        \"mimeType\": \"image/x-mkcd-f4\",\n        \"displayName\": \"q4\"\n    },\n    \"image6\": {\n        \"data\": \"hwQQABAAAACZmZmZmZmZmRkRERERERGRGREREREUQZEZEREREUEUkRkRERERQRSRGREREREUQZEZERERERERkRkRERERERGRGREREREREZEZERERERERkRkRERERERGRGREREREREZEZERERERERkRkRERERERGRGREREREREZGZmZmZmZmZmQ==\",\n        \"mimeType\": \"image/x-mkcd-f4\",\n        \"displayName\": \"q3\"\n    },\n    \"image3\": {\n        \"data\": \"hwQQABAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAIAIAAAAAAAAAJAIABAAAAABAJUIEAAAAANBVRQAAAAAAVFUEAAAAAEBVVQIAAAAARERUJAAAAAAAAEBEAAAAAAAAAEAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAA==\",\n        \"mimeType\": \"image/x-mkcd-f4\",\n        \"displayName\": \"fire\"\n    },\n    \"image2\": {\n        \"data\": \"hwQYAAwAAAAAAPAPAAAAAAAAgA8AAAAA8P+PDwAAAACAuIsPsPsAAACIiw+/+AAAAICI+7v4AAAAAIi7u/gAAAAAuLu7+AAAAAC4u4v5AAAA8Li7iA8AAADwuIv4AAAAAI+4i/8PAAAAj7u7+wwAAPCLu7v4AAAAv/u7ufgPAAC/+7u5+AwAAL/7u734AAAAv/+7vfgAAACfj7+9+AAAAP8AH7v4AAAAAAC/uw8AAAAAAL+LDwAAAAAA8PsAAAAAAADwDwAAAAA=\",\n        \"mimeType\": \"image/x-mkcd-f4\",\n        \"displayName\": \"Fire Plane Right\"\n    },\n    \"image7\": {\n        \"data\": \"hwQYAAwAAAAAAPAPAAAAAAAA8PsAAAAAAAC/iw8AAAAAAL+7DwAAAP8AH7v4AAAAn4+/vfgAAAC//7u9+AAAAL/7u734AAAAv/u7ufgMAAC/+7u5+A8AAPCLu7v4AAAAAI+7u/sMAAAAj7iL/w8AAADwuIv4AAAAAPC4u4gPAAAAALi7i/kAAAAAuLu7+AAAAACIu7v4AAAAgIj7u/gAAACIiw+/+AAAgLiLD7D7AADw/48PAAAAAAAAgA8AAAAAAADwDwAAAAA=\",\n        \"mimeType\": \"image/x-mkcd-f4\",\n        \"displayName\": \"Fire Plane Left\"\n    },\n    \"anim2\": {\n        \"namespace\": \"myAnimations\",\n        \"id\": \"anim2\",\n        \"mimeType\": \"application/mkcd-animation\",\n        \"data\": \"YmMwMjE4MDAxMDAwMDIwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwZmZmZmZmMDAwMDAwOGYwMDAwMDAwMGYwYmJiYmY5MDAwMDAwOGYwODAwMDBmMGJmYmJmYjBmMDAwMDAwYmY4ODAwZjA4Zjg4ZmZmZjA4MDAwMDAwYmY4Yjg4ODg4OGJiYmJiYmZmZmYwMDhmODg4OGI4YmJiYmJiYmJiYjFiYmJmZmZmZmZiZmJiYmJiYmJiOTlkZGJkYmJmYjAwMDBmMGJiYmI4OGJiYmJiYmJiOGIwZjAwMDBiZmJiOGJmODhiODg4ODg4ZmYwMDAwYjBiYmJiODhmZmZmZmZmZmZmMDAwMDAwYjA4ODg4ZjlmMDBjY2YwMDAwMDAwMDAwZjBmZmZmMGYwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwOGYwMDAwMDAwMDAwZmZmZmZmMDAwMDAwOGYwODAwMDAwMGZmYmJiYmY5MDAwMDAwYmY4ODAwMDBmMGZmZmZmZjA4MDAwMDAwYmY4Yjg4ODhmZmJiYmJiYmZmZmYwMDhmODg4OGI4YmJiYmJiOTk5OWJkYmJmZmZmZmZiZmJiYmJiYmJiYmJiYmJiYmJmYjAwMDBiZmJiOGI4OGJiYmJiYmJiOGIwZjAwYjBiYmJiODhmODhiODg4ODg4ZmYwMDAwYjA4ODg4ZjlmZmZmZmZmZmZmMDAwMDAwZjBmZmZmMGZmMDBjY2YwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMA==\",\n        \"displayName\": \"Fire Plane Right Animation0\"\n    },\n    \"anim1\": {\n        \"namespace\": \"myAnimations\",\n        \"id\": \"anim1\",\n        \"mimeType\": \"application/mkcd-animation\",\n        \"data\": \"YmMwMjE4MDAxMDAwMDIwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDBmZmZmZmYwMDAwMDAwMDAwMDAwMDAwMDA5ZmJiYmIwZjAwMDAwMDAwZjgwMDAwMDBmMGJmYmJmYjBmMDAwMDgwZjgwMDAwMDA4MGZmZmY4OGY4MGYwMDg4ZmIwMDAwZmZmZmJiYmJiYjg4ODg4OGI4ZmIwMGZmYmJiMWJiYmJiYmJiYmI4Yjg4ODhmOGJmYmJkYmRkOTliYmJiYmJiYmZiZmZmZmYwYjhiYmJiYmJiYjg4YmJiYjBmMDAwMDAwZmY4ODg4ODhiODhmYjhiYmZiMDAwMDAwMDBmZmZmZmZmZmZmODhiYmJiMGIwMDAwMDAwMDAwZmNjMDBmOWY4ODg4MGIwMDAwMDAwMDAwMDAwMDAwZjBmZmZmMGYwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDBmZmZmZmYwMDAwMDAwMDAwZjgwMDAwMDA5ZmJiYmJmZjAwMDAwMDgwZjgwMDAwMDA4MGZmZmZmZjBmMDAwMDg4ZmIwMDAwZmZmZmJiYmJiYmZmODg4OGI4ZmIwMGZmYmJkYjk5OTliYmJiYmI4Yjg4ODhmOGJmYmJiYmJiYmJiYmJiYmJiYmZiZmZmZmYwYjhiYmJiYmJiYjg4YjhiYmZiMDAwMDAwZmY4ODg4ODhiODhmODhiYmJiMGIwMDAwMDBmZmZmZmZmZmZmOWY4ODg4MGIwMDAwMDAwMDAwZmNjMDBmZjBmZmZmMGYwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMA==\",\n        \"displayName\": \"Fire Plane Left Animation\"\n    },\n    \"*\": {\n        \"mimeType\": \"image/x-mkcd-f4\",\n        \"dataEncoding\": \"base64\",\n        \"namespace\": \"myImages\"\n    }\n}",
  "images.g.ts": "// Auto-generated code. Do not edit.\nnamespace myImages {\n\n    helpers._registerFactory(\"image\", function(name: string) {\n        switch(helpers.stringTrim(name)) {\n            case \"a5zAhGKtmEx`ww9FE(zZ\":\n            case \"water\":return img`\n. 9 9 . \n9 9 9 9 \n9 9 9 9 \n. 9 9 . \n`;\n            case \"image1\":\n            case \"q1\":return img`\n9 9 9 9 9 9 9 9 9 9 9 9 9 9 9 9 \n9 1 1 1 1 1 1 1 1 1 1 1 1 1 1 9 \n9 1 4 1 1 4 1 1 1 1 1 1 1 1 1 9 \n9 1 1 4 4 1 1 1 1 1 1 1 1 1 1 9 \n9 1 1 4 4 1 1 1 1 1 1 1 1 1 1 9 \n9 1 4 1 1 4 1 1 1 1 1 1 1 1 1 9 \n9 1 1 1 1 1 1 1 1 1 1 1 1 1 1 9 \n9 1 1 1 1 1 1 1 1 1 1 1 1 1 1 9 \n9 1 1 1 1 1 1 1 1 1 1 1 1 1 1 9 \n9 1 1 1 1 1 1 1 1 1 1 1 1 1 1 9 \n9 1 1 1 1 1 1 1 1 1 1 1 1 1 1 9 \n9 1 1 1 1 1 1 1 1 1 1 1 1 1 1 9 \n9 1 1 1 1 1 1 1 1 1 1 1 1 1 1 9 \n9 1 1 1 1 1 1 1 1 1 1 1 1 1 1 9 \n9 1 1 1 1 1 1 1 1 1 1 1 1 1 1 9 \n9 9 9 9 9 9 9 9 9 9 9 9 9 9 9 9 \n`;\n            case \"image4\":\n            case \"q2\":return img`\n9 9 9 9 9 9 9 9 9 9 9 9 9 9 9 9 \n9 1 1 1 1 1 1 1 1 1 1 1 1 1 1 9 \n9 1 1 1 1 1 1 1 1 1 4 1 1 4 1 9 \n9 1 1 1 1 1 1 1 1 1 1 4 4 1 1 9 \n9 1 1 1 1 1 1 1 1 1 1 4 4 1 1 9 \n9 1 1 1 1 1 1 1 1 1 4 1 1 4 1 9 \n9 1 1 1 1 1 1 1 1 1 1 1 1 1 1 9 \n9 1 1 1 1 1 1 1 1 1 1 1 1 1 1 9 \n9 1 1 1 1 1 1 1 1 1 1 1 1 1 1 9 \n9 1 1 1 1 1 1 1 1 1 1 1 1 1 1 9 \n9 1 1 1 1 1 1 1 1 1 1 1 1 1 1 9 \n9 1 1 1 1 1 1 1 1 1 1 1 1 1 1 9 \n9 1 1 1 1 1 1 1 1 1 1 1 1 1 1 9 \n9 1 1 1 1 1 1 1 1 1 1 1 1 1 1 9 \n9 1 1 1 1 1 1 1 1 1 1 1 1 1 1 9 \n9 9 9 9 9 9 9 9 9 9 9 9 9 9 9 9 \n`;\n            case \"image5\":\n            case \"q4\":return img`\n9 9 9 9 9 9 9 9 9 9 9 9 9 9 9 9 \n9 1 1 1 1 1 1 1 1 1 1 1 1 1 1 9 \n9 1 1 1 1 1 1 1 1 1 1 1 1 1 1 9 \n9 1 1 1 1 1 1 1 1 1 1 1 1 1 1 9 \n9 1 1 1 1 1 1 1 1 1 1 1 1 1 1 9 \n9 1 1 1 1 1 1 1 1 1 1 1 1 1 1 9 \n9 1 1 1 1 1 1 1 1 1 1 1 1 1 1 9 \n9 1 1 1 1 1 1 1 1 1 1 1 1 1 1 9 \n9 1 1 1 1 1 1 1 1 1 1 1 1 1 1 9 \n9 1 1 1 1 1 1 1 1 1 1 1 1 1 1 9 \n9 1 1 1 1 1 1 1 1 1 4 1 1 4 1 9 \n9 1 1 1 1 1 1 1 1 1 1 4 4 1 1 9 \n9 1 1 1 1 1 1 1 1 1 1 4 4 1 1 9 \n9 1 1 1 1 1 1 1 1 1 4 1 1 4 1 9 \n9 1 1 1 1 1 1 1 1 1 1 1 1 1 1 9 \n9 9 9 9 9 9 9 9 9 9 9 9 9 9 9 9 \n`;\n            case \"image6\":\n            case \"q3\":return img`\n9 9 9 9 9 9 9 9 9 9 9 9 9 9 9 9 \n9 1 1 1 1 1 1 1 1 1 1 1 1 1 1 9 \n9 1 1 1 1 1 1 1 1 1 1 1 1 1 1 9 \n9 1 1 1 1 1 1 1 1 1 1 1 1 1 1 9 \n9 1 1 1 1 1 1 1 1 1 1 1 1 1 1 9 \n9 1 1 1 1 1 1 1 1 1 1 1 1 1 1 9 \n9 1 1 1 1 1 1 1 1 1 1 1 1 1 1 9 \n9 1 1 1 1 1 1 1 1 1 1 1 1 1 1 9 \n9 1 1 1 1 1 1 1 1 1 1 1 1 1 1 9 \n9 1 1 1 1 1 1 1 1 1 1 1 1 1 1 9 \n9 1 4 1 1 4 1 1 1 1 1 1 1 1 1 9 \n9 1 1 4 4 1 1 1 1 1 1 1 1 1 1 9 \n9 1 1 4 4 1 1 1 1 1 1 1 1 1 1 9 \n9 1 4 1 1 4 1 1 1 1 1 1 1 1 1 9 \n9 1 1 1 1 1 1 1 1 1 1 1 1 1 1 9 \n9 9 9 9 9 9 9 9 9 9 9 9 9 9 9 9 \n`;\n            case \"image3\":\n            case \"fire\":return img`\n. . . . . . . . . . . . . . . . \n. . . . . . . . . . . . . . . . \n. . . . . . . . . . . . . . . . \n. . . . . . . . . . . . . . . . \n. . . . . . . . . . 4 . . . . . \n. . . . 2 . . . . 4 4 . . . . . \n. . . . 2 4 . . 4 5 4 . . . . . \n. . . . . 2 4 d 5 5 4 . . . . . \n. . . . . 2 5 5 5 5 4 . . . . . \n. . . . . . 2 5 5 5 5 4 . . . . \n. . . . . . 2 5 4 2 4 4 . . . . \n. . . . . . 4 4 . . 2 4 4 . . . \n. . . . . 4 4 . . . . . . . . . \n. . . . . . . . . . . . . . . . \n. . . . . . . . . . . . . . . . \n. . . . . . . . . . . . . . . . \n`;\n            case \"image2\":\n            case \"Fire Plane Right\":return img`\n. . . . . . . . . . . . . . f f f f f f . . . . \n. . f 8 . . . . . . . . . f b b b b 9 f . . . . \n. . f 8 8 . . . . . . f f b b b b f f . . . . . \n. . f b 8 8 . . . f f 8 8 8 f f f f 8 . . . . . \n. . f b b 8 8 8 8 8 8 8 b b b b b b f f f f . . \nf 8 8 8 8 8 8 b b b b b b b b b b b b 1 b b f f \nf f f f f b b b b b b b b b 9 9 d d d b b b b f \n. . . . . f b b b b 8 8 b b b b b b b b b 8 f . \n. . . . f b b b b 8 8 f b 8 8 8 8 8 8 8 f f . . \n. . . b b b b b 8 8 f f f f f f f f f f . . . . \n. . . b 8 8 8 8 9 f . f c . f c . . . . . . . . \n. . . f f f f f f . . . . . . . . . . . . . . . \n`;\n            case \"image7\":\n            case \"Fire Plane Left\":return img`\n. . . . f f f f f f . . . . . . . . . . . . . . \n. . . . f 9 b b b b f . . . . . . . . . 8 f . . \n. . . . . f f b b b b f f . . . . . . 8 8 f . . \n. . . . . 8 f f f f 8 8 8 f f . . . 8 8 b f . . \n. . f f f f b b b b b b 8 8 8 8 8 8 8 b b f . . \nf f b b 1 b b b b b b b b b b b b 8 8 8 8 8 8 f \nf b b b b d d d 9 9 b b b b b b b b b f f f f f \n. f 8 b b b b b b b b b 8 8 b b b b f . . . . . \n. . f f 8 8 8 8 8 8 8 b f 8 8 b b b b f . . . . \n. . . . f f f f f f f f f f 8 8 b b b b b . . . \n. . . . . . . . c f . c f . f 9 8 8 8 8 b . . . \n. . . . . . . . . . . . . . . f f f f f f . . . \n`;\n        }\n        return null;\n    })\n\n    helpers._registerFactory(\"animation\", function(name: string) {\n        switch(helpers.stringTrim(name)) {\n            case \"Fire Plane Right Animation0\":\n            case \"anim2\":return [img`\n........................\n........................\n..............ffffff....\n..f8.........fbbbb9f....\n..f88......ffbbbbff.....\n..fb88...ff888ffff8.....\n..fbb8888888bbbbbbffff..\nf888888bbbbbbbbbbbb1bbff\nfffffbbbbbbbbb99dddbbbbf\n.....fbbbb88bbbbbbbbb8f.\n....fbbbb88fb8888888ff..\n...bbbbb88ffffffffff....\n...b88889f.fc.fc........\n...ffffff...............\n........................\n........................\n`, img`\n........................\n........................\n........................\n..f8..........ffffff....\n..f88.......ffbbbb9f....\n..fb88.....fffffff8.....\n..fbb88888ffbbbbbbffff..\nf888888bbbbbbb9999dbbbff\nfffffbbbbbbbbbbbbbbbbbbf\n....fbbbb888bbbbbbbbb8f.\n...bbbbb888fb8888888ff..\n...b88889fffffffffff....\n...ffffff..fc.fc........\n........................\n........................\n........................\n`];\n            case \"Fire Plane Left Animation\":\n            case \"anim1\":return [img`\n........................\n........................\n....ffffff..............\n....f9bbbbf.........8f..\n.....ffbbbbff......88f..\n.....8ffff888ff...88bf..\n..ffffbbbbbb8888888bbf..\nffbb1bbbbbbbbbbbb888888f\nfbbbbddd99bbbbbbbbbfffff\n.f8bbbbbbbbb88bbbbf.....\n..ff8888888bf88bbbbf....\n....ffffffffff88bbbbb...\n........cf.cf.f98888b...\n...............ffffff...\n........................\n........................\n`, img`\n........................\n........................\n........................\n....ffffff..........8f..\n....f9bbbbff.......88f..\n.....8fffffff.....88bf..\n..ffffbbbbbbff88888bbf..\nffbbbd9999bbbbbbb888888f\nfbbbbbbbbbbbbbbbbbbfffff\n.f8bbbbbbbbb888bbbbf....\n..ff8888888bf888bbbbb...\n....fffffffffff98888b...\n........cf.cf..ffffff...\n........................\n........................\n........................\n`];\n        }\n        return null;\n    })\n\n}\n// Auto-generated code. Do not edit.\n",
  "main.blocks": "<xml xmlns=\"https://developers.google.com/blockly/xml\"><variables><variable type=\"KIND_SpriteKind\" id=\"~zp:h99l$t:puWt^7HpS\">Fire</variable><variable type=\"KIND_SpriteKind\" id=\"b3qt}A6k{Y|Yr^LaRE6Y\">Burnt</variable><variable type=\"KIND_SpriteKind\" id=\"$J.Bxo|M{mi1P+`[A1?4\">Player</variable><variable type=\"KIND_SpriteKind\" id=\"uGq)5bGL26c-(,L_;6CB\">Projectile</variable><variable type=\"KIND_SpriteKind\" id=\"Rvp^^=8OAqmCeIUNc?{b\">Food</variable><variable type=\"KIND_SpriteKind\" id=\"@6hn/DkVnQ8`I`kv[x?{\">Enemy</variable><variable type=\"KIND_SpriteKind\" id=\"|/YN~|~tVm4.!8L*HioT\">Text</variable><variable type=\"KIND_SpriteKind\" id=\"]~dhh95wxb|OZ0;WHf|]\">StatusBar</variable><variable type=\"KIND_StatusBarKind\" id=\"nTxOIz$-~=7EJc(t7T#_\">Health</variable><variable type=\"KIND_StatusBarKind\" id=\"391Why~W9^9lqcoQQG0x\">Energy</variable><variable type=\"KIND_StatusBarKind\" id=\"GBBC+=aw4b7x0!=58!!*\">Magic</variable><variable type=\"KIND_StatusBarKind\" id=\"pJ,Vd?#{4|dO/(g(|A-H\">EnemyHealth</variable><variable id=\"8rA}EiRM2wHj_s|13j}t\">statusbar</variable><variable id=\"VLdeXP[_@1:J9GD!),Ia\">tinder</variable><variable id=\"h][qwl3T*G1}(r7MV7oZ\">mySprite</variable><variable id=\"jrX,vISS7PDA//D]zEB3\">dryGrass</variable><variable id=\"0Ko[yse36[jD#J3@^=53\">windSpeed</variable><variable id=\"fd9l0*ffabpTSLEUUfi:\">value</variable><variable id=\"d%BcCARShMY%=*.GH1gF\">list2</variable><variable id=\"aIS.OGw=J[wCQsP49qIZ\">spreadTimeBase</variable><variable id=\"lyaL+*o.a~O]/aD[uDr9\">newFire</variable><variable id=\"{V$QzFzwP$ImZ+nnTL^e\">facing</variable><variable id=\"-D8I`o1aNA~es3(JYLMk\">changeRate</variable><variable id=\"[?Yd11dvxugieayng`{_\">hoseDirection</variable><variable id=\"X[$g5gKr|jHN.aimnfy9\">projectile</variable><variable id=\"?SUf,tio_PwlgM:;5(A/\">myImage</variable><variable id=\"/LO0y==XA-vfLCV*rx!@\">mySprite2</variable><variable id=\"Yu@%}1H+Gs5NsuvWYM.y\">textSprite</variable><variable id=\"OIoJ`*MPvT]$kbOt{U=N\">textSprite2</variable></variables><comment data=\"0\" x=\"0\" y=\"0\" h=\"120\" w=\"480\">Track the remaining forest using a statusbar. You could initialize this using magic or remove the \"total tilemap rows/columns\" by just telling them what value to enter for the max/value</comment><block type=\"pxt-on-start\" x=\"-350\" y=\"-490\"><statement name=\"HANDLER\"><block type=\"variables_set\"><field name=\"VAR\" id=\"h][qwl3T*G1}(r7MV7oZ\">mySprite</field><value name=\"VALUE\"><shadow xmlns=\"http://www.w3.org/1999/xhtml\" type=\"math_number\"><field name=\"NUM\">0</field></shadow><block type=\"spritescreate\"><value name=\"img\"><shadow type=\"screen_image_picker\"><field name=\"img\">assets.image`Fire Plane Left`</field><data>{\"commentRefs\":[],\"fieldData\":{\"img\":\"myImages.image7\"}}</data></shadow></value><value name=\"kind\"><shadow type=\"spritekind\"><field name=\"MEMBER\">Player</field></shadow></value></block></value></block></statement></block></xml>",
  "main.ts": "namespace SpriteKind {\n    export const Fire = SpriteKind.create()\n    export const Burnt = SpriteKind.create()\n}\n/**\n * Track the remaining forest using a statusbar. You could initialize this using magic or remove the \"total tilemap rows/columns\" by just telling them what value to enter for the max/value\n */\nlet mySprite = sprites.create(assets.image`Fire Plane Left`, SpriteKind.Player)\n",
  "pxt.json": "{\n    \"name\": \"Save the Forest Assets Only\",\n    \"description\": \"\",\n    \"dependencies\": {\n        \"device\": \"*\",\n        \"tilemaps\": \"github:microsoft/pxt-tilemaps#v1.11.0\",\n        \"arcade-sprite-data\": \"github:microsoft/arcade-sprite-data#v0.1.0\",\n        \"arcade-sprite-util\": \"github:jwunderl/arcade-sprite-util#v0.2.4\",\n        \"arcade-story\": \"github:microsoft/arcade-storytelling#v1.0.2\",\n        \"arcade-minimap\": \"github:microsoft/arcade-minimap#v0.6.1\",\n        \"pxt-status-bar\": \"github:jwunderl/pxt-status-bar#v0.4.1\",\n        \"arcade-text\": \"github:microsoft/arcade-text#v1.3.0\"\n    },\n    \"files\": [\n        \"main.blocks\",\n        \"main.ts\",\n        \"README.md\",\n        \"assets.json\",\n        \"tilemap.g.jres\",\n        \"tilemap.g.ts\",\n        \"images.g.jres\",\n        \"images.g.ts\"\n    ],\n    \"targetVersions\": {\n        \"branch\": \"v1.5.46\",\n        \"tag\": \"v1.5.46\",\n        \"commits\": \"https://github.com/microsoft/pxt-arcade/commits/4f3f29bef862bcab766a47e42db2d3ed6b0060b1\",\n        \"target\": \"1.5.46\",\n        \"pxt\": \"7.1.25\"\n    },\n    \"preferredEditor\": \"blocksprj\"\n}\n",
  "tilemap.g.jres": "{\n    \"transparency16\": {\n        \"data\": \"hwQQABAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAA==\",\n        \"mimeType\": \"image/x-mkcd-f4\",\n        \"tilemapTile\": true\n    },\n    \"tile3\": {\n        \"data\": \"hwQQABAAAABmZmZmZmZmZmZmZmZmZmZmZmZmZmZmZmZmZmZmZmZmZmZmZmZmZmZmZmZmZmZmZmZmZmZmZmZmZmZmZmZmZmZmZmZmZmZmZmZmZmZmZmZmZmZmZmZmZmZmZmZmZmZmZmZmZmZmZmZmZmZmZmZmZmZmZmZmZmZmZmZmZmZmZmZmZg==\",\n        \"mimeType\": \"image/x-mkcd-f4\",\n        \"tilemapTile\": true,\n        \"displayName\": \"wall\"\n    },\n    \"tile2\": {\n        \"data\": \"hwQQABAAAABmZma8zGxmZmZmxsu7bGZmZma268zMbGZmZsXsxrtsZmZmzETCy2xmZmbL7sTMZmZmZcZOzrzMZmZmTOTkvMtmZma8VOTMzGZmZrwuzstsZmZmy07Cy2xmZmZL5MbMbGZmZsblvMxmZmZmxsu8zGZmZmZmzMtmZmZmZma8bGZmZg==\",\n        \"mimeType\": \"image/x-mkcd-f4\",\n        \"tilemapTile\": true,\n        \"displayName\": \"firePit\"\n    },\n    \"tile1\": {\n        \"data\": \"hwQQABAAAABmZmZmZmZmZmZmZoaIZmZmZmaGeHdoZmZmZndmdmdmZmaGdndmZ2ZmZnhmd2d3Zmxmd2d2Z3fGbHZ3Z3Znd+5sZndndmd3xm5meGZ3Z3dmbGaGdndmZ2ZmZmZ4ZnZnZmZmZoZ4d2hmZmZmZoaIZmZmZmZmZmZmZmZmZmZmZmZmZg==\",\n        \"mimeType\": \"image/x-mkcd-f4\",\n        \"tilemapTile\": true,\n        \"displayName\": \"trees\"\n    },\n    \"tile8\": {\n        \"data\": \"hwQQABAAAABm5mZmZmb+bmZmZmZm5u5uZmZm/2b2u/72Zma/b767+2ZmZvb7vfv7Zvb//+u/vO9mv+6+7P///vbr++u+7O6+v/9mv+7u7v//Zmb27/7//mbWZu/+/7vvZmb2/m++y/tmZvZvZv67+2ZvZsZm5rv+Zu5vZmbm7v5m5mZmZmbmbg==\",\n        \"mimeType\": \"image/x-mkcd-f4\",\n        \"tilemapTile\": true,\n        \"displayName\": \"smoulder\"\n    },\n    \"level1\": {\n        \"id\": \"level1\",\n        \"mimeType\": \"application/mkcd-tilemap\",\n        \"data\": \"MTAxMjAwMTIwMDAzMDMwMzAzMDMwMzAzMDMwMzAzMDMwMzAzMDMwMzAzMDMwMzAzMDEwMTAxMDEwMTAxMDEwMTAxMDEwMTAxMDEwMTAxMDEwMzAzMDEwMTAxMDEwMTAxMDEwMTAxMDEwMTAxMDEwMTAxMDEwMzAzMDEwMjAxMDEwMTAxMDEwMTAxMDEwMTAxMDEwMTAxMDEwMzAzMDEwMTAxMDEwMTAxMDEwMTAxMDEwMTAxMDEwMTAxMDEwMzAzMDEwMTAxMDEwMTAxMDEwMTAxMDEwMTAxMDEwMTAxMDEwMzAzMDEwMTAxMDEwMTAxMDEwMTAxMDEwMTAxMDEwMTAxMDEwMzAzMDEwMTAxMDEwMTAxMDEwMTAxMDEwMTAxMDEwMTAxMDEwMzAzMDEwMTAxMDEwMTAxMDEwMTAxMDEwMTAxMDEwMTAxMDEwMzAzMDEwMTAxMDEwMTAxMDEwMTAxMDEwMTAxMDEwMTAxMDEwMzAzMDEwMTAxMDEwMTAxMDEwMTAxMDEwMTAxMDEwMTAxMDEwMzAzMDEwMTAxMDEwMTAxMDEwMTAxMDEwMTAxMDEwMTAxMDEwMzAzMDEwMTAxMDEwMTAxMDEwMTAxMDEwMTAxMDEwMTAxMDEwMzAzMDEwMTAxMDEwMTAxMDEwMTAxMDEwMTAxMDEwMTAxMDEwMzAzMDEwMTAxMDEwMTAxMDEwMTAxMDEwMTAxMDEwMTAxMDEwMzAzMDEwMTAxMDEwMTAxMDEwMTAxMDEwMTAxMDEwMTAxMDEwMzAzMDEwMTAxMDEwMTAxMDEwMTAxMDEwMTAxMDEwMTAxMDEwMzAzMDMwMzAzMDMwMzAzMDMwMzAzMDMwMzAzMDMwMzAzMDMwMzAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMA==\",\n        \"tileset\": [\n            \"myTiles.transparency16\",\n            \"myTiles.tile1\",\n            \"myTiles.tile2\",\n            \"myTiles.tile3\"\n        ],\n        \"displayName\": \"level1\"\n    },\n    \"*\": {\n        \"mimeType\": \"image/x-mkcd-f4\",\n        \"dataEncoding\": \"base64\",\n        \"namespace\": \"myTiles\"\n    }\n}",
  "tilemap.g.ts": "// Auto-generated code. Do not edit.\nnamespace myTiles {\n    //% fixedInstance jres blockIdentity=images._tile\n    export const transparency16 = image.ofBuffer(hex``);\n    //% fixedInstance jres blockIdentity=images._tile\n    export const tile3 = image.ofBuffer(hex``);\n    //% fixedInstance jres blockIdentity=images._tile\n    export const tile2 = image.ofBuffer(hex``);\n    //% fixedInstance jres blockIdentity=images._tile\n    export const tile1 = image.ofBuffer(hex``);\n    //% fixedInstance jres blockIdentity=images._tile\n    export const tile8 = image.ofBuffer(hex``);\n\n    helpers._registerFactory(\"tilemap\", function(name: string) {\n        switch(helpers.stringTrim(name)) {\n            case \"level1\":\n            case \"level1\":return tiles.createTilemap(hex`12001200030303030303030303030303030303030303030101010101010101010101010101010103030101010101010101010101010101010103030102010101010101010101010101010103030101010101010101010101010101010103030101010101010101010101010101010103030101010101010101010101010101010103030101010101010101010101010101010103030101010101010101010101010101010103030101010101010101010101010101010103030101010101010101010101010101010103030101010101010101010101010101010103030101010101010101010101010101010103030101010101010101010101010101010103030101010101010101010101010101010103030101010101010101010101010101010103030101010101010101010101010101010103030303030303030303030303030303030303`, img`\n..................\n..................\n..................\n..................\n..................\n..................\n..................\n..................\n..................\n..................\n..................\n..................\n..................\n..................\n..................\n..................\n..................\n..................\n`, [myTiles.transparency16,myTiles.tile1,myTiles.tile2,myTiles.tile3], TileScale.Sixteen);\n        }\n        return null;\n    })\n\n    helpers._registerFactory(\"tile\", function(name: string) {\n        switch(helpers.stringTrim(name)) {\n            case \"transparency16\":return transparency16;\n            case \"wall\":\n            case \"tile3\":return tile3;\n            case \"firePit\":\n            case \"tile2\":return tile2;\n            case \"trees\":\n            case \"tile1\":return tile1;\n            case \"smoulder\":\n            case \"tile8\":return tile8;\n        }\n        return null;\n    })\n\n}\n// Auto-generated code. Do not edit.\n"
}
```

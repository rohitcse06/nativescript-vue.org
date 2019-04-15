---
title: ActionDialog
apiRef: https://docs.nativescript.org/api-reference/modules/_ui_dialogs_#action
contributors: [MisterBrownRSA, rigor789, ikoevska]
---

The `action()` method shows a list of selectable options and a cancellation button. Use it to let the user choose between options or dismiss the selection.

The method is part of the [`dialogs` module](https://docs.nativescript.org/api-reference/modules/_ui_dialogs_).

---

## Basic use

The `action()` method is available globally. You can call it anywhere in your app.

```JavaScript
action("Your message", "Cancel button text", ["Option1", "Option2"])
  .then(result => {
    console.log(result);
  });
```

[> screenshots for=ActionDialog <] 
## Calling Action on Button Tap
1.  Calling action function on button tap
<Button text="Say Hello" @tap="onButtonTap" />
                <!--Add your page content here-->
                
2. Script with Action:
<script>
    export default {
        methods: {
            onButtonTap() {
                action("Hello Rohit", "Cancel button text", [
                    "Option1",
                    "Option2"
                ]).then(result => {
                    console.log(result);
                });
                console.log("Button was pressed");
            }
        },

        data() {
            console.log("Button was pressed");
            return {
                message: "Hi Rohit"
            };
        }
    };
</script>
#Native Play Ground Example URL:
https://play.nativescript.org/?template=play-vue&_ga=2.157655994.1802957207.1555357206-859830356.1555357206&id=VlGR0B

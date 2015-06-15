To order your pizza you need to use the size slider to select the size of your pizza. You can scroll throught the selection and choose which one you want to order.

I modified the amount of pizzas rendered in the background from 200 to 30 which greatly reduced the frame rate issue. To further reduce the frame rate I assign document.getElementsByClassName("mover") to items so that it isn't being assigned each time the loop happens. It simply gets items. And I took out "document.body.scrollTop / 1250;" which prevents the calculation being done everytime you scroll saving you more of those precious frames.

Since we are changing the size of all the pizzas I made the calculations outside of the loop. That way each pizza knows what size it needs to be depending on the selector.
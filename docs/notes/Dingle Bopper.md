---
share: true
tags:
  - LED
  - electronics
---

What we're talking about here is the light, wire and diffuser. I wanted to try to find the optimal way to build these, since I had 128 of them to make!

- 4 conductor 22 AWG cable in a white housing
- PEX-B pipe as a collar
- WS2812D LED ([found on Ali express, from Ray Wu's store](https://www.aliexpress.us/item/2251832507785281.html?gps-id=pcStoreJustForYou&scm=1007.23125.137358.0&scm_id=1007.23125.137358.0&scm-url=1007.23125.137358.0&pvid=8a2bd986-c0af-4f42-928b-9d5504ecacd1&_t=gps-id%3ApcStoreJustForYou%2Cscm-url%3A1007.23125.137358.0%2Cpvid%3A8a2bd986-c0af-4f42-928b-9d5504ecacd1%2Ctpp_buckets%3A668%232846%238108%231977&pdp_npi=3%40dis%21USD%2112.0%2112.0%21%21%21%21%21%402103010c16872746450256228e6464%2160551219073%21rec%21US%211909564133&spm=a2g0o.store_pc_home.smartJustForYou_2004669007107.1&gatewayAdapt=glo2usa))
- A ping pong ball, as a diffuser

Since we're wiring up `WS2812D` lights, and the data lines need to be in series, I needed a 4 conductor wire. The only thing I still have any concern about with the wire, is that there is a bit of a curvature to it from being in a roll.

## The ping pong ball

I discovered a pretty good way to create holes in ping pong balls very quickly. I stick a bolt in the vice, and hit it with a torch for about fifteen seconds, and I can quickly put holes in ping-pong balls. 

![[ball-light.jpeg]]First, find the join line on the ball with a light


![[ball-bolt.jpeg]]

And voila! A hole!

## The Electronics

Each LED has to get soldered to the end of an approximate 2 ft cable. ![[led-solder.jpeg]] I haven't found a really easy way to do this, it is tedious. 🤷‍♂️

After that, I found a great product that I think is going to work well for insulation. As you can see, the conductors are eerily close above. But doing 512 heat shrinks on these tiny guys just isn't an option. So, I found "liquid tape" at the local hardware store. I think this should be totally fine since everything is going to be really static.

![[IMG_0485.jpeg]]


## Assembly

Then I just pop the LED into the hole in the ping pong ball, slide the collar on while hitting it with the hot glue gun to keep it in place.


## Testing

Another thing, is I need to make sure these things actually work before I install them. I wired up a breadboard with a few key attributes that I found helpful.

1. The ESP32 is programmed to send signal to 3 LEDs.
2. I've added a momentary button that powers the board on and off, so that as I'm wiring things up for the test I can't accidentally damage anything.
3. I've added alligator clips straight to the board, which i've affixed with staples, for attaching and testing the dingle-bopper very quickly and easily.

Once attached, I hit the button and I can see that all three lights are working. The one that I'm testing is in the middle of the series, which also shows that it's passing its signal on as intended.


## A Completed Dingle-Bopper

![[IMG_0487.jpeg]]